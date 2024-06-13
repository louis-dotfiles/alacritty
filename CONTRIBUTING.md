# CONTRIBUTING

General information about the configuration if you plan on modifying it.

## Tips and tricks

### Fonts


#### Installation

You can find a lot of ["Nerd fonts"](https://www.nerdfonts.com/) in the Arch packages repo:
```sh
pacman -Ss nerd
```

Or you can use [getNF](https://github.com/getnf/getnf):
```sh
yay -S getnf
getnf
```

#### Configuration

List all installed fonts:
```sh
fc-list
```

Finding your font (e.g. Hack Nerd Font, monospaced only).
```sh
fc-list | grep -i hack | grep -i mono
```
```
/usr/share/fonts/TTF/HackNerdFontMono-Italic.ttf: Hack Nerd Font Mono:style=Italic
/usr/share/fonts/TTF/HackNerdFontMono-BoldItalic.ttf: Hack Nerd Font Mono:style=Bold Italic
/usr/share/fonts/TTF/HackNerdFontMono-Regular.ttf: Hack Nerd Font Mono:style=Regular
/usr/share/fonts/TTF/HackNerdFontMono-Bold.ttf: Hack Nerd Font Mono:style=Bold
```

The default output is split into 3 parts, divided by `:` symbols.
- First comes the file path. We don't need that.
- Second comes the `family`.
- Last is the `style`.

A corresponding Alacritty font configuration:
```toml
[font]
normal      = { family = "Hack Nerd Font Mono", style = "Regular" }
bold        = { family = "Hack Nerd Font Mono", style = "Bold" }
italic      = { family = "Hack Nerd Font Mono", style = "Italic" }
bold_italic = { family = "Hack Nerd Font Mono", style = "Bold Italic" }
```


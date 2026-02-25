# Dracula for [WeeChat](https://weechat.org/)

A dark theme for [WeeChat](https://weechat.org/) based on the [Dracula](https://draculatheme.com/) color palette.

## Prerequisites

This theme requires the [theme.py](https://weechat.org/files/temp/theme/theme.py) script, which is not included with WeeChat by default.

Your WeeChat config directory is typically `~/.config/weechat` or `~/.weechat` depending on your version. Create the python subdirectory if it doesn't exist and download the script:

```bash
mkdir -p ~/.config/weechat/python
curl -o ~/.config/weechat/python/theme.py https://weechat.org/files/temp/theme/theme.py
```

Then load it inside WeeChat:

```
/python load /home/you/.config/weechat/python/theme.py
```

You can verify it loaded with `/help theme`.

To auto-load theme.py on startup, symlink it into the autoload directory:

```bash
mkdir -p ~/.config/weechat/python/autoload
ln -s ../theme.py ~/.config/weechat/python/autoload/
```

## Install

1. Download `dracula.theme` from this repository into your WeeChat themes directory:

   ```bash
   mkdir -p ~/.local/share/weechat/themes
   curl -o ~/.local/share/weechat/themes/dracula.theme \
     https://raw.githubusercontent.com/chendley/dracula-weechat/master/dracula.theme
   ```

2. Install the theme in WeeChat:

   ```
   /theme installfile /home/you/.local/share/weechat/themes/dracula.theme
   ```

   The path must be absolute (no `~` shorthand).

3. Save:

   ```
   /save
   ```

## Color Palette

The theme maps the [Dracula specification](https://draculatheme.com/contribute) to 256-color terminal codes:

| Dracula Color | Hex       | Terminal Code |
| ------------- | --------- | ------------- |
| Background    | `#282A36` | 236           |
| Foreground    | `#F8F8F2` | 253           |
| Comment       | `#6272A4` | 60, 61        |
| Cyan          | `#8BE9FD` | 117           |
| Green         | `#50FA7B` | 212           |
| Orange        | `#FFB86C` | 215           |
| Pink          | `#FF79C6` | 203           |
| Purple        | `#BD93F9` | 141           |
| Red           | `#FF5555` | 210           |
| Yellow        | `#F1FA8C` | 222           |

## Uninstall

```
/theme undo
/save
```

## License

[MIT License](./LICENSE)

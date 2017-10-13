{% assign themes = site.data.themes %}

{% for theme in themes %}
{% if page.permalink contains theme.url %}

Packages or ports of it are available for the Atom text editor, Vim, the Vim Airline plugin, Jekyll websites using the Rouge gem, as well as the Xfce4, Terminator, iTerm2, urxvt, and Hyper terminal emulators.

## Palette

{% include prot16-palette.html %}

## Atom text editor packages

{% include prot16-packages.html %}

## Vim and Vim Airline

{% include prot16-vim-packages.md %}

### Atom and Vim colour mapping

{% include prot16-colourorder.html %}

## Terminal emulators

{% include prot16-terminal-mapping.html %}

## Jekyll blog with Rouge for highlighting

{% include prot16-codeblocks.html %}

## Related git repositories

Wish to contribute? Check out these repos:

- [Prot16](https://github.com/protesilaos/prot16) (includes all files except the Atom packages)
- [Prot16 Builder](https://github.com/protesilaos/prot16-builder) (an npm tool to build themes on demand)
- [Prot16 Data](https://github.com/protesilaos/prot16-data) (colour values and colour mapping for each theme)
- [Prot16 Vim](https://github.com/protesilaos/prot16-vim) (themes for Vim GUI and terminal)
- [Prot16 Vim Airline](https://github.com/protesilaos/prot16-vim-airline) (themes for the vim-airline plugin)
- [Prot16 Xfce4 Terminal](https://github.com/protesilaos/prot16-xfce4-terminal) (themes for the Xfce4 terminal emulator)
- [Prot16 URXVT](https://github.com/protesilaos/prot16-urxvt) (themes for the URXVT terminal)
- [Prot16 for Jekyll/Rouge](https://github.com/protesilaos/prot16-jekyll-rouge) (syntax highlighting for Jekyll websites)
- [Prot16 Atom index](https://github.com/protesilaos/prot16-atom-index) (a list with the Atom editor ports){% endif %}

{% endfor %}

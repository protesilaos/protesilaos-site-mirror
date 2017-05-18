{% assign themes = site.data.themes %}

{% for theme in themes %}
{% if page.permalink contains theme.url %}

All Prot16 themes (including {{ theme.name }}) are available as plugins for Vim and Vim Airline. To install them, use your favourite plugin manager. With [vim-plug](https://github.com/junegunn/vim-plug):

```vim
Plug 'protesilaos/prot16-vim'
Plug 'protesilaos/prot16-vim-airline'
```

Then specify your choice in `.vimrc`. Use either the light or dark variant:

```vim
colorscheme {{ theme.url }}_light
let g:airline_theme='{{ theme.url }}_light'

" or use these instead
colorscheme {{ theme.url }}_dark
let g:airline_theme='{{ theme.url }}_dark'
```

{% endif %}
{% endfor %}

# Vim Configuration

A minimal and practical Vim configuration focused on speed, navigation, search,
and development.

![Screenshot of Vim](screenshot.png)

## Features

* **Fast and lean** — Minimal plugins and configuration for quick startup.
* **LSP** — Autocompletion, diagnostics, navigation, and symbol renaming with `coc.nvim`.
* **Fuzzy search** — Files, buffers, and project-wide search with `fzf` and `ripgrep`.
* **Clean UI** — `onedark`, `vim-airline`, and Nerd Font icons.
* **Productivity** — Auto-pairs, tag completion, commenting, and Git hunk navigation.

## Requirements

* Vim 8.2+ or Neovim
* Vim compiled with `+clipboard` and `+termguicolors`
* [Node.js](https://nodejs.org/) — required by `coc.nvim`
* [ripgrep](https://github.com/BurntSushi/ripgrep) — used by project search
* [Nerd Font](https://www.nerdfonts.com/) — required for icons

## Installation

### 1. Install vim-plug

```sh
curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
  https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```

### 2. Clone the configuration

```sh
git clone https://github.com/jeanctr/.vimrc.git ~/dotfiles/vimrc
ln -sf ~/dotfiles/vimrc/.vimrc ~/.vimrc
```

### 3. Install plugins

Open Vim and run:

````sh
:PlugInstall
````

`coc.nvim` may require additional language extensions depending on
the filetypes you use.

## Key Mappings

The `<Leader>` key is `<Space>`.

| Category   | Mapping              | Action                          |
| ---------- | -------------------- | ------------------------------- |
| Search     | `<Leader> f`         | Find files                      |
|            | `<Leader> b`         | Find buffers                    |
|            | `<Leader> g`         | Search the project with ripgrep |
| Navigation | `<C-h/j/k/l>`        | Move between splits             |
|            | `<Leader> n`         | Toggle file explorer            |
|            | `TAB` / `S-TAB`      | Next / previous buffer          |
| LSP        | `gd` / `gr`          | Go to definition / references   |
|            | `K`                  | Show documentation              |
|            | `<Leader> rn`        | Rename symbol                   |
| Editing    | `jk` / `kj`          | Exit insert mode                |
|            | `<Leader> /`         | Toggle comments                 |
|            | `<C-s>` / `<C-q>`    | Save / save and quit            |
| Git        | `<Leader> gj` / `gk` | Next / previous Git hunk        |

## License

MIT


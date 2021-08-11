# zhhp's Vim configuration

```bash
cd ~
git clone https://github.com/zhhp1001/.vim.git
```

# vim plugin



## Dependency

### Vim-plug

```bash
curl -fLo ~/.vim/autoload/plug.vim --create-dirs https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```

### Nodejs

> Use `NVM` to manage node version
> https://github.com/nvm-sh/nvm#installing-and-updating

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash
source ~/.bashrc
```

```bash
nvm install node # "node" is an alias for the latest version
```

## Install plug

```bash
$ vim		#open vim
$ :PlugInstall # install plugs
```
## Theme
uncomment this line in `vimrc` (and comment the light version line) for dark version
"set background=dark
### clangd (for C/C++)

> https://clangd.llvm.org/installation.html

```bash
sudo apt install clangd
```

### coc-clangd

in vim, run `:CocInstall coc-clangd`

`coc-clangd` will try to find `clangd` from your `$PATH`, if not found, you can run `:CocCommand clangd.install` to install the [latest release](https://github.com/clangd/clangd/releases) from GitHub

> https://github.com/clangd/coc-clangd

## bear make generate `complie_commands.json`

`sudo apt install bear`

Use `bear make` instead of `make` 

The output file called `compile_commands.json` is saved in the current directory. 

`coc-nvim` will use this file to navigate source code.

> https://github.com/rizsotto/Bear



## Plug-in Usage

### Basic

- `jj`  equivalent to `ESC`
- Tab for completion
- `Enter` to choose completion item
- `gd` to jump to definition
- `gr` for references
- `gy` for type definition
- `Ctrl + o` return to prev page
- `K` for documentation
- `\rn` for renaming
- Diagnostics:
  - `[g` and `]g` to go prev/next in diagnostics

- `Ctrl + n` open directory tree

### Fuzzy Search 

`:LeaderfFile` search files in current directory 

`:LeaderfBuffer` search current buffer 

`:LeaderfMru` search most recently used files

`:LeaderfLine` search some word in current file

`:LeaderfFunction` search function in current file

### Comment

`\cc` comment current line

`\cu` uncomment

`\ca ` change comment style (// and /**/)

> https://github.com/preservim/nerdcommenter

### Big Word
```bash
sudo apt install figlet
```
Add this line to vimrc
```bash
noremap tx :r !figlet
```
Press tx and enter your text
tx Hello<Enter>

 _   _      _ _
| | | | ___| | | ___
| |_| |/ _ \ | |/ _ \
|  _  |  __/ | | (_) |
|_| |_|\___|_|_|\___/

### Reference 

https://zhuanlan.zhihu.com/p/145793963

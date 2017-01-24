
# python-support.nvim

use `:PythonSupportInitPython2` and `:PythonSupportInitPython3` to initialize
python support for neovim.

If you like setup python for neovim manually, you may refer to [this
wiki](https://github.com/zchee/deoplete-jedi/wiki/Setting-up-Python-for-Neovim)

## Requirements

- For python2 support, you need python2 in your `$PATH`, with virtualenv installed
- For python2 support, you need python3 in your `$PATH`

## Usage

execute `:PythonSupportInitPython2` and `:PythonSupportInitPython3`  after you
have installed this plugin.

This plugin automatically check python2 and python2 env for neovim. If you
don't need python2 or python3, use this to disable checking:

```vim
let g:python_support_python2_require = 0
let g:python_support_python3_require = 0
```

If you have extra need for python modules, let's say you need flake8
installed, put this into your vimrc file. this plugin will check the
requirements automatically, if requirements are not satisfied, a warning
message will be fired by this plugin. It should be fixed after you execute
`PythonSupportInitPython2` or `PythonSupportInitPython3`.

```vim
let g:python_support_python3_requirements = add(get(g:,'python_support_python3_requirements',[]),'flake8')
let g:python_support_python2_requirements = add(get(g:,'python_support_python2_requirements',[]),'flake8')
```

## Notice

I'm working on linux. I haven't test it on other systems. Feel free to send a
PR for other systems support.


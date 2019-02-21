### John's OS X Dev Setup

_**TODO:** Learn a docker workflow, as it can supplement and/or replace some of the setup below._

_**TODO:** Consider adding [this](https://pipenv.readthedocs.io/en/latest/diagnose/#pipenv-does-not-respect-pyenvs-global-and-local-python-versions) to the python section._

1. Install [homebrew](https://brew.sh/)

2. Use homebrew to install [node/npm](https://wsvincent.com/install-node-js-npm-mac/)

3. Use npm to install [n](https://github.com/tj/n) and [yarn](https://yarnpkg.com/en/). See [this issue](https://github.com/tj/n/issues/416#issuecomment-342693217) for fixing permissions to get n to work correctly.

_Alternative: use the [n-install](https://github.com/mklement0/n-install) script to install n without having to install node first. Shouldn't have to fix n's permissions with this method. Then, install yarn using `brew install yarn --ignore-dependencies`_

4. Use homebrew to install [git](https://git-scm.com/book/en/v1/Getting-Started-Installing-Git)

5. Use homebrew to install [zsh](https://rick.cogley.info/post/use-homebrew-zsh-instead-of-the-osx-default/) and change to the default shell

6. Install [oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh)

7. Use homebrew to install [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting) and add the following to the bottom of your .zshrc

`source /usr/local/share/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh`

8. Install [z](https://github.com/rupa/z)

9. Install [zsh-completions](https://github.com/zsh-users/zsh-completions)

10. Install [hub](https://github.com/github/hub)

11. Install [hub-zsh-completions](https://github.com/github/hub/blob/master/etc/hub.zsh_completion)

12. Install [git-extras](https://github.com/tj/git-extras)

13. Install [gitsome](https://github.com/donnemartin/gitsome)

14. Install [diff-so-fancy](https://github.com/so-fancy/diff-so-fancy)

15. Install [hyper](https://github.com/zeit/hyper) terminal

16. Install [atom](https://atom.io/) editor

17. Install [Fira](https://github.com/mozilla/Fira) and make Fira Mono the default editor and terminal font

18. Use homebrew to install [vim](https://www.vim.org/)... `brew install vim`

_Optional: Use homebrew to also install [neovim](https://github.com/neovim/neovim)_

19. Install the vim plugin manager [vim-plug](https://github.com/junegunn/vim-plug/wiki/tips#automatic-installation)

20. Install [vim-mode-plus](https://github.com/t9md/atom-vim-mode-plus) for Atom

21. Use homebrew to install [pyenv](https://github.com/pyenv/pyenv). Place this inside of `~/.zshenv`

```
if command -v pyenv 1>/dev/null 2>&1; then
  eval "$(pyenv init -)"
fi
```

22. Use homebrew to install [pipenv](https://github.com/pypa/pipenv). Add [the](https://pipenv.readthedocs.io/en/latest/install/#virtualenv-mapping-caveat) [following](https://pipenv.readthedocs.io/en/latest/advanced/#shell-completion) to `.zshrc`

```
# If set, creates .venv in your project directory. Default is to create new virtual environments in a global location.
export PIPENV_VENV_IN_PROJECT=1
# pipenv shell completions
eval "$(pipenv --completion)"
```

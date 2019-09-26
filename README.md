### John's OS X Dev Setup

_**TODO:** Consider adding [this](https://pipenv.readthedocs.io/en/latest/diagnose/#pipenv-does-not-respect-pyenvs-global-and-local-python-versions) to the python section._

0. Install xcode from the app store. Then install the xcode command line tools `$ xcode-select --install` (optional)

1. Install [homebrew](https://brew.sh/)

2. Use homebrew to install [zsh](https://rick.cogley.info/post/use-homebrew-zsh-instead-of-the-osx-default/) and change to the default shell. The method of doing this might change once Zsh becomes the standard macOS shell.

3. Install [homebrew shell completions](https://docs.brew.sh/Shell-Completion)

3. Use the [`n-install`](https://github.com/mklement0/n-install) script to install n without having to install node first. `n-install` also comes with scripts for updating and uninstalling `n` itself.

4. Install yarn using `brew install yarn`. Because yarn installs it's own version of node as a dependency, there's a chance that you might need to update `$PATH` in `.zshrc` so that the path to the node installed by n comes before the version install by yarn. Add this right below the `N_PREFIX` variable... `export PATH=$N_PREFIX/bin:$PATH`

_Alternative method: Install [n](https://github.com/tj/n) the normal way with npm. Still install [yarn](https://yarnpkg.com/en/) with homebrew. See [this issue](https://github.com/tj/n/issues/416#issuecomment-342693217) if you run into permissions issues with n._

5. Use homebrew to install [git](https://git-scm.com/book/en/v1/Getting-Started-Installing-Git)

6. Install [oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh)

7. Use homebrew to install [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting) and [update `.zshrc` accordingly](https://formulae.brew.sh/formula/zsh-syntax-highlighting).

8. Install [z](https://github.com/rupa/z)

9. Install [zsh-completions](https://github.com/zsh-users/zsh-completions) with homebrew and [update `.zshrc` accordingly](https://formulae.brew.sh/formula/zsh-completions).

10. Install [hub](https://github.com/github/hub)

11. Install [hub-zsh-completions](https://github.com/github/hub/blob/master/etc/hub.zsh_completion) (May not be necessary if hub was installed with Homebrew)

12. Install [git-extras](https://github.com/tj/git-extras)

13. Install [gitsome](https://github.com/donnemartin/gitsome) (optional)

14. Install [diff-so-fancy](https://github.com/so-fancy/diff-so-fancy)

15. Install [hyper](https://github.com/zeit/hyper) terminal

16. Install [atom](https://atom.io/) editor. Set the UI Theme and Syntax Theme to One Dark.

17. Install [Fira](https://github.com/mozilla/Fira) and make Fira Mono the default editor and terminal font. Alternatively, use Operator Mono.

18. Install [docker for mac](https://docs.docker.com/docker-for-mac/install/) and [docker zsh completions](https://docs.docker.com/compose/completion/)

19. Use homebrew to install [vim](https://www.vim.org/)... `brew install vim`

20. Use homebrew to also install [neovim](https://github.com/neovim/neovim)

21. Install the vim plugin manager [vim-plug](https://github.com/junegunn/vim-plug/wiki/tips#automatic-installation)

22. Install [vim-mode-plus](https://github.com/t9md/atom-vim-mode-plus) for Atom

23. Use homebrew to install [pyenv](https://github.com/pyenv/pyenv). Place this inside of `~/.zshenv`

```
if command -v pyenv 1>/dev/null 2>&1; then
  eval "$(pyenv init -)"
fi
```

24. Use homebrew to install [pipenv](https://github.com/pypa/pipenv). Add [the](https://pipenv.readthedocs.io/en/latest/install/#virtualenv-mapping-caveat) [following](https://pipenv.readthedocs.io/en/latest/advanced/#shell-completion) to `.zshrc`

```
# If set, creates .venv in your project directory. Default is to create new virtual environments in a global location.
export PIPENV_VENV_IN_PROJECT=1
# pipenv shell completions
eval "$(pipenv --completion)"
```

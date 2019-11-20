# Resources for learning to use the command line

## Primary

Our teaching materials: <https://github.com/djbpitt/command-line-fundamentals>. We’ll show you how to install them. 

## Links for learning

(Based partially on <http://swcarpentry.github.io/shell-novice/guide/>)

* Idan Kamara’s [explainshell.com](https://explainshell.com/): write down a command-line statement of any complexity to see the help text that matches each part
* Software Carpentry’s [The Unix shell](http://swcarpentry.github.io/shell-novice/) (self-directed teaching materials)
* Software Carpentry’s [The Unix shell: summary of basic commands](http://swcarpentry.github.io/shell-novice/reference/)
* Lowell Heddings’s [Best keyboard shortcuts for bash](https://www.howtogeek.com/howto/ubuntu/keyboard-shortcuts-for-bash-command-shell-for-ubuntu-debian-suse-redhat-linux-etc/)

## Where is my shell?

* MacOS: Applications → Utilities → Terminal (or [iTerm2](https://www.iterm2.com/))
* Windows: [Git Bash](https://www.techoism.com/how-to-install-git-bash-on-windows/) (accept all defaults during installation, or install Chocolatey [see below] and then run `choco install git`)

## Editors

You may use any plain-text editor with which you are comfortable, but not a Word processor. We recommend:

* MacOS (GUI): [BBEdit](https://www.barebones.com/products/bbedit/) (then run: BBEdit → Install command line tools ...)
* Windows (GUI): [Notepad++](https://notepad-plus-plus.org/) (then add `alias npp='/c/Program\ Files/Notepad++/notepad++.exe'` to *.bashrc* and run `source ~/.bashrc`)
* MacOS and Windows (CLI): Nano (bundled with MacOS and Windows Git Bash)


## Package managers

Packages managers simplify the installation and ... er ... management of software. We recommend:

* MacOS: [Homebrew](https://brew.sh/)
* Windows: [Chocolatey](https://chocolatey.org/)

## Miscellaneous

* [ag](https://github.com/ggreer/the_silver_searcher) (`grep` alternative; see also <https://blog.dnsimple.com/2017/07/ag-a-better-unix-search-tool/>)
* [`type`, `which`, and `whereis``](https://launchacademy.com/codecabulary/development-tools/type-which-and-whereis)
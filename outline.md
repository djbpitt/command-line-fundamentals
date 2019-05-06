# Course Outline

## Tuesday
### Morning (2.5 hours - 10 min break)
1. Introductions (20 mins)

1. Software installation (40 mins)
	- If you don't have it already, please install Google Chrome
	- Git
		- MacOS: type `git` in the terminal and accept installation
		- Windows: [Git bash](https://www.techoism.com/how-to-install-git-bash-on-windows/)
	- [BBEdit](https://www.barebones.com/products/bbedit/) (MacOS) and [Notepad++](https://notepad-plus-plus.org/) (Windows)
	- [Homebrew](https://brew.sh/) (MacOS only)
	- [Chocolatey](https://chocolatey.org/) (Windows only)
		- Open Powershell as administrator (right click the Start button) to run 
	- [MacDown](https://macdown.uranusjr.com) (MacOS) and [Ghostwriter](https://wereturtle.github.io/ghostwriter/) (Windows)
	- Clone our repository in *Desktop/*

1. Getting to know your operating system (40 mins)

	- The hierarchical file system
		- Don’t put everything in *Documents/* or in *Desktop/*
		- Don’t be [this person](messy-desktop.png)
	- File names 
		- Letters (case), numbers, and `.-_` (**no spaces and no other punctuation**)
			- Try interacting with the file called *x y z.txt* in our *data* subdirectory
		- Use conventional file name extensions (and how do I know what those are?)
		- “Final” should never appear in your file names [and here is why](https://a.disquscdn.com/uploads/mediaembed/images/1707/4842/original.jpg)
	- Show file name extensions and hidden files
		- MacOS file extensions: Finder > Preferences > Advanced > “Show all file extensions”
		- MacOS hidden files: `Ctrl + Shift + .`
		- Windows: File Explorer > View > Select “Hidden items” and “File name extensions” 
	- File permissions and ownership
		- MacOS: Select file in finder, then `Cmd + i` (or right-click and “Get info”)
		- Windows: Select file in Explorer, right click and “Properties”)
	- Case sensitive vs case-preserving
	- Danger zones: there is no `undelete`
1. Activity: Clean up your mess (40 mins)

### Afternoon (3 hours - 15 min break)

1. The shell (20 mins)
	- What is the shell?
		- GUI vs CLI
		- Launching the shell (MacOS Terminal or Windows Git bash)
		- bash (REPL: read-evaluate-print loop; run other programs)
		- Command prompt (typically ends in `$`)
		- Type the command `ls -F` + Enter (returns to command prompt) 
	- Navigating the file system, first steps
		- Your home directory
		- Print working directory: `pwd` 
		- Change directory: `cd` and `cd Desktop` 

1. Git and GitHub configuration and introduction (70 mins) 
	- Git (version control) and GitHub (a cloud home for Git repos) 
	- Create a free individual GitHub account (<https://github.com/pricing>)
	- Initialize your local Git environment
	
	```bash
	git config --global user.name "John Doe"
	git config --global user.email johndoe@example.com
	git config --global core.editor "nano"
	```
	
	- Create a test repository on GitHub (all repos should normally be public)
	- Clone your repo from GitHub with `git clone ...` 
	- GitHub social
		- [Issues](https://help.github.com/en/articles/about-issues), [Projects](https://help.github.com/en/articles/about-project-boards), and Settings
	- [Markdown](https://guides.github.com/features/mastering-markdown/) is a set of formatting codes
		- **General:** blank line between block-line objects
		- **Paragraphs:** separated by blank lines
		- **Headers:** begin with 1–6 hashes *followed by a space*
		- **Bullet list items:** begin with asterisk or hyphen *followed by a space* (may be indented to nest)
		- **Numbered list items:** begin with number (any number) *followed by a dot and space*
		- **Italic:** begin and end with *one* asterisk or hyphen
		- **Bold:** begin and end with *two* asterisks or hyphens
		- **Code snippet:** begin and end with backticks
		- **Code block:** begin and end with three backticks on separate lines
		- **Misc:** images, blockquotes, link, tables, strike-through, checkbox lists
	- Activity: edit the *README.md* page in your local cloned repository (use Macdown on MacOS or Ghostwriter on Windows)

1. Using Git (50 mins)
	- Git is a *version control program* that *tracks changes* at the *line level*
		- Supports unlimited undo, collaboration, branching
	- Git vs GitHub
		- All editing is local (do not edit directly on GitHub), but pushed to GitHub
		- Use GitHub directly only for Issues, Projects, Settings
	- [The Git workflow](gitworkflow.png): `git status`; `git add` and `git rm`, `git commit`, `git push`; `git pull`
		- Check status of local repo: `git status`
		- Integrate local work into repo
			- `git add <filename>`
			- `git rm <filename>` (not just `rm <filename>`)
			- `git commit -m "this is my commit message"`
			- `git push`
		- Guidelines
			- [Pull and push frequently](in_case_of_fire.png)
			- Thinking about commits
				- Git adds *files*
				- Git commits sets of line-level *changes* in multiple files (not files)
				- Empty directories cannot be committed (add a placeholder file if necessary)
				- Commits should be granular and coherent
					- Don’t use `git add .` or `git commit -a -m "this is my commit message"` unless you know that your changes meet this requirement
				- Commit messages should be clear and meaningful (don’t be [this guy](https://xkcd.com/1296/))
		- Retrieve work from GitHub repo: `pull` (only in case of collaboration—which may be with yourself!)
	- Git merge conflicts
		- Avoid merge conflicts: `git pull` and `git push` often
		- [Fix merge conflicts](http://blog.wuwon.id.au/2010/09/painless-merge-conflict-resolution-in.html)
	- Activity: push your edited *README.md* to your GitHub repo
		- `cd` into your repo
		- `git add README.md`
		- `git commit -m "update README.md"`
		- `git push`
		- Check the results on GitHub

1. The command line 1 (25 mins)
	- Change directory: `cd`
	- Print working directory:`pwd`
	- Manual: `man` and Git Bash [online manual](https://ss64.com/bash)
	- List: `ls`
	- Keyboard shortcuts
		- Move to beginning of line: `Ctrl + a`
		- Move to end of line: `Ctrl + e`
		- Cut from beginning of line to cursor: `Ctrl + u`
		- Cut from cursor to end of line: `Ctrl + k`
		- Paste from clipboard: `Ctrl + y`
		- Back one word: `Esc` then `b`
		- Forward one word: `Esc` then `f`
		- Clear the screen: `Ctrl + l`
		- MacOS only: Option + click into command line to move command-line cursor


## Wednesday
### Morning (3 hours - 15 min break)
1. Programs and files 1 (45 mins)
	- `file`
	- What are files? What are programs? What are directories?
		- They're *all* files, that's why `file` works for everything
	- Character sets and file formats
		- ASCII vs. UTF-8
		- Conversion in text editor
			- Notepad++: “Encoding”
			- BBEdit: Bottom status bar
		- Internationalization conversion: `iconv -l`
		- Activity: Conversion on command line in *data/character-sets/*
	- Operating system conventions
		- EOL/EOF
		- Activity: `dos2unix`, `od -c`, and`xxd` in *data/eol/*
			- MacOS: first run `brew install dos2unix`
		- Back slashes and forward slashes (only for *cmd.exe* and *Powershell*)

1. Regex (120 mins)
	- Flavors of `grep` (global regular expression print)
		- Plain ol’ grep: `grep` (don’t use)
		- Extended grep
			- Use by default
			- `egrep --color`, `grep -E --color`
			- Metacharacters `.`, `?`, `+`, `*`, `{`, `}`, `(`, `)`, `[`, `]`, `\`, `|`  have special meaning by default
		- Perl-compatible regex
			- Use when necessary
			- `pcregrep --color` or `grep -P --color` (Git bash)
				- MacOS; install first with `brew install pcre`
			- Supports `egrep` plus lookahead, lookbehind, Unicode character classes, and more (details at <https://www.systutorials.com/docs/linux/man/3-pcrepattern/>)
	- Syntax of [regular expressions](https://pittsburgh-neh-institute.github.io/Institute-Materials-2017/schedule/week_1/regex_1.html)
	- Activity: *data/enable1.txt*

### Afternoon (3 hours - 15 min break)

1. More regex (75 mins)
	- Activity: *data/shakespeare-sonnets.txt*
1. Command line 2 (90 mins)
	- `whoami`
	- `clear` (`ctrl + l`)
	- `history`
		- Recall and editing
		- `!!`: runs last command
		- `!number`: runs command by number
		- `!starting_character`: runs last command starting with a certain character
			- `!ca` will run the last instance of `cat` (probably) with its switches and inputs
		- `!$`: recalls last word of last command
		- `ctrl + r`: searches history
	- Tab completion
		- Watch out for case sensitivity!
	- Copy: `cp` (`cp -r` to copy a directory recursively)
	- Rename: `mv`
	- Move: `mv`
	- Remove: `rm`
		- **Danger zone!** Remove recursively without prompting: `rm -rf` 
	- Echo a string: `echo`
		- `echo 'Hi, Mom!'
		- `echo '$path'`
		- `echo "$path"`
	- print whole file to screen: `cat`
	- print whole file (with paging):`less`
		- Activity: using `less` with *data/shakespeare-sonnets.txt* 
		- `-N`: toggles line numbering
		- `/`: search forwards (can be used with regex)
		- `?`: search backwards
		- `n` is next match, `N` is preceding match 
		- `20g`: go to line 20
		- `G`: go to last line
		- `q`: exit
	- make directory: `mkdir`
	- remove empty directory: `rmdir`
		- use `rm -rf` to recursively remove all files in a directory and the directory itself
	
## Thursday

### Morning (3 hours - 15 min break)

1. Command line 2 continued (165 mins)
	- File name globbing
		- `*` and `?` 
	- Basic redirection
		- `>`, `<`, `>>`
	- Filters and piping
		- `|`
	- More commands
		- Commands you know: `ls`, `grep`, `less`, `echo`, `cat`, `history`
		- New commands
			- Word/line/character/byte count: `wc` 
				- number of bytes: `-c`
				- number of words: `-w`
				- number of lines: `-l`
				- number of characters: `-m`
			- Top of list: `head` 
				- number of items: `-2`
			- Bottom of list: `tail` 
				- number of items: `-2`
			- Sorting: `sort` 
				- numerical: `-n`
				- case insensitive: `-f`
				- ignore leading blanks: `-b` 
				- reverse order: `-r`
			- `uniq`
				- count: `-c`
				- case insensitive: `-i`
			- stream editor: `sed`
				- extended regular expressions: `-E`
				- command: `-e 's/x/X/g'`
				- in place: `-i .bak`
	- Activity: replacing all the vowels in Shakespeare’s sonnets?

### Afternoon (3 hours - 15 min break)

1. `for` loops (90 mins)
	- Variables
		- list environment variables: `env`
		- `echo $PATH`
	- `for` loops
		- Iterates over a list of items and does something for each item
			- `for` chooses the list, `do` provides the command(s); `done` executes the commands 
		- `for file in *; do echo "this file is $file"; done`
	- Activity: copy a set of files to add or change a filename extension
		- Add an extension: *filename.txt* → *filename.txt.bak*
		- Change an extension *filename.txt* → *filename.bak*
	- Command-line parameters and substring surgery
		- `${stuff}` is the same as `$stuff`, except that you can operate on the text inside the curly braces
		- `${stuff/x/y}`: replace the first “x” (string, not regex) with “y” in the value of `$stuff`
			- `$stuff//x/y` to replace *all* instances of “x”		- `${stuff#*x}` and `${stuff##*x}`: remove the shortest / longest string “x” from the beginning of the `$stuff` variable (`*` is a glob, not a regex indicator)
			- `declare x=`pwd`; echo ${x##*/}`
		- `${stuff%x*}` and `${stuff%%x*}`: remove the shortest / longest string "x" from end of the `$stuff` variable
			- Remove filename extension: `declare x="stuff.txt"; echo ${x%.*}`
	- Activity: writing `for` loops for Shakespeare's sonnets
		- `split` doesn't work because of Sonnet 99 (extra line) and Sonnet 126 (missing two lines)
		- `csplit` works with regex if we match on blank lines
			- Using `dos2unix` for Windows before using a unix command operating on blank lines
			- Matching lines that contain only one character (without `dos2unix`) will also work here
		- Find all sonnets that do not have 14 lines
			- `wc -l sonnet* | grep -v '^ *15'`
		- With a for loop
			- `for file in *; do ; done` 		
1. Programs and files 2 (75 mins)
	- The environment and PATH variable
		- directories with executable programs that can be run from the command line (example: `cat` is a program that is available in your $PATH)
	- Setting a variable
		- `export name='command'` (at command line or in *~/.bashrc*)
	- Aliasing and *.bashrc*
		- `source ~/.bashrc`
		- temporary aliases: `alias ll="ls -l"`
		- permanent aliases: *~/.bashrc*
	- Navigating your file system and programs (now that you know what you're doing)
		- `tree` (use `brew install tree` for MacOS) or `tree.com //f` on Windows 
		- `help`
		- `man`, `info`, and `apropos`
		- `which` and `type`
			- run `man which`
			- run `which man` 
		- `whereis`
			- if you've ever used Python, this is a command you need 
		- using `find`
			- `find . -name shakespeare-sonnets.txt -print`
	- Compression and archiving
		- `zip` (`zip -r archivename *.txt`) and `unzip` (`-t` is test, `-l` is list) 
		- `gzip` and `gunzip` 
		- `tar` (`tar -xvf filename.tar`); `unrar`
	- Activity: compress your new sonnet files 
		- make a new archive
		- list and test your new archive
		- copy it to a new directory (make one!) and unzip it there 

## Friday 

### Morning (3 hours - 15 min break)

#### Web technologies

1. HTML/CSS

	- Hypertext Markup Language (HTML) is a controlled XML vocabulary (meaning it has angle brackets and a strict schema) that is used to hold and organize content for the web
	- Cascading Style Sheets (CSS) is a styling language for HTML. One can specify colors, fonts, spacing, etc using CSS
	- JavaScript is a client-side programming language that allows for interaction and dynamic content totally produced within the user's browser, rather than on the server.

1. Activity: Using Developer tools in Chrome's “Inspect”	
1. Installing and using PanDoc

	- `brew install pandoc`
	- `choco install pandoc`
	- Activity: convert `outline.md` to HTML

1. Downloading files from the command line
	- `curl` is a filter that outputs to stdout (this means you can pipeline it) and `wget` (creates something, is recursive)
		- `wget http://dh.obdurodon.org/bartleby.txt`
		- `curl -s http://dh.obdurodon.org/bartleby.txt | wc`  

### Afternoon (1.5 hours - no break)

#### Structured review

- Activity: Preparing *Ulysses* as plain text
	1. change directories into *data/ulysses_practice*
	2. `ls` around and see what's up!

____

## Miscellaneous information

* Links to [external resources](resources.md)
* Contact your instructors
	* David: djbpitt at gmail.com
	* Gabi: gabakeane at gmail.com





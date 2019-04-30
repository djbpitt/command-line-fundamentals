# Course Outline
## Order of topics covered

### Tuesday
#### Morning (2.5 hours - 10 min break)
1. Introductions (20 mins)

1. Software installation (40 mins)
	- Git
		- MacOS: type `git` in the terminal and accept installation
		- Windows: [Git bash](https://www.techoism.com/how-to-install-git-bash-on-windows/)
	- [BBEdit](https://www.barebones.com/products/bbedit/) (MacOS) and [Notepad++](https://notepad-plus-plus.org/) (Windows)
	- [Homebrew](https://brew.sh/) (MacOS only)
		- Then: `brew install dos2unix`
	- [MacDown](https://macdown.uranusjr.com) (MacOS) and [Ghostwriter](https://wereturtle.github.io/ghostwriter/) (Windows)
	- Clone our repository in *Desktop/*

1. Getting to know your operating system (40 mins)

	- The hierarchical file system
		- Don’t put everything in *Documents/* or in *Desktop/*
	- File names 
		- Letters (case), numbers, and `.-_` (**no spaces and no other punctuation**)
		- File name extensions
		- “Final” should never appear in your file names [and here is why](https://a.disquscdn.com/uploads/mediaembed/images/1707/4842/original.jpg)
	- Show file name extensions and hidden files
		- MacOS file extensions: Finder > Preferences > Advanced > “Show all file extensions”
		- MacOS hidden files: `Ctrl + Shift + .`
		- Windows: File Explorer > View > Select “Hidden items” and “File name extensions” 
	- File permissions and ownership
		- MacOS: Select file in finder, then `Cmd + i` (or right-click and “Get info”)
		- Windows: Select file in Explorer, right click and “Properties”)
	- Danger zones: there is no `undelete`
	- Case sensitive vs case-preserving
1. Activity: Clean up your mess (40 mins)

#### Afternoon (3 hours - 15 min break)

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
	- [The Git workflow](gitworkflow.png): `status`; `add`, `commit`, `push`; `pull`
		- Check status of local repo: `git status`
		- Integrate local work into repo
			- `git add <filename>`
			- `git rm <filename>` (not just `rm <filename>`)
			- `git commit -m "this is my commit message"`
			- `git push`
		- Guidelines
			- [Pull and push frequently](in_case_of_fire.png)
			- Git adds *files*
			- Git commits sets of line-level *changes* in multiple files (not files)
			- Empty directories cannot be committed (add a placeholder file if necessary)
			- Commits should be granular and conherent (don’t use `git add .` or `git commit -a -m "this is my commit message"` unless you know that your changes meet this requirement)
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

### Wednesday
#### Morning (3 hours - 15 min break)
1. Programs and files 1 (45 mins)
	- `file`
	- What are files? What are programs? What are directories?
		- They're *all* files, that's why `file` works for everything
	- Character sets and file formats
		- ASCII vs. UTF-8
			- *rendering errors can occur if you're using the wrong character set*
		- Conversion in text editor
			- Notepad++: “Encoding”
			- BBEdit: Bottom status bar
		- Internationalization conversion: `iconv -l`
		- Activity: Conversion on command line  
	- Operating system conventions
		- EOL/EOF
		- `dos2unix`
		- Back slashes and forward slashes (only for cmd.exe and Powershell)

1. Regex (120 mins)
	- Flavors
		- `egrep`	 
	- syntax of regex expressions
	- practicing in an online tool
	

#### Afternoon (3 hours - 15 min break)
1. More Regex (75 mins)
	- `grep` and `egrep`
1. Command line 2 (90 mins)
	- `whoami`
	- `clear`
	- `history`
	- recall and editing
	- tab completion
	- `cp`
	- `mv`
	- `rm`
	- `less`
	- `mkdir`
	- `rmdir`
	
### Thursday
#### Morning (3 hours - 15 min break)
1. Command line 2 continued (165 mins)
	- comparing wildcards/file name globbing with regex
	- redirection
	- filters (piping)
	- `cat`
	- `wc`
	- `head`
	- `tail`
	- `sort`
	- `uniq`
	- keyboard shortcuts

#### Afternoon (3 hours - 15 min break)
1. Programs and files 2 (165 mins)
	- for loops
	- the environment and PATH variable
	- finding commands and files
	- aliasing and .bashrc
	- `help`
	- `which`
	- `whereis`
	- `find`
	- `type`
	- `diff` and `wdiff`

### Friday 
#### Morning (3 hours - 15 min break)
##### Web technologies
- HTML/CSS
- JavaScript
- PanDoc
- How the Internet works

#### Afternoon (1.5 hours - no break)
- structured review
- exam?

## Admin information

[External resources](resources.md)

### Contact

* djbpitt at gmail.com
* gabakeane at gmail.com





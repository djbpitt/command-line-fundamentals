# Configuring git

## Create an account on GitHub

Create a free individual account by following the instructions at <https://github.com/pricing>.

## Install command-line git tools

Follow the instructions at <https://www.atlassian.com/git/tutorials/install-git> (first options for each operating system)

## Initialize your local git settings

Open a terminal and enter the following commands, replacing John Doe’s information with the name and email address that you used when you configured your account on GitHub. You only have to do this once (on each computer that you use). 

```bash
git config --global user.name "John Doe"
git config --global user.email johndoe@example.com
git config --global core.editor "nano"
```	
# Git

Git is a version control system, a simple command line tool for keeping a history on the state of your source code projects.

## Getting Started

### Installation
-------------------------

For Ubuntu/ Debian users:

<pre class="brush: shell">
sudo apt-get install git
</pre>

For Mac OS X users who use homebrew:

<pre class="brush: shell">
brew install git
</pre>

For Windows users, download and install <a href="http://railsinstaller.org/" target="_blank">Rails Installer</a> which comes with mysisgit

### Configuration
-------------------------

<pre class="brush: shell">
git config --global user.email "me@here.com"
git config --global user.name "Your Name"
</pre>

### Recommended Guides for Git Beginners
-------------------------

### <a href ="http://rogerdudler.github.com/git-guide/" target="_blank"> git - the simple guide (no deep shit) </a>

### <a href ="http://gitimmersion.com/" target="_blank"> Git immersion </a>


### Defining a Gitignore
-------------------------

The .gitignore file contains files or folders you want to ignore for a project. These will not be included on the list of files and folders to be tracked for changes and will not be commited. Developers usually ignore temporary files created or probably configuration files.


### Defining a Global Gitignore
-------------------------------

The .global_gitgnore resides on your home directory. If you use Linux or OS X, the file is ~/.global_gitignore

#### Common files and folders to ignore for a Ruby on Rails project

<pre class="brush: ruby">
*.rbc
*.sassc
.sass-cache
capybara-*.html
.rspec
/.bundle
/vendor/bundle
/log/*
/tmp/*
/db/*.sqlite3
/public/system/*
/coverage/
/spec/tmp/*
**.orig
rerun.txt
pickle-email-*.html
</pre>

For OS X users, we ignore the following files:

<pre class="brush: ruby">
.DS_Store
.AppleDouble
.LSOverride
Icon


# Thumbnails
._*

# Files that might appear on external disk
.Spotlight-V100
.Trashes
</pre>

Fore more files to ignore, check the <a href="https://github.com/github/gitignore/tree/master/Global" target="_blank">gitignore</a> list updated by several developers worldwide.

### Creating a new git repository
-------------------------------

<pre class="brush: shell">
mkdir something
cd something
git init
</pre>


### Git Hosting
-------------------------------

### <a href ="http://assembla.com/" target="_blank"> Assembla </a>

### <a href ="https://github.com/" target="_blank"> Github </a>


### Ruby on Rails Hosting
-------------------------------

### <a href ="https://heroku.com/" target="_blank"> Heroku </a>


### Setup Git on a Shared Hosting Server
-------------------------------

You need an SSH user or a user who can log in to your account via a terminal.

<pre class="brush: shell">
ssh user@host

mkdir project
cd project
git --bare init

</pre>

Your git repository link would look like:


<pre>
user@host:~/project
</pre>

### Connect repository to a remote server
-------------------------------

<pre class="brush: shell">
git remote add origin path/to/remote/repo.git
</pre>

### Checking for changes
-------------------------------

<pre class="brush: shell">
git status
</pre>

### Make sure you can edit commit messages with your editor
-------------------------------

If you are using MacVim:

<pre class="brush: shell">
git config --global core.editor "mvim"
</pre>

If you are using Sublime Text 2 on a Mac:

<pre>
Install <a href="http://www.sublimetext.com/docs/2/osx_command_line.html" target="_blank">subl</a>
git config --global core.editor "subl -n -w"
</pre>

### Determine the current branch
-------------------------------

<pre class="brush: shell">
git branch
</pre>

### Checkout a branch
-------------------------------

<pre class="brush: shell">
git checkout branch-name
</pre>

If you just to want to add a specific file:

<pre class="brush: shell">
git add filename
</pre>


### Adding up changes
-------------------------------

If you want to add modified files, new files and remove deleted files:

<pre class="brush: shell">
git add -A
</pre>

If you just to want to add a specific file:

<pre class="brush: shell">
git add filename
</pre>


### Commit message
-------------------------------
<pre class="brush: shell">
git commit -m "message"

</pre>

or

<pre class="brush: ruby">
#opens up an editor
git commit -a
</pre>


### Updating the remote repository
-------------------------------

<pre class="brush: shell">
git push origin master
</pre>


### Retrieving changes from the remote repository
-------------------------------

<pre class="brush: shell">
git pull origin master
</pre>


## Other Resources

### <a href ="http://git-scm.com/book" target="_blank"> Pro Git: A free definitive book written by Scott Chacon</a>
### <a href ="https://github.com/progit/progit" target="_blank"> Pro Git contents updated the community</a>
### <a href ="http://railscasts.com/episodes/96-git-on-rails" target="_blank"> Git on Rails </a>


## Contributors to this guide

<a href ="https://blog.bridgeutopiaweb.com" target="_blank"> Katherine G. Pe</a>, software developer.


## Contributing

<a href ="https://github.com/railsgirls-ph/rails-girls-manila-2012" target="_blank"> Fork the project and create a pull request if you have some changes</a>

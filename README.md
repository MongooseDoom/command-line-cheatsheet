# Mac

## Basics

<table style="width: 100%">
    <tr>
        <td>cd</td>
        <td>change directory</td>
    </tr>
    <tr>
        <td>ls</td>
        <td>list files in directory</td>
    </tr>
    <tr>
        <td>ls -l</td>
        <td>list files in directory with more info</td>
    </tr>
    <tr>
        <td>touch [filename]</td>
        <td>create new file</td>
    </tr>
    <tr>
        <td>mkdir [directory]</td>
        <td>create new directory</td>
    </tr>
    <tr>
        <td>ln -s /path/to/original /path/to/symlink</td>
        <td>create a symlink</td>
    </tr>
    <tr>
        <td>pwd</td>
        <td>path of the current directory (present working directory)</td>
    </tr>
    <tr>
        <td>rm [filename]</td>
        <td>remove file</td>
    </tr>
    <tr>
        <td>cp [file] [new file]</td>
        <td>copy file</td>
    </tr>
    <tr>
        <td>mv [file] [new filename]</td>
        <td>move/rename file</td>
    </tr>
    <tr>
        <td>open .</td>
        <td>open current directory in finder</td>
    </tr>
    <tr>
        <td>open [file]</td>
        <td>open file in default application</td>
    </tr>
    <tr>
        <td>open -a "Application Name" [filename]</td>
        <td>open file with specific application</td>
    </tr>
    <tr>
        <td>!!</td>
        <td>repeats last command Example: <code>sudo !!</code></td>
    </tr>
    <tr>
        <td>ctrl + c</td>
        <td>kill whatever you're running</td>
    </tr>
    <tr>
        <td>ctrl + w</td>
        <td>delete last word</td>
    </tr>
    <tr>
        <td>ctrl + u</td>
        <td>delete to start of line</td>
    </tr>
    <tr>
        <td>ctrl + a</td>
        <td>move cursor to start of line</td>
    </tr>
    <tr>
        <td>ctrl + e</td>
        <td>move cursor to end of line</td>
    </tr>
    <tr>
        <td>cmd + k</td>
        <td>clear window</td>
    </tr>
</table>

## Tricks

Drag and drop directory into terminal to get path

The tab key is your friend. When you're entering a directory you can use it to autocomplete what you've already typed in or to show you a list of what's in the directory.

## Aliases
An alias is a shortcut for terminal commands

### File to add aliases to:
~/.bash_profile

### Examples:
<pre><code>alias htdocs="cd /Applications/MAMP/htdocs"
alias prh="cd /Applications/MAMP/htdocs/princeresortshawaii_com/branches/redesign-2015"

alias edit_hosts='st /etc/hosts'
alias edit_vhosts='st /Applications/XAMPP/xamppfiles/etc/extra/httpd-vhosts.conf'
alias edit_aliases="st /Users/jkeiser/.oh-my-zsh/custom/my_aliases.zsh"

alias xampp="sudo /Applications/XAMPP/xamppfiles/xampp"</code></pre>

In the example, entering <code>htdocs</code> would be the same as <code>cd /Applications/MAMP/htdocs</code>


## SVN
http://www.linuxfromscratch.org/blfs/edguide/chapter03.html

<table>
    <tr>
        <td>svn checkout [url]</td>
        <td>check out a repository</td>
    </tr>
    <tr>
        <td>svn status</td>
        <td>shows locally modified items</td>
    </tr>
    <tr>
        <td>svn add [filename]</td>
        <td>when you create a new file or directory, you need to let svn know about it by using the add command</td>
    </tr>
    <tr>
        <td>svn update<br>svn up</td>
        <td>syncs local with SVN server</td>
    </tr>
    <tr>
        <td>svn commit -m "Commit Message"</td>
        <td>sends your changed files, added files, and deleted files to the SVN server with a commit message</td>
    </tr>
    <tr>
        <td>svn log</td>
        <td>display commit log messages</td>
    </tr>
    <tr>
        <td>svn log -r {2015-05-01}:{2015-05-31}</td>
        <td>display commit log messages between two dates</td>
    </tr>
</table>

## Git
http://rogerdudler.github.io/git-guide/

<table>
    <tr>
        <td>git clone [url]</td>
        <td>create a working copy of a repository. similar to svn checkout</td>
    </tr>
    <tr>
        <td>git status</td>
        <td>shows locally modified items</td>
    </tr>
    <tr>
        <td>git add [filename]</td>
        <td>include files in what will be committed</td>
    </tr>
    <tr>
        <td>git add *</td>
        <td>add all files to be committed</td>
    </tr>
    <tr>
        <td>git commit -m "Commit Message"</td>
        <td>record changes to repository. does not commit to remote</td>
    </tr>
    <tr>
        <td>git pull</td>
        <td>pulls changes from remote repository</td>
    </tr>
    <tr>
        <td>git push</td>
        <td>pushes changes to remote repository</td>
    </tr>
    <tr>
        <td>git stash save</td>
        <td>save your local modifications</td>
    </tr>
    <tr>
        <td>git stash apply</td>
        <td>apply stash modifications on top of the current working tree state</td>
    </tr>
    <tr>
        <td>git checkout -b [branch name]</td>
        <td>create a new branch and switch to it</td>
    </tr>
    <tr>
        <td>git checkout [branch name]</td>
        <td>switch to different branch</td>
    </tr>
</table>

## Vim
Vim is a text editor within terminal. You'll sometimes find yourself in vim when using terminal so it's important to know a few things about it.

Vim has four modes: Normal, Insert, Visual, and Command.

#### Normal
Esc key

Vim starts in normal mode. You can navigate the file and start editing.

#### Insert
<code>a, A, i, I, o, and O</code>

In this mode, you can edit the file like you would in a normal text editor. **To exit Insert mode, hit Esc to return to Normal mode.**

#### Visual
<code>v, V, and Ctrl-v</code>

In Visual mode, you can select text.

#### Command
<code>:</code>

Anytime you use the <code>:</code> command in Normal mode, you will enter into Command mode. In Command mode, you can perform complex editing functions, file actions, or shell actions.

#### How to close Vim
Keep calm and use these:

In Normal mode, you can type <code>ZZ</code> to save everything and exit. If you're in Insert mode, remember to hit Esc to return to Normal mode first.

In Command mode, you can use these to save and quit:

<code>:w</code> to save  
<code>:wq</code> to save and quit  
<code>:q</code> to quit without saving  

add <code>!</code> at the end to force the operation to write without questions

Example: <code>:wq!</code>

## MySQL

#### How to login to MySQL
If you're using XAMPP:<br/>
<code>/Applications/xampp/xamppfiles/bin/mysql -uroot -p</code>

#### Create/Delete
<b>Create:</b><br/>
<code>CREATE DATABASE [database name];</code><br/>
<b>Delete:</b><br/>
<code>DROP DATABASE [database name];</code><br/>

#### Import/Export

<b>Export:</b><br/>
<b>Import:</b><br/>
<code>USE [database name];</code><br/>
<code>source [path to sql file];</code><br/>

#### How to exit
<code>exit;</code>

## Extra

### iTerm
http://iterm2.com/

iTerm is a replacement for Terminal. It has a lot of nice features but the one I use the most is the hotkey window.

###  Oh-My-Zsh
http://ohmyz.sh/

I use Oh-My-Zsh for its better tab completion, themes, and plugins.

Features:

- <code>take [directory name]</code> Same as mkdir [directory name]; cd [directory name];
- Type first part of command and use arrows keys to navigate history
- ctrl + r allows you to search through recent commands

Plugins:

- [z](https://github.com/robbyrussell/oh-my-zsh/wiki/Plugins-Overview#fs-jumping) - Learns what directories you frequently use
- [sudo](https://github.com/robbyrussell/oh-my-zsh/wiki/Plugins#sudo) - Press escape twice to add sudo to beginning of line


### Trash
https://github.com/sindresorhus/trash
Alternative to using <code>rm</code> that moves files to the trash

## Resources
- [Command Line Power User](http://commandlinepoweruser.com/)
- [The Command Line Crash Course](http://cli.learncodethehardway.org/)


#Windows

## Basics

Commands for PowerShell

<table>
    <tr>
        <td>cd</td>
        <td>change directory</td>
    </tr>
    <tr>
        <td>ls</td>
        <td>list files in directory</td>
    </tr>
    <tr>
        <td>New-Item [filename] -ItemType file</td>
        <td>create new file</td>
    </tr>
    <tr>
        <td>mkdir</td>
        <td>create new directory</td>
    </tr>
    <tr>
        <td>pwd</td>
        <td>path of the current directory</td>
    </tr>
    <tr>
        <td>del [filename]</td>
        <td>remove file</td>
    </tr>
    <tr>
        <td>cp [file] [new file]</td>
        <td>copy file</td>
    </tr>
    <tr>
        <td>mv [file] [new filename]</td>
        <td>move/rename file</td>
    </tr>
    <tr>
        <td>explorer .</td>
        <td>open current directory in finder</td>
    </tr>
</table>

## Extra
Drag and drop into PowerShell to get path.

The tab key is your friend. When you're entering a directory you can use it to autocomplete what you've already typed in or to show you a list of what's in the directory.

## Extra
### Cygwin
https://cygwin.com/

Cygwin is a Windows program that replaces the standard shell with one that closely resembles a Unix machine. There are a lot of alternatives to cygwin so I suggest finding one that you like.

### Gow
https://github.com/bmatzelle/gow/wiki

A light weight alternative to Cygwin.

### cmder
http://gooseberrycreative.com/cmder/

Console emulator for Windows!

---
layout: default
---

### Description

| KIK-LG219 | 5 cr |
| Command line tools for linguists | fall 2020 |

The course "command line tools for linguists" is an introductory course to command line environment and its tools. It is aimed at bachelor students in languages who are interested in language technology. No previous knowlegde of command line tools is needed. Course work consists of weekly assignments and a final project. The course format is an online course.

### Week 1: Setting Up the Command Line Environment & Command Line Basics

- setting up the command line environment on your personal computer or Helsinki University account
- introduction to the basic "commands"
- introduction to text editors and emacs basics
- the difference between text files and binary files

I learned how to set up a command line environment on my personal (Windows) computer by running Ubuntu on VirtualBox. I learned the basic commands: cp, wget, ls, mkdir, mv, echo, touch, cat, rm, less, cd.

Example of one learned command: ```mkdir KIK-LG219``` creates a directory called KIK-LG219

### Week 2: Navigating a Unix system

- the UNIX file system
- handling directories
- users, groups and file permissions in UNIX
- initializing, monitoring and killing processes
- working with remote servers

I learned how to locate PIDs and how to kill a process by using the command ```kill```. I also learned how form a remote connection to a server.

### Week 3: Basic Corpus Processing

- what are different encoding systems (ASCII, Latin-1, utf-8)
- converting text files to a different encoding
- basic text processing commands
- redirecting standard streams
- introduction to RegEx

I learned how to convert Windows text files to UNIX encoding format using command ```dos2unix```. I also learned basic regular expressions; for example, this is how you find how many words start with lowercase "e" in a text file:

```egrep "^e" file.txt | wc -l```

egrep means we're using regex, ^ is the start of the line, wc -l counts the lines

### Week 4: Advanced Corpus Processing

- chaining commands using pipes
- searching via grep command
- editing files with sed
- using RegEx with sed
- advanced regular expressions
- generating a frequency list, a sentence per line format and transforming a text file into a list of n-grams

I learned how to create a frequency list and a sentence per line text file. I also learned how to make a list of n-grams.

A freq list can be generated with the following code:

```cat [filename] | tr -s '\n\r\t ' '\n' | tr -dc "[:alnum:]\n'" | sort | uniq -c | sort -nr -> [filename.freq]```

### Week 5: Scripting and Configuration Files

- writing simple scripts
- creating a .bashrc file and using it to create your own pleasant working environment
- UNIX environment variables

This week was very difficult for me, I still don't understand how scripts work even though I tried my best.

The only thing I learned this week was that if you can't run a script because you are lacking permissions, using a command ```chmod u+x myscript.sh``` grants execute permissions to all users.

### Week 6: Installing and Running Programs

- giving commands as a root user
- installing software using apt-get or brew
- installing python packages with pip
- creating a python virtual environment
- writing a Makefile and running it

I learned how to become a root user to install programs using the command ```sudo```. I also learned to install python modules with pip. Writing a Makefile was a bit more difficult but I managed to do it.

A code

```animals.gz: lion fish
       gzip $@ $^```

will make a gzip-archive animals.gz that contains both files "lion" and "fish"

### Week 7: Version Control

- version control using Git and Github
- setting up your Git repository
- committing changes
- introduction to Git branches

I learned about GitHub and what it's used for. I learned to set up a repositiory and how to commit and push changes to Git using commands git add -A, git commit -m and git push. When using git commit -m, you need to add a message what changes you are going to push to git, for example:

```git commit -m "Edited cmdline_course.md"```

I also learned how to make branches (git branch [branch name]) and switch between them (git checkout -b [branch name]) as well as how to merge branches (git merge [branch name]).

### Final project

The final project of this course was to build this website and publish it on GitHub pages. I learned how to create a template repositiory and how to display webpage while editing by using ```bundle exec jekyll serve```. Now I know how to build a GitHub webpage.

![kuva](https://thumbs.dreamstime.com/z/mature-man-computer-smiling-20855484.jpg)
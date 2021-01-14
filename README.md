<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="#table-of-contents">
    <img src="https://raw.githubusercontent.com/johnunar/cheatsheets/master/images/command.png?token=AHRYNKKSZSV5FRU2LAJLW4DABGFEE" alt="Logo" width="150">
  </a>

  <h3 align="center">Cheatsheet</h3>

  <p align="center">
  All-time favorites
    <br />
    <br />
    <a href="https://github.com/johnunar/cheatsheets/issues">Report Bug</a>
    ·
    <a href="https://github.com/johnunar/cheatsheets/issues">Request Feature</a>
  </p>
</p>



<!-- TABLE OF CONTENTS -->
## Table of Contents

* [About the Project](#about-the-project)
* [Command line](#command-line)
* [PostgreSQL](#postgresql)
* [Conda & Pip](#conda--pip)
* [Python](#python)
* [Django](#django)
* [Heroku](#heroku)
* [Git](#git)
* [Roadmap](#roadmap)
* [Contact](#contact)


<!-- ABOUT THE PROJECT -->
## About The Project

Useful commands and tips all at one place. Created as a personal open-source project, feel free to collaborate!

<!-- Command line -->
## Command line

##### Check what process is running on a port 8000
MacOS
```shell script
lsof -i tcp:8000
```
Linux
```shell script
netstat -vanp tcp | grep 8000
```

<!-- PostgreSQL -->
## PostgreSQL
MacOS
```shell script
pip install psycopg2-binary
```
Other
```shell script
pip install psycopg2
```

<!-- Conda -->
## Conda & Pip
#### [Conda docs](https://docs.conda.io/en/latest/)

##### Create a new environment named py35, install Python 3.5
```shell script
conda create --name py35 python=3.5
```

##### Activate the new environment to use it
```shell script
conda activate py35
```

##### Leave the active environment
```shell script
conda deactivate
```

##### Get a list of all my environments, active environment is shown with *
```shell script
conda env list
```

##### Install a new package
Conda (fewer packages)
```shell script
conda install <package-name>
```
Pip
```shell script
pip install <package-name>
```

##### Create or update requirements.txt file
```shell script
pip freeze > requirements.txt
```

<!-- Python -->
## Python
#### [Python docs](https://docs.python.org/)


<!-- Django -->
## Django
#### [Django docs](https://docs.djangoproject.com/)

##### Convert \\n to \<br/> in templates
```html
{{my_field.label|linebreaks}} 
```

<!-- Heroku -->
## Heroku
#### [Heroku docs](https://devcenter.heroku.com/)

##### Copy database to a new app
```shell script
heroku pg:backups:capture --app sushi # sushi is name of source app
heroku pg:backups:restore sushi::b001 --app sushi-2 # b001 - name of backup, sushi-2 - dest. App
```

##### Clone entire app
```shell script
heroku plugins:install heroku-fork
heroku fork --from my-production-app --to my-development-app
```

<!-- Git -->
## Git
#### [Git docs](https://git-scm.com/doc)

### Basics

##### Create empty git repo <optional:in specified directory>
```shell script
git init <directory>
```

##### Clone repo located at <repo> onto local machine
```shell script
git clone <repo>
```

##### Stage all changes in <directory/file> for the next commit
```shell script
git add <directory/file>
```

##### Commit the staged snapshot with message
```shell script
git commit -m "<message>"
```

##### List which files are staged, unstaged, and untracked.
```shell script
git status
```

### Config

##### Define author details to be used for all commits in current repo (or globally)
```shell script
git config (--global) user.name <name>
git config (--global) user.email <email>
```

##### Create alias for a Git command.
###### E.g. alias.glog “log --graph --oneline” will set ”git glog” equivalent to ”git log --graph --oneline.
```shell script
git config --global alias.<alias-name> <git-command>
```

##### Open the global configuration file in a text editor for manual editing.
```shell script
git config --global --edit
```

### F-ups

When something does not go by the plan. **Proceed at your own risk.**

##### Remove directory from git ONLY
```shell script
git rm -r --cached <directory>
```

<!-- ROADMAP -->
## Roadmap

<!-- CONTACT -->
## Contact

Jan Unar
* [unar.dev](https://unar.dev/)
* [@JohnnyUnar](https://twitter.com/JohnnyUnar)
* [johnunar@gmail.com](mailto:johnunar@gmail.com)

Project Link: [https://github.com/johnunar/cheatsheets](https://github.com/johnunar/cheatsheets)
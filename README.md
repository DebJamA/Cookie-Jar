# Development Environment  
  
#### Installations and upgrades on computer  
  
**1.** macOS Ventura 13.4.1  
  
**2.** Download [latest version of Python](https://www.python.org/downloads/) (for Mac) and follow prompts of Installer:  
`% python3 --version`  
> Output: Python 3.11.5  
  
**3.** Upgrade pip:  
`% pip3 install --upgrade pip`  
`% pip3 -V`  
> Output: pip 23.2.1  
  
**4.** Install [latest version of pipenv](https://pypi.org/project/pipenv/) - a Python virtualenv management tool:  
`% pip3 uninstall pipenv`  
`% pip3 install pipenv`  
`% python3 -m pipenv --version`  
> Output: pipenv, version 2023.9.1  
  
**5.** Ensure [current version](https://git-scm.com/downloads) of [Git is installed](https://git-scm.com/download/mac) and configured on Mac (using [Homebrew](https://brew.sh/)):  
`% brew update && brew upgrade`  
`% git --version`  
> Output: git version 2.42.0 
  
**6.** Ensure [current version of SQLite3](https://ports.macports.org/port/sqlite3/) is installed on Mac:  
`% sqlite3 --version`  
> Output: 3.43.0 2023-08-24  
  
#### Create new project in GitHub: Cookie Jar  
  
**1.** Log in to your GitHub account [or create a GitHub account](https://github.com/signup?ref_cta=Sign+up&ref_loc=header+logged+out&ref_page=%2F&source=header-home)    
  
**2.** Create GitHub repo  
	a. New repository  
	b. Repository name: ***Cookie Jar***  
	c. Choose repository visibility: Public  
	d. Do not initialize the new repository with README, gitignore, or license files  
	e. Create repository  
	f. Keep this page open to later copy the remote repository URL  
  
**3.** Ensure [PyCharm Community Edition](https://www.jetbrains.com/pycharm/download/?section=mac) (for Mac) is installed  
    
**4.** Open PyCharm to [Create a Python project](https://www.jetbrains.com/help/pycharm/pipenv.html):  
***Cookie Jar***  
a. Configure Python interpreter:  
- new environment **pipenv**  
- make sure Base interpreter is **Python 3.11**  
  
b. Launch pipenv subshell in the venv (cookieJar):  
	`(cookieJar)% pipenv shell`  
  
**5.** Initialize git repository  
a. `(cookieJar)% git init`  
> Output: Initialized empty Git repository in /.../.../.../PycharmProjects/cookieJar/.git/  
   
b. Set and verify new remote  
	`(cookieJar)% git remote add cookiejar https://github.com/DebJamA/Cookie-Jar.git`  
	`(cookieJar)% git remote -v`  
> Output:  
> cookiejar https://github.com/DebJamA/Cookie-Jar.git (fetch)
> cookiejar https://github.com/DebJamA/Cookie-Jar.git (push)
  
c. Create a new branch:  
`(cookieJar)% git checkout -b cookieJar-1`  
> Output: Switched to a new branch 'cookieJar-1'  
  
**6.** Create `.gitignore` file in root directory  
> Copy/paste from [mooowooo repo](https://gist.github.com/MOOOWOOO/3cf91616c9f3bbc3d1339adfc707b08a)  
  
**7.** Create `README.md` in root directory  
  
#### Push to GitHub:  
 
`(cookieJar)% git status`  
```
Output:  
On branch cookieJar-1

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .gitignore
        Pipfile
        README.md

nothing added to commit but untracked files present (use "git add" to track)
```  
  
`(cookieJar)% git add .`  
`(cookieJar)% git status` 
```
Output:  
On branch cookieJar-1

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   .gitignore
        new file:   Pipfile
        new file:   README.md
```  
  
`(cookieJar)% git commit -m "set up dev env"`  
`(cookieJar)% git push cookiejar cookieJar-1`  
```  
Output:  
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (5/5), 3.39 KiB | 1.69 MiB/s, done.
Total 5 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/DebJamA/Cookie-Jar.git
 * [new branch]      cookieJar-1 -> cookieJar-1
```  
  
---  

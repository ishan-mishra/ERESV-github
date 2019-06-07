*'In my experience with teaching Github, the syntax is pretty easy to pick up but the terminology and work flow is the most confusing.'* - Natasha Batalha

### List of resources:

1. Git Started with Github (Udemy): https://www.udemy.com/git-started-with-github/
2. Official Github guide: https://guides.github.com/activities/hello-world/ 
3. GitHub Ultimate (Udemy): https://www.udemy.com/github-ultimate/?couponCode=FC_STUDENTS
4. https://rogerdudler.github.io/git-guide/
5. http://marklodato.github.io/visual-git-guide/index-en.html

### Helful notes for GitHub website content:

- Talk about both user/organization pages (separate repository  & URL is `<your user-name>.github.io`) and individual project pages (same repository as the project & URL is `<your user-name>.github.io/<your repository’s name>`


### Helpful notes for introductory GitHub content:

1. What is Git? 
- Distributed source control system
- Used for collaborations and version control

2. Core concepts
- Repository contains files, history, config managed by Git. 
- Three states of Git:
    1. *Working directory*
    2. *Staging area*: pre-commit holding area
    3. *Commit*: Git repository (history)
- Remote repository (GitHub): can be considered as a fourth state (a website that hosts `.git` repositories) 
- Master branch: branches are like timelines that contain changes/commits; default branch is called Master branch. 

3. Command line or GUI? 
Git was originally designed for command line; new features make it to command line first; online assistance mostly for command line; with command line we get one set of commands mostly independent of platform

4. Git installation
- Windows: https://git-for-windows.github.io
  - Open Git-Bash; type `git version` to verify installation
- MacOS: Open command line and type `git version`
  - If not installed, press `Install` in the prompt-window

5. Basic Git workflow:
- Setup a GitHub account
- Setup a project folder
- Configure global username and email: 
  - `git config --global user.name “Abe Lincoln”`
  - `git config --global user.email “mrabe@git.training”`
  - Check with `git config --global --list`
- Copy repository from GitHub to your local computer (cloning)
  - `git clone “url of the repository”`
  - Go into the repository directory and type `git status`; It should tell you that you are on branch `master`; `origin/master` refers to the repository on GitHub
  - `git status` tells us about any changes between the working directory, staging area, local repository and the remote GitHub repository
- First commit:
  - Create a simple text file: `echo “some random text” >> start.txt`
  - `cat start.txt` to display content of file
  - `git status` would now show one untracked file. (*File still in working area*)
  - `git add start.txt` will add the file to the staging area. Git refers to this as `changes to be committed` (*File now in staging area*)
  - *Note*: To add all the untracked files to the staging area: `git add .`
  - `git commit -m “comment for the commit”` will add the file to the local repository. (*File now moved to local repository*)
- To put the file on Github : 
  - `git push origin master` 
  - `origin` refers to the GitHub repository
  - `master` refers to the branch we want to push to
  - *File is now also on the remote Github repository*

6. Alternate way to start a new local git repository
  - `git init fresh-project`
  - `cd fresh-project`
  - `ls -al` tells command line to see the .git folder
  - `cd .git` to check out all the components of the git folder
  - `git status` will tell us that we are on the master branch

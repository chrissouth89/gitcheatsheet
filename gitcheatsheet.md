# Git Basics

**MAIN RESOURCES**

- [Article Explaining What is Git](https://tuts.alexmercedcoder.com/2021/1/guidetogit/)
- [Video Intro to Git](https://www.youtube.com/watch?v=L4zbgo7KFoA&list=PLY6oTPmKnKbYjGEm9nLowExbgkI-epIgg&index=7&t=9s)
- [Video working with git Remotes](https://www.youtube.com/watch?v=TOsVVxXdtu8&list=PLY6oTPmKnKbYjGEm9nLowExbgkI-epIgg&index=9&t=2s)
- [Setting up SSH on Git](https://www.youtube.com/watch?v=6u84sACs0v0&list=PLY6oTPmKnKbYjGEm9nLowExbgkI-epIgg&index=8)

Early on you will using git to get code (pull) from a remote repository (on github), writing your own code, tracking it with git, and moving (push) the code from your computer (local version) to github.

When using git locally (on your computer), you have been running the commands in Terminal (Command line).

A git command has a minimum of 1 argument.

Git commands are always executed by first typing `git`

The first argument is the command (or verb), like

- `git init` (initialize a new git repository)
- `git push` (send the code to a remote location)

The second(+) argument gives the first argument context (when needed)

- `git add .` (add all files in this directory)
- `git pull origin master` (get all files from the url that has an alias of `origin`, from the branch `master`)

Lastly, flags can be added

- `git remote -v` (git show remote(s) and be verbose(give more detail))

Here is a table of our commonly used git commands that we've used in this course so far:

| git | Argument | Flag(s)/Additional arguments |                                                                  Description                                                                   |
| :-: | :------: | :--------------------------: | :--------------------------------------------------------------------------------------------------------------------------------------------: |
| git |   init   |                              |                                                          Initializes a new repository                                                          |
| git |   add    |       `.` or filename        |                             Takes untracked files and adds them to the staging area so that they can be committed                              |
| git |  commit  |      -m 'some message'       |                             Takes a snapshot of files in the staging area/ saves this version of them as a commit                              |
| git |  remote  |              -v              | Shows the remote repositories associated with the local repository. Most repositories have an alias for their urls like `origin` or `upstream` |
| git |   pull   |       upstream master        |                                   Gets files from a url with an alias of `upstream` from its branch `master`                                   |
| git |   push   |          origin dev          |                                       Sends files to a url with an alias of `origin` to its branch `dev`                                       |
| git |   log    |          --oneline           |                              Shows a log of commits of a repo (--oneline shows a truncated message)_`q` to exit_                               |
| git |  status  |                              |                                        Shows the state of files in a repo (untracked, modified, staged)                                        |

Note: `fork` is not on this list because `fork` is not a git command; it is github-specific for copying a repository on github to a new location on github.

### Generating a new GitHub repo

Open GitHub and create a new repo.
After you create a new repo in GitHub, open your terminal and cd into the folder you are trying to link to github.

Step 1) Inside your project folder you will initialize git by typing `git init` in the terminal that has the project folder open.

Step 2) Stage all of the changed files to using the `git add .` command.

Step 3) Commit all of the staged files using the `git commit -m ""` command typing whatever commit message you want inside the double quotes.

Step 4) Change your branch to main using the`git branch -M main` command.

Step 5) Add your Git repo to your project using `git remote add origin "your repo link here"` do not use the "" and copy the link from the SSH tab of the GitHub repo to use your SSH key we previously added.

Step 6) Push your code from your computer to GitHub using `git push -u origin main`

Step 7) Checkout your new Git repo in your browser and show off your code!

### Git VCS - Branches and Merging

Git is a VCS (Version Control System). There are a few popular ones, but git ends up being a top choice because of its branching and merging feature.

If we think back to our past projects, when we wanted to implement some major changes to our code and failed our popular options were to

- `???Z` throughout our files and hope for the best
- Comment out a ton of code and hope to restore the functionality of our code to a previous version
- Seriously contemplate coding out our project from scratch again
- Curl up into a ball and hope the code would revert via magic

[Git's about page has 4 great reasons why it works so well for individuals and large teams.](https://git-scm.com/about)

- Frictionless Context Switching - Switch between branches, whenever! No worries!
- Role-Based Codelines - Have many versions of your code - Production, Development, Day-to-Day etc.
- Feature Based Workflow - Create a new branch for each feature
- Disposable Experimentation - if a branch doesn't work out, you can just walk away or toss it. It has no impact on the working code

You may be thinking 'this sounds too good to be true!' It's not! But there is a catch! Git requires changing the way we are used to working on projects. Which means it takes some time and practice to learn to use git.

![git workflow from git about page](https://i.imgur.com/MXiZRI0.png)

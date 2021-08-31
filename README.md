# GithubPoc

**GIT Overview:**

It is a good idea to introduce yourself to Git with your name and public email address before doing any operation. The easiest way to do so is:
- $ git config --global user.name "Your Name Comes Here"
- $ git config --global user.email you@yourdomain.example.com

**Adding a new project:**

Create new directory and add git in it.
  - $ mkdir project
  - $ cd project
  - $ git init

Git will reply
  - Initialized empty Git repository in .git/

You’ve now initialized the working directory—​you may notice a new directory created, named ".git".

**Cloning a  project**

After creating project on github or if project is already on github and you want to copy the code from there you have to clone the project:
- $ git clone https://github.com/tj-valuecoders/githubPoc.git

This  will needed your github username and password for authentication.

**Making changes in Project:**

Modify some files, then add their updated contents to the index:
- $ git add file1 file2 file3

You are now ready to commit. You can see what is about to be committed using git diff :
- $ git diff

You can also get a brief summary of the situation with git status:
- $ git status
```
On branch master
Changes to be committed:
Your branch is up to date with 'origin/master'.
  (use "git restore --staged <file>..." to unstage)

  modified:   file1
  modified:   file2
  modified:   file3
```
  
If you need to make any further adjustments, do so now, and then add any newly modified content to the index. Finally, commit your changes with:

- $ git commit -m “commit message”

Alternatively, instead of running git add beforehand, you can use

- $ git commit -a

which will automatically notice any modified (but not new) files, add them to the index, and commit, all in one step.
A note on commit messages: Though not required, it’s a good idea to begin the commit message with a single short (less than 50 character) line summarizing the change, followed by a blank line and then a more thorough description. The text up to the first blank line in a commit message is treated as the commit title, and that title is used throughout Git.
  
**PUSH and PULL:**

Now you have to push your changes to remote , so that your local changes are reflected on remote github.
- $ git push origin branchName

Now if you want to pull the code from other branch into your working branch then you can do via pull command:
- $ git pull origin branchName

**Note: we can use ($ git rebase) instead of pull that will be a good approach to get rid from conflicts**



**Playing around Project History/Commits**

At any point you can view the history of your changes using
- $ git log

If you also want to see complete diffs at each step, use
- $ git log -p

Often the overview of the change is useful to get a feel of each step
- $ git log --stat --summary

To check list of commits
- $ git log --oneline
 
**Managing Branches**

Now we want to create new branch:
- $ git checkout -b “brnachName”

If you also want to switch branch from one branch to another branch
- $ git checkout branchName

If you want to check list of branches you can do with:
- $ git branch

If you want to delete any current/remote branch:
- $ git checkout -d/-D “brnachName”

If you also want to switch branch from one branch to another branch
- $ git checkout branchName

If you want to check list of branches you can do with:
- $ git branch

If you also want to merge branch current branch to another branch
- $ git merge anotherbranchName (its a fast-forward merge)
- $ git rebase anotherbranchName (it will merge only the latest commits)

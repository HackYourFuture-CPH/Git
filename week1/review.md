Tutorial for HackYourFuture Git basics :octocat:. 
This tutorial has 6 sections:

1. Command line interface (bash)
2. Git
3. Branches
4. Github
5. Pull requests
6. Checkout


Also you can watch the class recordings [here](https://drive.google.com/open?id=1eT5xWxG2GQHLAxMRNp2Bnb4VcSnJpb7s).

And the slides used in the class can be found [here](https://drive.google.com/open?id=1sR3er7alG-LXNadByoiNHlTiwhxrDgzlJaTt_GdTImY).


# 1. Command line (bash)

We used the command line a lot, a few basic commands we need are:
 - `pwd` to find where we are, in which folder/directory.
 - `ls` to list all the contents in the current directory.
 - `cd <folder_name>` to change directory to `folder_name`.
 - `mkdir <folder_name>` to create a new folder/directory named `folder_name`.

Marco has also made a cool video with 10 important commands, which you can see [here](https://www.youtube.com/watch?v=kN1-tseJnt0&amp).

# 2. Git

## 2.1 What is Git

* [ ] Version Control (aka Revision control, source control)
* [ ] Distributed version control system, Linus Torvalds, 2005
* [ ] GIT: Global Information Tracker

Bottom line: it is a program used to track changes in your files (in particular code).

If you need, you can read more here:
 - what is version control: https://www.atlassian.com/git/tutorials/what-is-version-control (5 min)
 - what is git: https://www.atlassian.com/git/tutorials/what-is-git (6 min)


## 2.2. Configuring Git

On your local machine, in the command line type:

```
git config --global user.email "email@email.com"
git config --global user.name "username"
```

Make sure that the email is the same you used for the github account.
You can run these commands again whenever you want to change the email or the user name.

To set the default text editor used by Git to vscode, you can run:

```
git config --global core.editor "code -w"
```

This command assumes you can start vscode from the command line by just typing `code`. On macOS this doesn't seem to work right out of the box, and you might want to check the top answer [here](https://stackoverflow.com/questions/29971053/how-to-open-visual-studio-code-from-the-command-line-on-osx) and follow the instructions there, or just ask your mentor to help you :)


## 2.3 Creating a repository on your computer

Create a new directory in your home directory or any other suitable location using:

```
mkdir git_example
```

Enter the directory:

```
cd git_example
```

and create a new git repository using:

```
git init
```

You can also create a repository on your local machine by cloning a remote repository with `git clone <URL>` command. This copies the repository from a remote machine (typically github) and initializes it on your machine. You can try to clone some public repositories on [github.com](www.github.com).

Before creating any repository make sure you are not inside a git repository already. This is very important!!! To do so type `git status`, if you get an error it means you are not inside a git repository and you can safely create a new one.


## 2.4 Workflow
 Working Directory -> Index -> Local 
 Your local repository consists of three "trees" maintained by git. The first one is your Working Directory (workspace) which holds the actual files. The second one is the Index which acts as a staging area, and finally the local repository itself which actually contains your commit history.


### 2.3.1 add and commit

The basic Git workflow consists of two steps.
First, you add files/changes (to the index/staging area) to be committed.

```
git add <file_name>
```

Second, you actually commit (save) your changes by doing:

```
git commit -m "Commit message"
```


# 3 Branches

## 3.1 Why Branches ?

To expand.
Trees need branches to expand.
Banks needs (office) branches to expand.
Company needs (code) branches to expand.
E.g. Branches for Bugs, testing, featuers, production, staging etc.


### 3.2 Working with branches

To view a list of all the local branches on your machine, run:
```
git branch
```

To create a new branch run:
```
git branch <branch_name>
```

To move to a branch run:
```
git checkout <branch_name>
```

Always check in which branch you are before creating a new one. 
For instance, for your homework you should always be in the master branch when you create your homework branch.


# 4. GitHub:

## 4.1 What is GitHub

GitHub is a code hosting platform for version control and collaboration. It lets you and others work together on projects from anywhere. There are other platforms like Gitlab and Bitbucket.


## 4.2 Creating a repository

Using your GitHub account, you can create a repository to which you can add files. 
Name the repository `git_example`. Create a public repository and **do not** check the box to create a README file. 
After you create the repository, the URL of your web page would be something like https://github.com/martamatos/git_example. Replace `martamatos` with your username. If you append `.git` to this URL, you will get the name of your GitHub repository: https://github.com/martamatos/git_example.git


## 4.3 Connecting your local repository to the remote repository on Github

When you have an existing local repository (in your computer) that you want to connect to the repository you just created on Github, you need to run:

```
git remote add origin <link_to_gihub_repository>
```

Here you are basically adding the connection to a remote repository named `origin`, where `origin` stands for the link to the github respository, for instance `https://github.com/marta_matos/git_example.git`.
To check if your local repository is connected to a remote repository (e.g. on Github) and what is the address of that repository you can always run:

```
git remote -v
```


## 4.4 Pushing changes

To send (upload) the contents of a given branch on your local repository to your remote repository (on github), run

```
git push origin <branch_name>
```

However, this command will fail if there are changes in the remote repository that you do not have on your local machine yet. In that case you first need to get (download) the changes from the remote repository to your local machine. To do so you do:

```
git pull origin <branch_name>
```


For the sake of consistency (and to avoid mistakes), make sure that when you push you do it to a branch with the same name as the branch where you are, e.g. if you are on a branch named `my_homework` then push to a branch named `my_homework` by typing `git push origin my_homework`.

When pulling, if you want to pull from a branch named, for instance `git_homework`, make sure that you are in a branch with the same name (`git_homework`) on your computer as well, and only then do `git pull origin <branch_name>`.


## 4.5 Troubleshooting

You could encounter errors if you do not follow the exact procedure as described above.
```
error: failed to push some refs to 'git@github.com:myrepo.git'
```
Solution:
```
git pull origin master
```

or

```
fatal: refusing to merge unrelated histories
```
Solution:
```
git pull --allow-unrelated-histories
```

## 4.6 Generating the ssh keypair

To create an ssh keypair start by opening GitBash (in Windows) or the terminal (in Linux and Mac) and type:

```
$ ssh-keygen -t ed25519 -C "your_email@example.com"
```

Supply your Github email address instead of this fake one. 
Accept the default location storage (default file) for the keys. When prompted for a passphrase either leave it empty or make up one, and don't forget it! This is your private key, do not share it with anyone.
You will have an `id_ed25519.pub` file in the directory  `~/.ssh/`, where `~/` is your home directory. 

You want to copy the contents of the `id_ed25519.pub` (open it with a text editor or use the command `cat id_ed25519.pub` in the command line to print out the contents of the file).  After you copy the contents of the `id_ed25519.pub` file, go to your GitHub account, go to the settings, find SSH and GPG keys option and add New SSH key.


# 5. Pull requests

Pull requests make it easier for developers to collaborate. They provide a user-friendly (web) interface for discussing proposed changes before integrating them into the official project.
In the simplest form, pull requests are a means for a developer to notify a team member that they have completed a feature. But the pull-request is more than just a notification. It's a dedicated forum where teammates can post feedback, push follow-up commits.
Even though it is named a pull request it is more like a merge request, where you ask for permission to merge a branch into another branch.


## What does a pull request contain:
When you create a pull request, you want another developer to merge your branch into another branch. This means that you need to provide 2 pieces of information to create a pull request:
* the destination branch
* the branch to be merged

Pull requests can be used in conjunction with various workflows:
* [Feature-branch workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/feature-branch-workflow)
* [Gitflow workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow)
* [Forking workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/forking-workflow)


The workflow you use in your homework is pretty much the Feature-branch workflow, where the central repository is your `hyf-homework` repository, and the feature branch is your homework branch. Also, instead of BitBucket you use Github.

There are a few other differences, for instance:
- in the section "Start with the master branch", instead of doing:
    ```
    git checkout master
    git fetch origin 
    git reset --hard origin/master
    ```
  to update your master branch, you should just do:

    ```
    git checkout master
    git pull origin master
    ```
- once the pull request is accepted you just merge it directly on github, no need to use the command line :)



# 6. Checkout

We didn't talk about this in class, but it's kind of nice to know.
To move around a repository, to different branches or commits, you can use the `git checkout` command.

 When you do `git log` you see the history of all commits in the branch where you are. The first line of each commit looks like `commit fe48414f5c9a21c986ae3c65f198d477a81299cc`, where the weird sequence of numbers and letters is the commit hash key. If you  want to go to a particular commit all you need to do is:

```
git checkout <commit_hash_key>
```

At that point you can take a look around and see what your code looked like. 
Do **not** commit any changes when are in that state, it will probably get you into trouble :)

To return to the latest commit you do:

```
git checkout <branch_name>
```

Where `branch_name` is the name of the branch where you are.
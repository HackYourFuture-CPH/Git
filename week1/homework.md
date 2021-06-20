# Homework

In this exercise you will get some practice submitting your homework by pushing it to Github and then creating a pull request. 
You will be using this workflow every week to submit your homeworks, so it's important that you get comfortable with it.
You will also practice adding/commiting files one by one.

You will use the `hyf-homework` repository on your computer to do the exercise. Here are the instructions:

1. Go to your `hyf-homework` repo on your computer
2. Go to branch `master`
3. Create a branch for your homework, named `git-week1`, and move to that branch
4. Inside the folder `hyf-homework/git/week1` create 3 new files:
   - a file named `my_favorite_food.txt`, inside the file write your favorite food recipe (you can just find a random recipe on google and paste it in the file ;) 
   - a file named `my_second_favorite_food.txt`, inside the file write the recipe for your second favorite food
   - a file named `countries.txt`, where you list three countries that you have visited (this doesn't need to be true, you can just write the names of three random countries)
5. Add and commit the file `my_favorite_food.txt`;
6. Add and commit the file `my_second_favorite_food.txt`;
7. Add and commit the file `countries.txt`;
8. Push your changes into your `hyf-homework` repository on Github.
9. Go to Github and create a pull request (PR) from the branch `git-week1` to `master`
10. Copy the link, post it on slack and tag your mentors, we will then check your homework and ask you to do a few more tasks :)


Commands that you will need: 
 - `git branch <branch_name>` - to create a new branch named `<branch_name>`
 - `git checkout <branch_name>` - to move to a branch named `<branch_name>`
 - `git add <file_name>` - tell git to start tracking a file and to update what will be commited
 - `git commit -m "commit_message"` - commit (save) your changes
 - `git push origin <branch_name>` - push (upload) your changes in your current branch to your github repository into the branch named `<branch_name>`.
 
 
 ***Note***
  For the sake of consistency (and to avoid mistakes), make sure that when you push you do it to a branch with the same name as the branch where you are, e.g. if you are on a branch named `my_homework` then push to a branch named `my_homework` by typing `git push origin my_homework`.
  
  When pulling, if you want to pull from a branch named, for instance `git_homework`, make sure that you are in a branch with the same name (`git_homework`) on your computer as well, and only then do `git pull origin <branch_name>`.


Other useful git commands:
 - `git status` - remember, it is your best friend, it tells you what is the state of your repository and sometimes what you should do.
 - `git branch` - this is your second best friend, it tells you in which branch you are (you can also see where you are when you do `git status`)
 - `git log`
 - `git log --oneline`
 - `git pull origin <branch_name>` - pull (download) your changes from your github repository in the branch named `<branch_name>`, into your current local branch. 

Command line commands that might be useful:
 - `pwd`- print working directory, to know where you are 
 - `cd <folder_name>` - to go inside a folder named `<folder_name>` 
 - `cd ..`- to go to the parent folder of your current folder
 - `mkdir <folder_name>` - to create a new folder
 - `ls`- list all the folder contents
 - `ls .*` - list all the folder contents, also invisible folders/files (e.g. the git folder)

# Class exercises

These exercises are meant for a flipped classroom, where the students prepare in advance and the class time is dedicated to exercises.

The first two exercises are a priority, the third is nice to do, the fourth and fifth can be skipped. The fifth can be done by the students as homework.


## Exercise 1

The goal of this exercise is to do some commits on our local repository and push them to github.
It will basically follow the first part of the class videos.

We will use the `hyf-homework` repo and the branch `master`.

1. clone your own `hyf-homework` repo into your computer (this is to get everyone on the same page, otherwise it can be a mess);
2. create a folder named `class_playground` under `hyf-homework/Git/week1`;
3. create the following files inside the `class_playground` folder: `apples_file.txt`, `bananas_file.txt`, `oranges_file.txt`;
4. add some text to each of the files;
5. add and commit the `apples_file.txt`;
6. add and commit both the `oranges_file.txt` and the `bananas_file.txt`;
7. add more text to the `apples_file.txt`;
8. add and commit the changes in the `apples_file.txt`;
7. push your changes to Github.



## Exercise 2

The goal of this exercise is to practice the homework workflow.
It will basically follow the second part of the class videos.

We will use the `hyf-homework` repo.

1. when you are on `master` branch, create a branch named `git_exercise_2` and move to it;
2. create a file named `my_homework.txt` inside `hyf-homework/Git/week1/class_playground`;
3. add some text to the `my_homework.txt` file;
4. add and commit the changes in the `my_homework.txt` file;
5. add more text to the `my_homework.txt` file;
6. add and commit the changes in the `my_homework.txt` file;
7. push the branch `git_exercise_2` to github;
8. on github, create a pull request from `git_exercise_2` to `master`;
9. on your computer add some more text to the `my_homework.txt` file;
10. on your computer, add and commit the changes in the `my_homework.txt` file;
11. push the branch `git_exercise_2` to github;
12. on github, check what happened to the pull request you created in step 8, and merge the PR
13. go to the `master` branch
14. update `master` by "downloading" the new commits from github: `git pull origin master` 



## Exercise 3

In this exercise you will get an error when pushing to github and you will have to solve it.

We will use the `hyf-homework` repo.

1. on your `hyf-homework` repo go to the branch `master`
2. create a branch named `git_exercise_3` and move to it;
3. on the folder `hyf-homework/Git/week1/class_playground` create a file named `colors.txt`;
4. add two colors to the file `colors.txt`, one per line;
5. add and commit the changes in the `colors.txt` file;
6. push the branch `git_exercise_3` to github.
7. on github, go to the branch `git_exercise_3` and add a color in the first line of the file `colors.txt`, commit your changes;
8. on your computer, add a color in the last line of the file `colors.txt`, add and commit your changes;
9. push the branch `git_exercise_3` to github.



## Exercise 4

In this exercise you will get a merge conflict and you will have to solve it.

We will use the `hyf-homework` repo.

1. on your `hyf-homework` repo go to the branch `master`
2. create a branch named `git_exercise_4` and move to it;
3. on the folder `hyf-homework/Git/week1/class_playground` create a file named `movies.txt`;
4. add two movie names to the file `movies.txt`, one per line;
5. add and commit the changes in the `movies.txt` file;
6. push the branch `git_exercise_4` to github.
7. on github, go to the branch `git_exercise_4` and add a movie name in a new line at the end of the file `movies.txt`, commit your changes;
8. on your computer, add a movie name in a new line at the end of the file `movies.txt`, add and commit your changes;
9. push the branch `git_exercise_4` to github.



## Exercise 5

The goal of this exercise is to get more familiar with branches.

Take notes of the answers to the questions in points 14, 15, 16, 17, 18, 19, 22, 23, 25, and 26. Discuss the answers in your breakout room.


1. create a new folder in your Desktop called `branch_exercise`;
2. using the command line go to that folder and create a new repository there (`git init`);
3. create a new file in that folder called `countries.txt`;
4. add two country names (one per line) to the `countries.txt` file;
5. commit your changes;
6. create a new branch named `add_countries`, move to that branch;
7. add two more country names (one per line) to the `countries.txt` file;
8. commit your changes;
9. go back to `master`;
10. create a new branch named `add_cities`, move to that branch;
11. create a new file named `cities.txt`;
12. add two city names (one per line) to the `cities.txt` file;
13. commit your changes;
14. go back to `master` and take a look around your folder. Which files do you see? What are their contents?
15. do `git log --oneline`. Which commits do you see?
16. go to the `add_countries` branch and take a look around your folder. Which files do you see? What are their contents?
17. do `git log --oneline`. Which commits do you see?
18. go to the `add_cities` branch and again take a look around your folder. Which files do you see? What are their contents?
19. do git `log --oneline`. Which commits do you see?
20. now go to `master`;
21. merge the branch `add_countries` with master (`git merge add_countries`);
22. take a look at your folder, which files do you see? What are their contents?
23. do `git log --oneline`. Which commits do you see?
24. now merge the branch `add_cities` with master (`git merge add_cities`)
25. take a look at your folder, which files do you see? What are their contents?
26. do `git log --oneline`. Which commits do you see?

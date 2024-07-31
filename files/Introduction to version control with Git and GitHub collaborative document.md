![](https://i.imgur.com/iywjz8s.png)


# Introduction to version control with Git and GitHub collaborative document

2024-07-30

Welcome to The Workshop Collaborative Document.

This Document is synchronized as you type, so that everyone viewing this page sees the same text. This allows you to collaborate seamlessly on documents.

----------------------------------------------------------------------------

This is the Document for today: https://tinyurl.com/git-erasmus

##  🫱🏽‍🫲🏻 Code of Conduct

Participants are expected to follow these guidelines:
* Use welcoming and inclusive language.
* Be respectful of different viewpoints and experiences.
* Gracefully accept constructive criticism.
* Focus on what is best for the community.
* Show courtesy and respect towards other community members.
 
## ⚖️ License

All content is publicly available under the Creative Commons Attribution License: [creativecommons.org/licenses/by/4.0/](https://creativecommons.org/licenses/by/4.0/).

## 🙋Getting help

To ask a question, just raise your hand.

If you need help from a helper, place a pink post-it note on your laptop lid. A helper will come to assist you as soon as possible.

## 🖥 Workshop website
https://esciencecenter-digital-skills.github.io/2024-07-30-ds-git-ErasmusMC/

🛠 Setup
https://esciencecenter-digital-skills.github.io/2024-07-30-ds-git-ErasmusMC/#setup

## 👩‍🏫👩‍💻🎓 Instructors
Sven van der Burg, Carsten Schnober

## 🧑‍🙋 Helpers
Claire Donnelly, Serena Defina

## 👩‍💻👩‍💼👨‍🔬🧑‍🔬🧑‍🚀🧙‍♂️🔧 Roll Call
Name/ pronouns (optional) / job, role / social media (twitter, github, ...) / background or interests (optional) / city


## 🗓️ Agenda
* 09:30	Welcome and icebreaker
* 09:45	Workshop Introduction
* 10:00	Introduction to Git, setting up Git
* 10:30	Coffee break
* 10:45	Creating a repository, tracking changes.
* 11:30	Coffee break
* 11:45	Exploring history, ignoring things
* 12:30	Lunch Break
* 13:30	Remotes in GitHub
* 14:15	Coffee break
* 14:30	Collaboration with Git and GitHub
* 15:15	Coffee break
* 15:30	Collaboration through forking
* 16:15	Wrap-up
* 16:30	END

## 🏢 Location logistics
* Coffee?
* Toilets?
* Emergency?
* Wifi?

## 🎓 Certificate of attendance
If you attend the full workshop you can request a certificate of attendance by emailing to training@esciencecenter.nl.
Please request your certificate within 8 months after the workshop, as we will delete all personal identifyable information after this period.

## 🔧 Exercises


#### 1. Which command(s) below would save the changes of myfile.txt to my local Git repository?

1. `git commit -m "my recent changes"`
2. `git init myfile.txt`
   `git commit -m "my recent changes"`
3. `git add myfile.txt`
   `git commit -m "my recent changes"`
4. `git commit -m myfile.txt "my recent changes"`




#### 2. Committing Multiple Files
Remember that the staging area can hold changes from any number of files that you want to commit as a single snapshot.

1. Add some text to ``mars.txt`` noting your decision to consider Venus as a base
2. Create a new file ``venus.txt`` with your initial thoughts about Venus as a base for you and your friends
3. Add changes from both files to the staging area, and commit those changes.


#### 3. (optional) A new repository
1. Create a new Git repository on your computer called bio.
2. Write a three-line biography for yourself in a file called me.txt.
3. Add the file to the staging area, and commit your changes.
4. Make a modification.
5. Display the differences between its updated state and its original state.


###  Exploring history exercise

1. Recovering Older Versions of a File

Jennifer has made changes to the Python script that she has been working on for weeks, and the modifications she made this morning “broke” the script and it no longer runs. She has spent ~ 1hr trying to fix it, with no luck…

Luckily, she has been keeping track of her project’s versions using Git! Which commands below will let her recover the last committed version of her Python script called data_cruncher.py? Multiple options might be correct:

1. `$ git checkout HEAD`
2. `$ git checkout HEAD data_cruncher.py` <- Correct answer
3. `$ git checkout HEAD~1 data_cruncher.py`
4. `$ git checkout <unique ID of last commit> data_cruncher.py` <- Also correct







2. (optional) Understanding Workflow and History

What is the output of the last command in

```
$ cd planets
$ echo "Venus is beautiful and full of love" > venus.txt
$ git add venus.txt
$ echo "Venus is too hot to be suitable as a base" >> venus.txt
$ git commit -m "Comment on Venus as an unsuitable base"
$ git checkout HEAD venus.txt
$ cat venus.txt #this will print the contents of venus.txt to the screen
```

1. Venus is too hot to be suitable as a base
2. Venus is beautiful and full of love <- Correct
3. Venus is beautiful and full of love <- Correct
4. Venus is too hot to be suitable as a base
5. Error because you have changed venus.txt without committing the changes





3. (optional) Reverting a Commit

Jennifer is collaborating on her Python script with her colleagues and realizes her last commit to the project’s repository contained an error and she wants to undo it. git revert [erroneous commit ID] will create a new commit that reverses Jennifer’s erroneous commit. Therefore git revert is different to git checkout [commit ID] because git checkout returns the files within the local repository to a previous state, whereas git revert reverses changes committed to the local and project repositories.
Below are the right steps and explanations for Jennifer to use git revert, what is the missing command?

1. `________ # Look at the git history of the project to find the commit ID`
2. `Copy the ID (the first few characters of the ID, e.g. 0b1d055).`
3. `git revert [commit ID]`
4. Type in the new commit message.
5. Save and close

ANSWER: `git log`



### Optional exercises during SSH setup check
#### 1. CHECKING UNDERSTANDING OF `git diff`
Consider this command: `git diff HEAD~9 mars.txt`. What do you predict this command will do if you execute it? What happens when you do execute it? Why?

Try another command, `git diff [ID] mars.txt`, where [ID] is replaced with the unique identifier for your most recent commit. What do you think will happen, and what does happen?

#### 2. GETTING RID OF STAGED CHANGES
`git checkout` can be used to restore a previous commit when unstaged changes have been made, but will it also work for changes that have been staged but not committed? Make a change to mars.txt, add that change using `git add`, then use `git checkout` to see if you can remove your change.

#### 3. IGNORING NESTED FILES
Given a directory structure that looks like:

```bash
results/data
results/plots
```

How would you ignore only `results/plots` and not `results/data`?

#### 4. INCLUDING SPECIFIC FILES
How would you ignore all `.csv` files in your root directory except for final.csv? Hint: Find out what `!` (the exclamation point operator) does

### GitHub GUI

Browse to your `planets` repository on GitHub. Under the Code tab, find and click on the text that says “XX commits” (where “XX” is some number). Hover over, and click on, the three buttons to the right of each commit. What information can you gather/explore from these buttons? How would you get that same information in the shell?

#### (optional) Push vs. Commit

In this lesson, we introduced the `“git push”` command. How is `“git push”` different from `“git commit”`?

#### (optional) GITHUB TIMESTAMP
Create a remote repository on GitHub. Push the contents of your local repository to the remote. Make changes to your local repository and push these changes. Go to the repo you just created on GitHub and check the [timestamps](https://swcarpentry.github.io/git-novice/reference.html#timestamp) of the files. How does GitHub record times, and why?

### Exercise: Working as a project collaborator (in pairs)

Do this exercise in pairs. Each person is submitter (S) and reviewer ( R) once.

#### Part 1
- PERSON R: Add person S as a collaborator to your repository
- PERSON R: Create an issue in the repository
- PERSON S: Clone this repository to your system
- PERSON S: Create a new branch
- PERSON S: Make the changes requested in the issue
- PERSON S: Push the changes to the remote repository on GitHub
- PERSON S: submit a Pull Request, refer to the issue (e.g. "Closes #1")

#### Part 2
- PERSON R: review the Pull Request
- PERSON S: address the comments
- PERSON R: approve the Pull Request
- PERSON S: merge the Pull Request

#### (Optional) Create and resolve merge conflicts
- PERSON R: Push a change on the main branch
- PERSON S: Push a change to the same line of code on a new branch
- PERSON S: Open up a pull request
- This should lead to a merge conflict
- PERSON S+R: Try to solve the merge conflict

## 🧠 Collaborative Notes

#### Workshop Introduction:

- Track changes on steriods: you can see who made changes to the code, feature called 'git blame'
- Like an unlimited undo button where you can easily go back in time to a previous version
- Good for collaboration, you are able to work in large teams.

#### Introduction to Git, setting up Git

- Check your version of git installed:
`git --version`

- First we will configure git and fill out our information. This is information other people will see later:
    ```
    git config --global user.name "Your Name"
    git config --global use.email your.email@email.com
    git config --global core.autocrlf input
    git config --global core.editor nano
    ```

    The `--global` flag fills out this information globally, all this information will be the same for every git repository

    Check your configuration: `git config --global --edit`
    If you want to check what options you have: `git config --help`
- Create a new directory (folder) in the location you want it:

    ```
    cd /path/to/location
    mkdir planets
    cd planets
    ```
    Initialise a repository:
    
    ```git init```
    
- Check the status of your repository:

    ```git status```
    
    This should be clean for now:
    
    ```
    On branch main

    No commits yet
    ```
    
#### Creating a repository, tracking changes
- Create a new file `nano mars.txt`, enter some text and save. If we check `git status` again, we will see that git has now noticed that there have been some changes. 
    (Don't worry about Windows warning you about line breaks)

- We can now add and commit the changes we have made:

    ```
    git add mars.txt
    git commit -m "Add information about Mars"
    git status
    ```
    The commit message is something you or other people can look back on to know what changes were made. It is nice if all changes that are made in a commit, logically belong together. For best practices the commit should be written like an instruction in the present tense. 
    
    `git add` can be used to add multiple files that belong to the same change:
    `git add mars.txt venus.txt`
    
    If you are sure that you can commit changes to all files in the repository you can also do: `git add .`
    Be careful not to add any unwanted files before committing though. 
    
    
    You can also check `git log` which will give you a history of the changes.
 
- If you want to remove changes that you have not committed yet, you can undo them by:

    `git checkout --mars.txt`
    
    or
    
    `git restore mars.txt`

    If you have accidentally added (or staged) a file and you want to remove it from the staging area: `git restore --staged mars.txt`. This will still keep your changes but you can then use `git checkout` to undo them if needed. 
 
- If you want to view the changes between a file and the repository, then you can run:
`git diff mars.txt`

    `git log` shows you the history of the changes you have made
    `git log --oneline` compresses the information to one line per change

- Git works on file level, if add a sub-directory it will not track those changes. However, if you add files to that sub-directory, then it will consider it a change and keep the structure. 

    So, if we create a sub-directory called "spaceships" and add a file "apollo-11":

    ```
    Changes not staged for commit:
      (use "git add <file>..." to update what will be committed)
      (use "git restore <file>..." to discard changes in working directory)
            modified:   spaceships/apollo-11.txt
    ```
    
 #### Exploring history, ignoring things
 
- If you need to revert to a certain commit, you can use the hash identifier, which looks like this:
    ` commit e7cecbd7b449bbacd2be4fcd1410486e34407372`
    In practice you only need the first 6 characters: 
    `e7cecb`
    or anything which is unique.
    Alternatively you can use `HEAD` and count back from there. i.e `HEAD~1` will be the commit before the last one.
    
    These identifiers can also be used to look at differences between 2 commits:
    `git diff HEAD~1`
    
- We can use these identifiers to revert previous changes we have made:
    `git checkout e7cecbd7b mars.txt`
    
    or 
    
    `git restore e7cecbd7b mars.txt`
    
    This will come up as a change to commit, since git keeps a history of all changes including undoing changes. 
    
#### Ignoring files

First, lets create some data files and check git status:

```
mkdir results
touch a.csv b.csv results/a.out
git status
```

Your output should look something like this:

```
On branch main
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        a.csv
        b.csv
        results/
```

We do not want to commit these data file so lets create a gitignore file:

```
touch .gitignore
```

In it we can add the following information:

```
*.csv
*.out
```

If you check git status again, your output should look something like this:

```
On branch main
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .gitignore
```
    
We can now commit the gitignore file, as other people would also want to ignore the same files. 

#### Remotes in GitHub

First lets create a repository in GitHub. Go to the github website, by going to your profile and clicking on "new". Pick an owner, for now make it public and do not add a README file. 

We now have an empty repository. As we already have a repository, we want to push an existing repository.

Make sure you copy the `ssh` instructions from GitHub and not the https instructions:

```
git remote add origin git@github.com:user/repo-name.git
git branch -M main
git push -u origin main
```

If you accidentally did copy the https you can correct it in the following way:

```git remote set-url origin new.git.url/here```

Then run through the same 2 commands. 

### Collaboration with Git and GitHub
#### Add a person as collaborator:
Go to settings -> Collaborators -> Add people

There is a distinction between what Git as a tool provides versus what GitHub as a platform provides. GitHub as a platform provides additional useful functionality like issues, peer review, continuous integration and a nice visual overview of everything.

#### Open up a new issue
Go to `Issues` -> `New issue`

#### Clone the repository
Click on the big green `Code` button on GitHub. Then in your terminal:
```
git clone <ssh-url>
```

#### Git branches
Branches in Git allow you to work on different tasks or features in isolation from the main codebase, enabling parallel development and easy integration of changes. They help manage multiple lines of development without interfering with each other, ensuring a stable and organized workflow.

##### Create a new branch
``` 
git branch mars-colour
```

##### Move into new branch
```
git checkout mars-colour
```

#### Open up a pull request
- Go to the `Pull requests` tab.
- Click on the green `New pull requests` button.
- Select the correct base branch (the branch that you want to merge into, typically main) and the head branch (the branch that you want to merge, typically the branch that you just created)

#### Peer review
- In the `Pull requests` tab go to the open pull request.
- Go to the `Files changed` tab within the Pull Request view. 
- Add comments inline and or then click on the green `Review changes` button to finish your review


To view the "Network" you can go to the "Insights" in the repository page on GitHub and click on "Network"
## 💬 Feedback

### Tips :bulb: 

- More exercises to practice can never hurt!
- A light theory introduction about working directory, stage and .git folder would be useful.
- Explain some terminology a bit more (e.g., what are branches, ...) (I am not familiar to this terminology)


### Tops :+1:

- I really like the editable webpage with information
- Good pace and interaction
- I like that you regularly check whether everyone understands/follows  
- The pace is perfect (as a beginner) and the concepts are explained in a way that make them more tangible! 
- Very useful exercises and good pace!
- explanation clear and practice exercices were well calibrated

### Sven's reflections:
- We will get a bigger exercise in the afternoon, where we will really put you to the test!
- Learn by doing approach

## Git 30 seconds
### Scoring table
| **Group** | round 1 | round 2 | round 3 | Total |
|-----------|---------|---------|---------|-------|
| 1         |      2  |    2    |     4   |   8   |
| 2         |     2   |    3    |     3   |   8   |
| 3         |     3   |   3     |     1   |   7   |
| 4         |    3    |    2    |    1    |   6  |
| 5         |       3 |      2  |   2     |   7   |


### Round 1
- Collaboration
- GitHub
- `git status`
- staging area
- `git add`

### Round 2:
- Commit message
- `.gitignore` file
- Reproducibility
- The terminal
- `HEAD`

### Round 3
- Reusability
- `git log`
- Repository
- `main` branch
- `git config`

## 📚 Resources

- [Github cheat sheet](https://education.github.com/git-cheat-sheet-education.pdf)
- [Command line cheat sheet](https://www.stationx.net/linux-command-line-cheat-sheet/)
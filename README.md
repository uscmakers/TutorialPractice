# TutorialPractice

## Need help at any time?
If you need ANY help, feel free to make a github issue! On the top tab on the github page, you will see a tab called "issues". Please write your issue there and a member of our team will answer your questions asap!

## Crash Course of How to Navigate the Command Line 
If you have windows, you want to use the "command prompt" application. If you use a Mac, you want to use the "terminal".

- cd ..: go back to the previous directory
- cd folder1: move inside folder1
- ls(mac)/dir(windows): list all the files in the current directory
- mkdir <folder_name>: make a folder with the name "folder_name"
- rm <file_name>: delete the file "file_name" permanently
- rm -r <folder_name>: delete the folder "folder_name" and all its contents permanently
- touch <file_name>: create an empty file

## Installation:
### Windows:
1. Get a github account and accept the invitation from "uscmakers" *important*
2. Go to https://git-scm.com/download/win and the download will start automatically.
3. Download sublime with this link: https://www.sublimetext.com/3 (select the windows version)
	1. If you already have a text editor such as VS Code, BBedit, Notepad++, Atom, etc, feel free to skip this step
4. Download the linux shell https://ubuntu.com/download/desktop. If you feel comfortable with the windows commands, feel free to skip this step.


### Mac:
1. Get a github account and accept the invitation from "uscmakers" *important*
2. Run: <git --version> on your terminal. If you don't already have git installed, this will prompt you to install git.
3. Download sublime with this link: https://www.sublimetext.com/3 (select the mac version)
	1. If you already have a text editor such as VS Code, BBedit, Notepad++, Atom, etc, feel free to skip this step
	
## Linking Github to the Terminal
1.  In the terminal, type these following commands. Make sure your email is your USC email, and make sure that your username is the username affiliated with your github.
```
	git config --global user.name "Your name here"
	git config --global user.email "your_email@example.com"
	git config  user.name "Some One"
	git config  user.email "email@email.com"
```
2. Generate and copy your ssh key 
```
	ssh-keygen -t rsa -C "your_email@example.com"
	pbcopy < ~/.ssh/id_rsa.pub
```
3. Go to github and sign into your account. Click on your profile picture on the top right of the screen and click on the "settings"
4. Click on "SSH and GPG keys", and add a new SSH Key. You should be able to control + v to copy the ssh key you generated in step 2. Make sure to title it something recognizable and relevant.
5. Type "ssh -T git@github.com" into your terminal. If you see "Hi username! You've successfully authenticated, but Github does not provide shell access.", you are good to go!


## Guide:
0. Complete Installation, Crash Course, and Linking Github to the Terminal in this order. (If you have worked with git on your laptop, you may have to do none/some of the steps)
1. Clone this repo:
	1. Navigate to the folder you want to copy this tutorial into using the crash course guide above (please use the command line!)
	2. Copy the address of the repo. Press the "code" button on the right top of the screen of the online github repo, and copy the address with either ssh or https
	3. type "git clone <address_you copied in step 1b>"- you should see the repo in your file explorer now!
	4. Navigate inside of the cloned folder by typing "cd TutorialPractice".
2. Pull Updates:
	1. In the command line, type "git pull" to pull all the updates from the upstream branch. Depending on when you do this, you might see other peoples' files load into your directory. This "refreshes" your local repository to reflect what the remote repository looks like.
3. Create a Branch
	1. Go back into the command line, and type "ls" or "dir". You should be able to see a README.md, and potentially other people's names.
	2. Now, lets orient ourselves and check which branch we are on by typing "git status". You should see that you are on the master branch. By default, you start on the master branch.
	3. Lets create a new branch by typing "git checkout -b <branch_name>" PLEASE title your branch your full name. Ex. Radhika_Agrawal
	4. Type "git status" again. You should see that you are now on your newly created branch.
4. Create a file
	1. Create a text file and name it your full name. Ex. Radhika_Agrawal.txt
	2. Open the file in your file explorer with Sublime (or editor of your choice)
	3. Write your name in the file!
	4. Save and close the file
5. Upload your code to github
	1. Type "git add -A". "-A" means all files
	2. Type "git commit -m "type a message here"". -m means that you will attatch a message to associate your commit with. In this case, just type a generic message briefly describing what you will be uploading.
	3. Type "git push". This should give you an error saying that you have not specified an upstream branch. 
	4. Copy what the error told you to type, which should be "git push --set-upstream origin <branch_name>". By doing this, you are setting where you will later be merging the branch to.
6. Create a pull request on github
	1. Navigate back to the github website and refresh. 
	2. Navigate to the "pull requests" tab
	3. You should see a button that says 'Compare and Pull Request'. Click on the button.
	4. Confirm that the "base" branch is Master, and the branch to be "compared" is your new branch.
	5. Title the pull request with your name Ex. Jenny's Pull Request. You can leave the comment section blank, or you can tag your partner in it.
7. Assign a Reviewer to your PR
	1. Look at the partner list that was generated for you. Add your partner as a reviewer on the right tab.
	2. Submit the pull request! 
8. Review your partner's PR
	1. If your partner has submitted a pull request, you need to review it so she/he can merge the branch back into master. Navigate to the PR tab at the top, and find your partner's pull request. 
	2. Look at the changes, and hit approve. Note: During an actual code review, you can add comments/suggestions, and choose not to approve it if necessary.
9. Merge your PR:
	1. Once your partner approves your PR, you can merge your branch into master. Find your PR on the PR page, and merge it into the master branch.
	2. You will then be able to see your file on the master branch!
10. Merge Conflicts:
	1. Look at Shivani's and Jenny's demo (which will also be uploaded to our Youtube channel), and practice making merge conflicts and resolving them! *optional*
	
## Git Shortcuts

- git pull: pull updates from the upstream branch
- git pull origin master: pull updates specifically from the master head 
- git add -A: add ALL the updates that were made in the local repo
- git add jenny.txt: add ONLY the updates that were made in jenny.txt
- git commit -m "write a message": commit the updates
- git push: push the updates from your local repo to your remote repo
- git push --set-upstream origin branch_name: push the updates to the remote repo AND set your upstream branch to master
- git status: check which branch you are on
- git checkout -b branch_name: make a new branch and switch branches
- git checkout branch_name: switch branches
- git branch --list: list the branches that you have on your local machine
- git branch -d branch_name: delete the branch

## Advanced Git Shortcuts

- git reset --soft HEAD~1: Undo one git commit (change the ~1 to ~5 if you want to undo the past 5 commits)
- git stash: Lets pretend that you were working on branch "avl" to work on avl trees. Even though you don't want to commit the code yet, you want to hop over to another branch to work another feature. You can save the work you were doing on the avl trees using stash.
- git stash list: List all the stashes you've stored
- git stash apply: You can re-apply the changes you've stashed back to your branch (most recent stash)
- git stash apply@{2}: Re-apply the second to most recent stash to your branches. (you can change the number to specify which stash you are talking about)


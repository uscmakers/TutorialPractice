# TutorialPractice

##Crash Course of How to Navigate the Command Line 
If you have windows, you want to use the "command prompt" application. If you use a Mac, you want to use the "terminal".

cd: change directory
	cd ..: go back to the previous directory
	cd folder1: move inside folder1

ls(mac)/dir(windows): list all the files in the current directory
mkdir <folder_name>: make a folder with the name "folder_name"
rm <file_name>: delete the file "file_name" permanently
rm -r <folder_name>: delete the folder "folder_name" and all its contents permanently
touch <file_name>: create an empty file

##Installation:
Windows:
1. Get a github account and accept the invitation from "uscmakers" *important*
2. Go to https://git-scm.com/download/win and the download will start automatically.
3. Download sublime with this link: https://www.sublimetext.com/3 (select the windows version)
	a. If you already have a text editor such as VS Code, BBedit, Notepad++, Atom, etc, feel free to skip this step


Mac:
1. Get a github account and accept the invitation from "uscmakers" *important*
2. Run: <git --version> on your terminal. If you don't already have git installed, this will prompt you to install git.

##Guide:
1. Clone this repo:
	a. Navigate to the folder you want to copy this tutorial into using the crash course guide above (please use the command line!)
	b. Copy the address of the repo using either ssh or https
	c. type "git clone <address_you copied in step 1b>"- you should see the repo in your file explorer now!
2. Create a file
	a. Go inside the repo using the command line
	b. Create a text file and name it your full name. Ex. Radhika_Agrawal.txt
	c. Open the file in your file explorer with Sublime (or editor of your choice)
	d. Write your name in the file!
	e. Save and close the file
3. Pull Updates:
	a. In the command line, type "git pull" to pull all the updates from the upstream branch. Depending on when you do this, you might see other peoples' files load into your directory.
4. Create a Branch
	a. Go back into the command line, and type "ls" or "dir" to confirm you can see the file
	b. Now, lets orient ourselves and check which branch we are on by typing "git status". You should see that you are on the master branch. By default, you start on the master branch
	c. Lets create a new branch by typing "git checkout -b <branch_name>" PLEASE title your branch your full name, just like your file. Ex. Radhika_Agrawal
	d. Type "git status" again. You should see that you are now on your newly created branch.
5. Upload your code to github
	a. Type "git add -A". "-A" means all files
	b. Type "git commit -m "type a message here"". -m means that you will attatch a message to associate your commit with. In this case, just type a generic message briefly describing what you will be uploading.
	c. Type "git push". This should give you an error saying that you have not specified an upstream branch. 
	d. Copy what the error told you to type, which should be "git push --set-upstream origin <branch_name>". By doing this, you are setting where you will later be merging the branch to.
6. Create a pull request on github
	a. Navigate back to the github website and refresh. You will be able to see your newly created branch in the dropdown list of branches.
	b. Now, create a "pull request" by clicking "Compare & pull request". 
	c. Title the pull request with your name Ex. Jenny's Pull Request. You can leave the comment section blank.
7. Assign a Reviewer to your PR
	a. Look at the partner list that was generated for you. Add your partner as a reviewer on the right tab.
	b. Submit the pull request! 
8. Review your partner's PR
	a. If your partner has submitted a pull request, you need to review it so she/he can merge the branch back into master. Navigate to the PR tab at the top, and find your partner's pull request. 
	b. Look at the changes, and hit approve. Note: During an actual code review, you can add comments/suggestions
9. Merge your PR:
	a. Once your partner approves your PR, you can merge your branch into master. Find your PR on the PR page, and merge it into the master branch.
	b. You will then be able to see your file on the master branch!
10. Merge Conflicts:
	a. Look at Shivani's and Jenny's demo, and practice making merge conflicts and resolving them! *optional*

##Git Shortcuts

git pull: pull updates from the upstream branch
git pull origin master: pull updates specifically from the master head
git add -A: add the updates 
git commit -m "write a message": commit the updates
git push: push the updates from your local repo to your remote repo
git push --set-upstream origin branch_name: push the updates to the remote repo AND set your upstream branch to master
git status: check which branch you are on
git checkout -b branch_name: make a new branch and switch branches
git checkout branch_name: switch branches
git branch --list: list the branches that you have on your local machine
git branch -d branch_name: delete the branch


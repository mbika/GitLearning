# GitLearning

This repo contains information about how to work with Git and list of commands that is mostly used for developers while managing their code versions.


Git Basic & its Commands
========================
=> when we install git we get a platform called gitbash , where we can execute the git commands.When the files move to local repository,
version controlling start.

Setting up your username globally for specific user on a specific machine : Command

1> git config --global user.name "Bikash"

Setting up your email globally for specific user on a specific machine : Command

2> git config --global user.email "bikash.mohapatra@collabera.com"

To see list of global Configuration has been done

3> git config --global --list

To initialise the current folder as git repo.This will create a hidden folder as .git, which stores all the configuration necessary for git to run.

4> git init

To see whater files present in Git

5> ls

To see the hidden files present in Git

6> ls -a  ['a' represents all files including visible files along with hidden files]

To check how many untracked files. Initially the code is created that is untracked files.

7> git status : Untracked files we can see by using this commands

To move untracked files to staging area

8> git add <filename>

To check if the files move from untracked to staging

9> git status

Send multiple untracked files to taging area[may be all 100 files  and folder also, we use below command]
['.' (dot) represents current working directory, having all files and folders]

10> git addd .

If we have put all untracked files to staging area, but we want to remove one file from staging area to untracked area, use below command

11> git rm --cached <filename>   [File name Ex:javanotes5.pdf]  || git reset <filename> [File name Ex:javanotes5.pdf]

To check if the file has moved back from staging to untracked

12> git status

Now commit the files to local repository for managing the version

13> git commit -m "provide the message"  [Example:"Fisrt Commit"]

To check how many version stored in local repository or we can say how many commits has been done in local repository.
When we do a commit, a commit id will be generated.Always the latest commit will show in order.

14> git log

if we want only commit information, there is a shortcut command

15> git log --oneline

To create empty files we have command

16> touch <filename1> <filename2> <filename3> <filename4>

Note : ["If we have some private files and we dont want git should touch these files,there is a way we can do that, which is know as "git ignore" file.
"git ignore" is an configuration file.Any file whose name is specified in .gitignore, cant be accessed by git.As long as the files are present in 
.gitignore, git cant touch it. gitignore file is used to hiding your sensitive data."]

To create gitignore file and add files to it, there is a command

17> cat > .gitignore
<filename1>
<filename2>
<filename3>
<filename4>
To comeout of the file we have to use a command ["ctrl+d"]

To check the no of files present in .gitignore file, we have command 

18> cat .gitignore
  

  
Lets learn about Git Branching and its commands.
================================================
  
Git Branching
=============
=> This is a feature of git which allows team members to create code related to
various functionalities on different branches and later merge with them with the 
"master" branch.Master is the default branch of git.

=> Branching help us to create the code in an uncluttred way

Commands
========

To see the list of all local branches

1> git branch

To see the list of all branches (local and remote)

2> git branch -a

To create a new branch

3> git branch <branch-name>

To move into a specific branch

4> git checkout <branch-name>

To create a branch and also move into it

5> git checkout -b <branch-name>

To merge a branch

6> git merge <branch-name>

To delete a branch that is already merged.This is also called as soft delete.

7> git branch -d <branch-name>

To delete a branch that is not merged.This is called as hard delete. 

8> git branch -D <branch-name>

Note : Whenever the branch is created the entire commit history of the
parent branch will be copied into the new branch.

Note : Irespective of on which branch a file is created or modified git
only check from which branch it is committed and that file belongs to the committed branch only.

# tutorialGitHub

What is Git | What is GitHub | Git Tutorial | GitHub Tutorial | Devops Tutorial | Edureka
https://www.youtube.com/watch?v=xuB1Id2Wxak&t=2570s
(1 hr 44 min)

Sign up and sign in to Github
- Create a new repository

Install Git
- from https://git-scm.com/download/win - download and install the 64 bit version for windows
- Create a local directory e.g. tutorialGitHub
- open git bash in folder
- git init
- Create a README.md
  - echo "# tutorialGitHub" >> README.md
- git add README.md
  - adds file to the index prior to commit
- git commit -m "first commit"
  - -m for commit message of the change
- git branch -M main
- git remote add origin https://github.com/ray-oh/tutorialGitHub.git
  - create a variable origin to represent the github location for the project
- git push -u origin main
- git status

Manage multiple files or folders
- clear
  - clears git bash

- git add -A
  - adds all untracked files to index
- git commit -a
  - commits all files (note small "a" as opposed to capital "A" for add

Parallel development - Branching
- create a new branch off a commit
  - git branch firstbranch
    - create a branch with name firstbranch - with copy of files from "master"
  - git checkout firstbranch
    - to switch to firstbranch
  - git add -A
  - git commit -a -m "making changes in first branch"
  - git checkout master
    - switching back to master branch
    
 Parallel development - Merging
 - git merge <source branch>
  - ensure you are in the target e.g. master - checkedout in master
 - git rebase master
  - from source - "merge" or rebase from firstbranch to master
  - reduce the number of branches - and create a cleaner linear sequence of commit history

Pushing changes from local repository to central/"github" repository
- git push
- require SSH - generate a SSH public key
  - ssh-keygen
  - cat /c/Users/Reshma/.ssh/id_rsa.pub   # view the ssh key string
  - copy and paste into github > settings > SSH and GPG keys > New SSH key > name of key e.g. SSH2
  - ssh -T git@github.com   # authentication of ssh with github
- create a new branch in github
  - git checkout firstbranch   # switch to firstbranch in local repository
  - git push origin firstbranch   # push all changes to github - including creation of a new firstbranch
- git push origin master    # to push all changes for master branch on local to central repo

![image](https://user-images.githubusercontent.com/115925194/196036734-98aceae0-0c6b-4873-8dc2-874336be40a6.png)

Rollback / revert to previous commits/versions
- checkout what has been changed in history
  - git log    # to check the commit hash
  - copy the first 8 of commit hash
  - git checkout <first 8 of the hexa decimal digits of the commit hash> <name of file to revert>
  

Learn Github in 20 Minutes
https://www.youtube.com/watch?v=nhNq2kIvi9s




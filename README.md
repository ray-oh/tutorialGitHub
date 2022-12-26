# tutorialGitHub
Tutorial on how to use Git, Github and VS Code for collaborative development

## Git and Github

1. [Getting started with Git](https://git-scm.com/book/en/v2/Git-Basics-Getting-a-Git-Repository)
2. [Github quick start - hello world](https://docs.github.com/en/get-started/quickstart/hello-world)
  - [Github pricing](https://github.com/pricing)
    - unlimited public/private repo
    - 2000 CI/CD minutes/month for private repo.  Free for public repo.
      - [GITHUB ACTIONS & CI/CD IN 3 MINS - youtube](https://www.youtube.com/watch?v=KwGMYJ6nZD8)
    - 500MB of package storage for private.  Free for public.
3. [Git fork vs clone](https://www.theserverside.com/blog/Coffee-Talk-Java-News-Stories-and-Opinions/git-fork-command-example-tutorial#:~:text=A%20Git%20fork%20is%20nothing,contribute%20to%20the%20code%20base.)
4. [Using Git with VScode - youtube](https://www.youtube.com/watch?v=i_23KUAEtUM)
5. [Learn Github in 20 Minutes - youtube](https://www.youtube.com/watch?v=nhNq2kIvi9s)
  - Collaborating on a open source project
  - Fork the main repo to your own repo, create feature or topic branches, test and if stable, propose a pull request to incorporate back to the main repo.
  - Branching - long running branches and topic branches https://git-scm.com/book/en/v2/Git-Branching-Branching-Workflows
6. [What is Git | What is GitHub | Git Tutorial | GitHub Tutorial | Devops Tutorial | Edureka - youtube](https://www.youtube.com/watch?v=xuB1Id2Wxak&t=2570s) (1 hr 44 min)

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
  


Git Fork vs Clone

![image](https://user-images.githubusercontent.com/115925194/209470556-3f73efc0-5574-4b97-a14e-3e1ba031567f.png)


## Advance Git Commands

- [Git Rebase & Squash in VS Code using GitLens Supercharge - youtube](https://www.youtube.com/watch?v=3o_01F04bZ4)
- [Pull Requests in VS Code - youtube](https://www.youtube.com/watch?v=LdSwWxVzUpo)

## Markdown

- [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
- [Cheatsheet for markdown syntax](https://www.markdownguide.org/cheat-sheet/)

## Licensing

- [Licensing a repo in github](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/licensing-a-repository)
  - You're under no obligation to choose a license. However, without a license, the default copyright laws apply, meaning that you retain all rights to your source code and no one may reproduce, distribute, or create derivative works from your work.
  - Most people place their license text in a file named LICENSE.txt (or LICENSE.md or LICENSE.rst) in the root of the repository
  - Some projects include information about their license in their README. For example, a project's README may include a note saying "This project is licensed under the terms of the MIT license."
- [Opensource legal guide](https://opensource.guide/legal/)
  - Making your GitHub project public is not the same as licensing your project. Public projects are covered by GitHub’s Terms of Service, which allows others to view and fork your project, but your work otherwise comes with no permissions.  If you want others to use, distribute, modify, or contribute back to your project, you need to include an open source license. For example, someone cannot legally use any part of your GitHub project in their code, even if it’s public, unless you explicitly give them the right to do so.
- [Contributor License Agreement](https://ben.balter.com/2018/01/02/why-you-probably-shouldnt-add-a-cla-to-your-open-source-project/)
  - In short, you can think of a CLA as somewhat of a “reverse open source license”. Whereas open source licenses are a copyright grant for users to use the project, a contributor license agreement, at its core, is the right for the project to incorporate a contributor’s code. Contributors may also be required to attest that they have the right to submit the code, or the CLA may include an explicit patent grant. Some CLAs go so far as to actually assign the developers copyright to the project.
  - Unlike licenses, however, contributor license agreements, or CLAs, are not standardized, meaning if you’re a contributor, you’ll have to read each CLA to determine what legal rights you’re giving away, before contributing (and hope you can parse what’s often dense legalese if you’re not yourself a lawyer).

## Other useful links

- Using VS Code Editor
  - [Getting Started with Visual Studio Code - youtube](https://www.youtube.com/watch?v=B-s71n0dHUk&list=PLj6YeMhvp2S5UgiQnBfvD7XgOMKs3O_G6)
  - [vscode web editor](https://code.visualstudio.com/docs/editor/vscode-web)
    - https://vscode.dev

- Using Jupyter Notebooks with VS Code
  - [Get started with Jupyter Notebooks in less than 4 minutes - youtube](https://www.youtube.com/watch?v=h1sAzPojKMg)
  - [Jupyter Notebooks in VS Code Walkthrough - youtbue](https://www.youtube.com/watch?v=DA6ZAHBPF1U)

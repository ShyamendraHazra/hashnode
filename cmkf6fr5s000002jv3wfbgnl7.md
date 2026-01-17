---
title: "Git basics and terminologies for beginners."
seoTitle: "Git basics and terminologies"
datePublished: Thu Jan 15 2026 08:17:42 GMT+0000 (Coordinated Universal Time)
cuid: cmkf6fr5s000002jv3wfbgnl7
slug: git-basics-and-terminologies-for-beginners
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1768464861918/122290db-eb28-4202-8a08-dc8a9fe70120.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1768465029036/f5360fc1-72e4-480a-a710-0f8fe1ca6e60.png
tags: version-control, git, gitcommands, version-control-systems

---

## What is Git?

If you are new to Git or version control in general it may seem daunting at first but trust me once you really understand the basics of Git, then Version Controlling using Git will become your second nature. Let’s keep it simple and focus on one step at a time.

Git is a free and open source Version Control System, that’s it. Now what is a Version Control System you may ask? It is a tool that helps you to track changes of your work across the whole working process. Simply Git allows you to store multiple snapshot of the changes you make to your work. Each newer snapshot contains some newer changes that were made after previous snapshot and link to it’s previous older snapshot of changes. So that you can easily undo redo or edit those changes.

Git enables multiple developers to work on the same project in their own machines simultaneously while contributing and sharing the latest changes with each other seamlessly. Each contributor work on and make changes to their version of the project and share the newer snapshots or commits with the rest, who then add that newer snapshot or commit (Sometimes multiple commits) into their local copy of the project and continue working with the newer version. Git also allows us to detect and resolve conflicts between two different commits made by different people.

That is all a Version Control System essentially does. If you want to understand VCS (Version Control Systems) in more depth then [read this article](https://blog.shyamhz.dev/version-control-system) that goes in detailed explanation of what a VCS is and why it is required in modern development. But you don’t have to worry about it too much to understand essentials of Git and from this article you can easily understand the basics of it.

Before we go all in with what is Git and how it works and all , let’s first understand why should we even concern ourselves with something like Git at all. What features Git offers that you should consider investing your time and energy to learn a new tool and it’s terminologies? Why should you even consider using Git in your projects at all?

Actually there are multiple crucial and unavoidable reasons to do so.

## Why use Git at all?

1. **Where, What and When :** When tracking changes with Git the first and foremost benefit you get is every snapshot that you ever make in your project is visible forever and can be identified later on no matter how big your project grows. Each and every change that you commit will be marked in full details as in Which files were changed, what changes were made exactly and when the changes were added permanently (committed) in essence the exact date and time the changes were committed.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1768400464792/19e34706-f79c-4b2c-a954-d5b50c0bf2e6.png align="center")
    
    Git solves that.
    
2. **By Whom :** Each commit also stores who authored it or created it. This might seem like a small addition but in real world development processes this can be a life saver, In bigger corporations teams of multiple people work on the same project and sometimes each team working on a specific part of the projects consists of multiple developers or experts. And in that scenario this detail makes co-operation, collaboration and teamwork a lot better. Especially it helps pinpointing source of the problems easily.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1768405241018/e2db578c-c264-455f-8e41-d31f86ccfb5d.png align="center")
    
    Git solves that too.
    
3. **Branching:** Git allows you to keep more than one parallel version of the project. This feature is actively utilized to test new features without tampering the main working files, fix bugs, roll out updates and provides other convenient and quality of life experiences for the developers.
    
    You can create a branch from any snapshot or commit of your project and you can merge branches to your main branch to integrate changes created in that secondary branch to your main branch and this is a popular technique that is actually used to develop and test new features without breaking the whole product or features at the consumer’s end.
    
4. **Rollback and Revert :** Git allows you to revert changes by switching to an older commit as working state or current state of the project and create a branch or make changes on that branch directly. This feature gives us a superpower to go back in the timeline of our project and fix mistakes or even diverge in a different branch from that exact point with a totally different timeline or simply undo any errors.
    
5. **Real world Collaboration:** Git is distributed Version Controlling System or simply said a distributed tracking tool. It not only allows a group of people working together on the same project, individually and locally, track and control their work but also it can act as a centralized hosted service that tracks changes made by everyone involved and working on the project in one place. Github, Gitea and Gitlab are just few examples that host the projects that are using Git on their remote server using this feature of Git.
    

## Brief History

Git was created in 2005 by Linus Torvalds, a Finnish programmer who is most popular as the creator of Linux kernel since 1991. After facing problems from proprietary Version Control Systems he created his own Version Control System to maintain the source code of Linux and named it Git.

***“Since its birth in 2005, Git has evolved and matured to be easy to use and yet retain these initial qualities. It’s amazingly fast, it’s very efficient with large projects, and it has an incredible branching system for non-linear development“ -*** [Official Git Docs](https://git-scm.com/book/en/v2/Getting-Started-A-Short-History-of-Git#:~:text=Since%20its%20birth%20in%202005%2C%20Git%20has%20evolved%20and%20matured%20to%20be%20easy%20to%20use%20and%20yet%20retain%20these%20initial%20qualities.%20It%E2%80%99s%20amazingly%20fast%2C%20it%E2%80%99s%20very%20efficient%20with%20large%20projects%2C%20and%20it%20has%20an%20incredible%20branching%20system%20for%20non%2Dlinear%20development)***.***

## Basic Git Terminologies

Before we go ahead and jump into all the fancy commands of Git, let’s first understand few key terms and words used in context of Git and version controlling in general. So that when we finally start learning Git, it would be a lot easier for us to do so without being confused in all the fancy jargon.

**Git Repository:** A Git repository is basically the workspace or the Project root directory or folder that is actively being tracked by Git for new changes. In the next section we will see how to setup our project as a Git repository or repo in short. This repo contains your project files and the .git folder where Git stores all of the internal files and folders used to maintain the Git repository.

**Tracked files:** As you can probably tell already that this refers to all the files that Git is actively tracking for changes and if any of these files are changed Git will tell you that they were modified. Yes if you create new files in your Git repo Git will not track them by default but report that they are untracked and need your attention. To actually track untracked files and changes in those files you must first tell Git to track it manually.

You can also create a “**.gitignore**” file, the file and directory names written inside this file are ignored and not tracked by Git.

**Staging area:** After you tell Git to track a new file in your Git repository manually or you tell Git to add the changes made to the files that are already being tracked, Git adds them to staging area to commit them, this is the place where all the recently added files and changes live. Git cannot preserve new changes directly. You need to add changes to staging area for Git to be able to preserve them.The staging area is basically Git’s way to know what exact changes will be committed in next commit and Git commits only the changes present in staging area.

**Commit:** Commit is an action that you tell Git to perform when you want to preserve all the changes added to the staging area. This new snapshot or changes permanently added to the repository is called a commit. Each commit has it’s own id or hash that Git uses to reference them individually. Each commit contains some additional metadata like author, creation date , link to previous commit.

**Branch:** Your Git repository can have multiple parallel versions that do not affect each other. These versions are called branches each with their individual commit history and different version of the project. Each repository has at least one branch called main. Git keeps the files in your working directory just as same as latest commit in the currently active branch. If you wish to incorporate changes committed in one branch into another you can merge them together.

**HEAD:** HEAD is nothing but a pointer that points to the currently active branch of your repository and that branch points to the latest commit made in that branch.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1768410074095/724a1e6e-ef7a-42d2-a141-d21583f444e5.png align="center")

## Basic Git commands

1. **Initialize a Git repository :** To use Git in our project we first need to initialize our project as a Git repository, so that Git can track the changes we make. To do that we use
    
    ```bash
    git init
    ```
    
    command.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1767698427744/551afa9a-7308-4cde-86af-3ca5e87f0ff8.png align="center")
    
    It creates a .git repository inside your project folder and initializes you project as a Git repository and looks for any changes made inside the repository. Whether the repository is empty or already have some files when initializing it, this command does not delete anything and only creates the .git folder.
    
2. **Check repository status :** This next command is one that you will use very often. This command is used to check the status of tracking in our Git repository. All the changes that are made will be listed by this
    
    ```bash
    git status
    ```
    
    command. All the untracked files, tracked changes that are not staged yet and all the staged changes yet to be committed are shown by this command. This command is frequently used to track the state of our repository.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1767698462079/80a6b5c3-b3e2-451a-8d21-58adec8c8c39.png align="center")
    
3. **Add latest changes :** To add the changes that you made in your repository to the staging area you need to use the
    
    ```bash
    git add <filenames> ...
    ```
    
    command. This command adds only those files that were given in it’s arguments to the staging area. Once the files are in staging area they can be committed. Also if there are too many files that you want to add to the staging area or do not want to manually add the file names to the command you can use
    
    ```bash
    git add .
    ```
    
    command too. This ‘.’ at the end of the command means all the files including all the untracked files (if any).
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1767698498259/8ef4a0ca-5262-4da8-9794-2ff9292cb772.png align="center")
    
4. **Finally committing the changes :** After all the modified files or new files that you want to commit are staged in the staging area they can be committed with
    
    ```bash
    git commit -m "<commit message>"
    ```
    
    command. Be mindful that the commit message is mandatory and you must provide a commit message to every commit you make or it will fail to commit the changes. After being committed the changes will permanently be listed as a commit in the commit history. Next we will see how to see that commit history.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1767698566243/90057368-44e4-48aa-8920-bbcf425e151c.png align="center")
    
5. **See the Commit history :** You can list all the commits that you made till now with
    
    ```bash
    git log
    ```
    
    command. This command lists all the commits in a stack view .i.e newest to oldest fashion and the top most commit is the last one you made. For each and every commit, in addition to the commit id or hash the Author (the one who made the commit) and the date time timezone (when the commit was made) followed by the commit message are listed also.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1767698592122/92ca244b-bb79-41ff-97d2-ccefe4c3bb91.png align="center")
    
6. **See the differences :** If you want to see the difference between two commits in your repository to check exactly what changes were made between them you can use
    
    ```bash
    git diff <commit1 hash> <commit2 hash>
    ```
    
    command. This command displays the additions and deletions to the files across the commits.The commit that has the commit1 hash is treated as base and the second commit2 hash is treated as the newer commit so you need to put older commit hash first and newer commit hash later if you want to see the changes in the correct order.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1767699398505/8edfe5d6-6f25-4c8d-b980-9dc8ff8cbc47.png align="center")
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1767699443863/c51a5d03-ade7-4dd6-95c8-bdfea5d3cd82.png align="center")
    
7. **Reset commit history :** Sometimes it may happen that you want to undo one or more commits or simply put those changes back to staging area or working directory, for that we use
    
    ```bash
    git reset <commit>
    ```
    
    command. This command moves the branch to point to that commit.
    
    Depending on what flags you used, it may permanently delete the changes made after that commit or put them in the staging area or un-stage them completely but not delete them. Let’s understand these flags.
    
    1. **Default or --mixed reset:**
        
        ```bash
        git reset --mixed <commit>
        ```
        
        or simply
        
        ```bash
        git reset <commit>
        ```
        
        this command (or the --mixed flag) just moves the current branch to that specified commit and removes all the commits made after that commit, but also preserves the changes that were stored in those removed commits. Those changes are not marked for next commit or not kept in the staging area but in the working directory (inside the actual files) itself ready to be staged again.
        
    2. Soft Reset
        
        ```bash
        git reset --soft <commit>
        ```
        
        This flag also removes the commits made after the specified commit while preserving the changes made in them. -- soft flag keeps those changes in the staging area or in the index file simply marked for next commit.
        
    3. **Hard reset :**
        
        ```bash
        git reset --hard <commit>
        ```
        
        You need to use this flag with caution and only when you are sure you want to **permanently delete** all the changes made after the specified commit. This flag not only removes the commits made after the specified commit but also overwrites you project directory to be exactly same as it was in the specified commit removing all the newer changes.
        

## Summary

Above commands are few of the most commonly used Git commands and just enough for you to get started with Git in your projects. Although there are many more functionalities and tools Git offers but if you just use the above mentioned ones you can easily get started with it and then learn as you go.

Git has become a very popular and very successful version control system because of it’s easy-to-use, fast, efficient and very intuitive commands. Due to wide adaption of Git many Git repository hosting services like Github, GItlab , Gitea, Bitbucket are build around the Git as an ecosystem. Git is an essential addition to your toolbox that will save you from a lot of trouble and will prove more useful as more time you spend in you development journey!

Hopefully you learnt importance and basics of Git from this blog and now will easily be able to start using **Git**. **Thank you** for reading.
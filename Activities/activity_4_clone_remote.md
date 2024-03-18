# Working with local and remote repositories

As we have seen, a repository is a space to save, manage and organize the files of a project. However, if your computer is where you do all the work, how can you download a remote repository and work locally?

This is where the concepts of local and remote repository come in. You see, all your repositories on Github are versions of your project that are hosted on the Internet or any other network, therefore, they are remote spaces.

To access its contents, you need to create a space on your computer from which you can send and receive changes made to it. We will call this place local repositories. In this section, you will learn how to create a local repository on your computer and then connect it to the remote repository you just created on Github.

**What is a remote?**: This is the version of a repository or branch that is hosted on a server, most likely GitHub.com. Remote versions can be connected to local clones so that changes can be synced.

**What is a clone?**: A clone is a copy of a repository that lives on your computer instead of on a website's server somewhere, or the act of making that copy. When you make a clone, you can edit the files in your preferred editor and use Git to keep track of your changes without having to be online. The repository you cloned is still connected to the remote version so that you can push your local changes to the remote to keep them synced when you're online.

## Overview

In this activity, you will:

- [Clone a remote repository in your computer.](#cloning-the-remote-repository)
- [Making and pushing local commits](#making-and-pushing-local-commits)

## Steps

### Cloning the remote repository

1. Create a folder on your computer (name it with a single word).
2. From Git bash, or the terminal, enter the directory you just created.
3. On Github, go to your repository.
4. On the right side, press the **Code** button. A window appears with options to make the clone. Verify that you selected the SSH option. Copy the address that appears there, either by pressing the **Copy url to clipboard** button, or by copying the adress itself.

![Clone repo 1](.images/4_clone/4_clone_1.png)

5. Back in the terminal, we will use the **git clone** command to make a local copy of the repository. Make sure to replace `{ssh url}` with the address you just copied.

```bash
$ git clone {ssh url}
```
![Clone repo 2](.images/4_clone/4_clone_2.png)

**Note**: If you see the option “Are you sure you want to continue connecting (yes/no/[fingerprint])?” indicate **yes**.

6. Your remote repository will be cloned (downloaded) inside a directory of the same name of the repository, creating your local repository.

![Clone repo 3](.images/4_clone/4_clone_3.png)

7. You can now edit file and make local commits.

### Making and pushing local commits

Now that we have the local repository ready on our computer, we can start making changes on it.

To upload content to a remote repository branch, files must go through several stages in which the changes that have been made to them are updated and tested. For this we will the following Git commands:

- **git add {file or directory}**: If the file is already being tracked by the repository, it is added to the staging area. If not, the repository starts tracking the file, and adds it to the staging area.
- **git commit -m “{Commit description}”**: Register the changes in the local repository's history.
- **git push origin {Branch}**: Push files from your local repository to the remote repository.

With this, we can start uploading content to the repository we just created. The usual workflow with a repository is as follows:

![Clone repo 4](.images/4_clone/4_clone_4.jpg)

Let's create a file, add it to the local repository, and then upload it to the remote repository.

1. Inside the repository's directory, create a new file called: **Repo.html**.
2. Copy the following code inside the file:
```html
<!DOCTYPE HTML>
<html>
    <head>
        <title>Version control</title>
    </head>
    <body>
        <main>
            <h1>Git and Github lab!</h1>
        </main>
    </body>
</html>
```
3. Make sure that the “All files” option is selected in the “Type” field.
4. Open git bash, or the terminal.
5. Access the directory where your local repository is located.
6. Execute the following commands in order:

```bash
# Shows the current state of the repository. The Repo.html file
# should be in an untracked state.
$ git status 

# Git will start tracking the file, and also adds it to the staging area.
$ git add Repo.html 

# It will show that the file is in the stagin area, ready to be commited.
$ git status

# Creates a commit of the files in the staging area. Remember to add a meaningul message.
$ git commit -m "Added Repo.html file."

# It should show that you have commits that are not in the remote repository.
$ git status

# Takes the local commits, and sends them to the remote repository, syncing their histories.
$ git push -u origin main
```

![Push changes](.images/4_clone/4_clone_4.png)

7. Use the **git log** command to see the history of the repository. It will show what commit all the pointers are located. In this case, both the local repository (HEAD), and the remote repository (origin/main), are pointing to the last commit.
 
![Git log](.images/4_clone/4_clone_5.png)

6. Back in github, you should see the file we just created.

![Github changes](.images/4_clone/4_clone_6.png)

## Finish

After you finish this activity, you should know:

- How to create files in the local repository. 
- How to track them, or add them to the staging area.
- How to create local commits.
- How to sync local changes to the remote repository.

## Resources

- [git commands](https://education.github.com/git-cheat-sheet-education.pdf) 
- [git add documentation](https://git-scm.com/docs/git-add)
- [git commit documentation](https://git-scm.com/docs/git-commit)
- [git status documentation](https://git-scm.com/docs/git-status)
- [git push documentation](https://git-scm.com/docs/git-push)
- [Working with remotes](Linkhttps://git-scm.com/book/en/v2/Git-Basics-Working-with-Remotes#Fetching-and-Pulling-from-Your-Remotes)

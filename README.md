# Git repository for your PX Group

This file gives an outline how to use git. 

## Installation of Git

To use Git you have to install the Git software. You can find this at [Git Downloads](http://git-scm.com/downloads). Pick your version based on your operating system. Make sure you install the command line or bash tools during installation. This is to ensure you can use it during Command Prompt or a Terminal session.

## Getting access to your repository

Each of you will have a login. When you commit to your Git repository it will ask you to login to ensure there is an identity to go alone with your push.

Your git repository is located at (http://smartsrv1.scem.uws.edu.au/cs####.git)

*The hashes being your project code, for example cs1404*

To get a copy of this repository on your computer you will have to clone it. This means grab all the files relating to it. To do this open up a terminal window, navigate where you want your files to be stored [If this is a website make sure it is in your websites folder which will be served] and type:

```
    git clone http://smartsrv1.scem.uws.edu.au/cs1404.git
```

This will copy all the files to the current present working director (pwd).

## Check everything is working okay

You will have to make sure the remote repositories are setup properly. To do this type:

```
    git remote -v
```

This will show something like:

```
    push origin -> http://smartsrv1.scem.uws.edu.au/cs1406.git
    pull origin <- http://smartsrv1.scem.uws.edu.au/cs1406.git
```

## Branching

The power of git is within its branching capability. Think of a tree. You can branch off from a certain state of the repository and then add to it without touching, or breaking, anything in the main branch. Your repository already has a master branch setup, and this branch is really where all production ready code ends up. The typical scenario is, I have a great idea and I want to explore it with a new branch. After I've built it I then merge it back to the master once I feel it is ready for everyone else to have. 

Here is how simple it is to branch. Once you have cloned your branch you are on branch master. You can check this by typing:

```
    git branch
```

This should come back with:

```
    *master
```

To create a new branch based on master all you have to do is:

``` 
    git branch new-menu
```

This branch is only on your computer, the others in your team will not be able to see this. To jump into this branch you type:

```
    git checkout new-menu
```

You will now be on branch new-menu. To confirm this type:

```
    git branch
```

It will spit out this to confirm your move to the new branch

```
    master
    *new-menu
```

The Star being the identifier for the active branch. If you want to move back to master you do ```git checkout master``` again.

## Adding and Committing

Once you create, mod, or delete files you will have to add them to the repository to make sure they are managed by git. Just carry on normally with working with your project, but once you're ready, or think, you have completed something funky add it to be commited. Here is a simple tutorial to teach you how.

1. Create a new file in your git repository folder.
2. Make sure it has been picked up by git by typing ```git status``` into the terminal
3. Now stage it for the repository by typing ```git add --all .``` *--all* being all files even the deleted ones - as what was once tracked may be removed.
4. Finalise the commit with typing ```git commit -m "Added new file ####.php"``` This will now have given the changes you have done a hash and a message.

That's it you've now added changes.

## Share or merge you branch

You have a branch and you want to show it off. You have two options. You can either push back to the remote master branch so when another member pulls they have your update, or you push the branch so others can check it out. The later is recommended as it enables everyone to test it before you add it to your production ready code. It is recommended one person commits to the master branch. This means the one controlling the master is sent a message through trello or an email and they check it out. Once happy with it, they finally commit it to the master so everyone has the latest changes.

To push the branch to the remote you have to type:

```
    git push -u origin <branch-name>
```

The *-u* tells git to monitor changes to this if others work on it.

## How to get updated code from others

Once someone has updated code and pushed it to the remote repository everyone will now have access to it. To see the branches available you have to type:

```
    git fetch
    git branch -a
```

This will list all the branches locally and remotely which you can then checkout and work on.

If in doubt shoot me a message on trello and I can help you out.




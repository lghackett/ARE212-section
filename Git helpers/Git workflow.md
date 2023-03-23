# Git workflow cheat sheet

Let's say you have cloned a remote repository onto your computer, either a forked one or not, by copying the "Code" link and running ``git clone URL`` on your computer. Now you want to actually work with this code.

There is a standard order of operations when working with git. First, before starting to work in a repository, make sure you're as up to date as possible on the changes that might have been implemented in the remote repository. In order to "sync up" to the remote repository, use:

```
git pull
```

Note that you need to have used ``cd`` to get in the right folder in terminal first. This will "pull" the remote changes into your local computer. If you are working on a fork and want to pull changes that might be in the upstream repository (see the forking guide), then do:

```
git fetch upstream
git pull
```

This tells git, first go find (fetch) the upstream changes, then pull them in. 

Then you will do some work, and are ready to package up what you have done and push it up to the remote repository. There are a couple of simple steps here.

## Step 1: Staging.

If you make changes then type

```
git status
```

into terminal, you will see that there are "Untracked files" potentially marked in red. These are your changed files, but they haven't been marked, or staged, to be pushed to the remote yet. This staging step lets you choose all or a subset of these files for pushing to the remote. For example, you might have one file that's finished and ready to be shared, but another you're only half way through, so you stage just one. Or you might stage everything. To add these files to get ready to push, do:

```
git add filename
``` 

To stage all changed files at once, do:

```
git add .
```

## Step 2: Commiting

Now we want to _commit_ our staged files. Think of a commit as a bundle of changes that we want to send to the remote repository. Standard git advice is that it is good to commit often, as commits also create snapshots of your project in time you can go back to (think like versions you can revert to in Dropbox or Drive, but you control when the version is made!). You commit whatever is _staged_ (step 1). So now that we have staged, we create a commit. Commits should have a message, flagged with ``-m`` that explains what this bundle of changes is.

```
git commit -m "This is my commit message"
```

## Step 3: Pushing

Now that we have created our snapshot, we are ready to share it with our team by sending it from our local computer to the remote. This is done with:

```
git push
```

## Warnings

One of the most powerful features of git is that it allows you to resolve _conflicts_ between your code and your teammate's code where you both change the same thing. However, conflicts are much better avoided than resolved. You can avoid creating conflicts by making sure you always:

* Pull before starting to work. This makes sure you incorporate other people's work before making changes yourself.
* ``git status`` is your friend. Check in with her early and often.
* Communicate with your team! Who is working on what when? How will you organize your files?
* Use git branches. Branches are a slightly more advanced, good-practice git tool that I will hopefully touch on later, but I would be remiss if I didn't mention them here. 

<p align="center">
<img src=git_image.png  width="40%">
</p>



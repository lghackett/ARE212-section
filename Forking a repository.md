# Forking a repository

First, make sure you have [git installed](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) on your computer.

- Go to the remote repository on GitHub, and click "Fork"
- Now you will see that you have a version of that repository in _your_ GitHub account, not Ethan's. Click the green Code button and copy the link.
- In terminal, navigate to the subfolder you will want to store this repository into with ``cd``
- Clone your version of the repository into this folder with ``git clone`` + the link you copied from GitHub.
	- After, running ``ls`` in the terminal you should see a new folder!
- ``cd`` into this new folder you just cloned.
- Tell git on your computer where to look for updates:

```
git remote add upstream https://github.com/ligonteaching/ARE212_Materials
```

- The easiest way to work with these materials without generating conflicts is to create copies of the notebook _before_ editing it. 
	- In jupyter this is very easy; just select the file in the jupyter navigator that pops up after running ``jupyter notebook`` and click "Duplicate"
- Before class, run the following to get the most updated materials:

```
git fetch upstream
git pull 
```

- Version control your own work by adding, commiting, pushing to ``origin`` if desired!
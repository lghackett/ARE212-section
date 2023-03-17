# Forking a repository

1. Go to the remote repository on GitHub, and click "Fork"
2. Clone your version of the repository
3. Tell git on your computer where to look for updates:

```
git remote add upstream https://github.com/ligonteaching/ARE212_Materials
```

4. The easiest way to work with these materials without generating conflicts is to create copies of the notebook _before_ editing it. 
5. Before class, run the following to get the most updated materials:

```
git fetch upstream
git pull 
```

6. Version control your own work by adding, commiting, pushing to ``origin`` if desired!
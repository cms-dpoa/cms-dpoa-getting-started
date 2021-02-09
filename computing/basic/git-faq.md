# Git FAQ

## When to clone and when to fork

If you mainly make small and quick changes to the project, you can clone the original repository locally, make your updates to a new branch of your own, test them locally, and then push that branch to the original repository.

If you make bigger changes that you need to keep safe before pushing them to the original repository, you can fork the original repository to have a version of it of your own. You would work on your own fork, and when done, push your updates to the origin.

## What you mostly need

```
git checkout -b my-updates
#do you edits
git add youreditedfile anotheredititedfile
git commit -m 'describe my updates'
git push origin my-updates
```

In the repository, you will not use `git add.` to add all changed files, because it includes the html files that you do not need to push. They will be automatically generated.

## Checking things

Check the origin of your git repository (where your updates go when you push)

```
git remote -v
```
Output for this repository
```
origin  git@github.com:cms-dpoa/cms-dpoa-getting-started.git (fetch)
origin  git@github.com:cms-dpoa/cms-dpoa-getting-started.git (push)
```

Check your branch

```
git branch
```

Check your local updates (all of this gets committed if you do git add -a -m "my updates")

```
git status
```

## Updating

Update your local master from the original repository (e.g. before starting a new local branch)

```
git checkout master
git pull
```

## Deleting and undoing things

Delete a branch (or force with -D if it hasn't been merged yet and you really want to get rid of it), first change to the master branch 

```
git checkout master
git branch -d <branch>
```

Remove a file from your list of updates (added by `add`)

```
git reset filename
```

Wrong files in your commit? Undo the last commit with

```
git reset --soft HEAD~1
```


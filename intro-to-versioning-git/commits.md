# Commits

## Introduction

## Learning Goals

- Explain how a commit in git is made using the git add and git commit commands
- Practice versioning code by creating commits in git
- Practice observing commit history using the commands git status, git log, git show, and git diff
- Explain different ways of "undoing" commits using git revert and git reset

## Vocabulary and Synonyms

Commit message | a way to communicate to anyone looking at the commit what changes the commit has

## git Tracks Changes as a Diff

Tracked

Untracked

## Anatomy of a Commit

Diff
  per file, lines added and deleted
Commit hash
  identifier
Commit message
Parent commit
Other stuff
  author, date

## Commits Build a Commit History

git log



## Creating a Commit on Your Local Machine

Go from changes in code into a commit: move changes through these three areas

3 areas:

Local changes
Staged changes
Committed changes

### Local Changes
How do you get changes here?
Open up any file in this repository
make a change
save the file

observe the changes in git diff

How do you move changes to the next area?

git add filename
git add foldername
git add relative thing like . (adds all changes from all tracked files)
git add -A (adds all files, included untracked files)

#### Tracked vs. Untracked

Small aside: When you add a new file to a project, git by default doesn't care about it -- it doesn't track the changes in that file, and that file is untracked.

As a rule, the first time a file is created, we must explicitly ask git to track the file using git add -A or git add filename or git add foldername.

Another good reason to default to explicitly running git add filename per filename

### Staged Changes

How do you get changes here?
You only get changes here if you've added them

observe the changes in git diff --staged

How do you move changes to the next area?

git commit
git commit -m

the command `git commit -m "Commit Message"` does these things:

1. Creates a commit with the staged changes and the commit message
1. Brings the developer into vim by default to give you a confirmation screen
1. Once you exit the confirmation screen, you should see confirmation that the commit was created

#### The Commit Message

Commit messages

Always

Grammar conventions differ per team (start with a verb, start with your name)

#### Navigating vim While Creating a Commit

Callout: vim is simply the default, feel free to change this. We recommend changing it to:

### Committed Changes

## Observing the Commit History

git status
git log
git show
git diff

### Practical Workflow

Every time I start my day:
git log
git status

Every time I run git status and I want to see my local changes:
git status
git diff

When I think I'm ready to create a commit:
git status
git log
git show
git diff
git add
git commit
git log
git show

## Debugging git Commits

Follow the error message and search engines as best as possible

There's a lot to learn, so
- don't be afraid to use the suggestions that git provides, they're usually pretty accurate
- don't be afraid to learn more git more deeply
- don't be afraid to ask for help

## "Undoing" Commits

### What is a Revert, Actually?

It's natural to eventually think, "all of the changes in that commit were wrong! We need to get rid of those changes!"

If we want to get rid of all changes inside of a commit, we want to revert a commit.

This is different than deleting a commit. **git is not built for developers to delete commits often.** Instead, a revert of a commit is... actually, a second commit, and all of the changes in the commit are the opposite.

**Undoing a commit is best thought of as adding more changes.**

If you want to do something more custom or specific than that, you'll need to learn more git and apply it to your specific situation!

### Resetting Local, Staged, And Committed Changes

git reset 

## Summary

## Check for Understanding
# Creating a Local Repository

To start `git` version control, simply navigate to the directory and initialize `git`:
```bash
git init
```

Then, `git` will create a repository[^1] and start tracking changes in that particular directory. Now, the directory can be separated into 3 section:
- Working directory - Space containing tracked and untracked changes
- Staging area - Space containing tracked changes to be committed
- Repository - Space containing all the snapshot

[^1]: A `.git` folder will be created. It contains all files necessary for version control.

## Staging

There might be multiple newly created files or modified files in a `git` repository. `git` can track a single file or all of the files. A file is staged when it is intended to be tracked.

|Tracking|`command`|
|-|-|
|All changes| `git add .`[^2]|
|Single file| `git add [file]`|
|Multiple file| `git add [file1] [file2]`|

[^2]: Note that the globbing character `*` will only add all changes in the current directory.

Note that when a file is staged, further changes to the file will only be in the `working directory` but not in the `staging area`. If a commit is done, only the changes made prior to the staging will be included in the snapshot. It needs to be staged again prior to the commit if all of the changes should be in the same commit.

## Status
To get the status of a repository, in particular whether there is staged or unstaged changes:
```bash
git status
```

## `.gitignore`
There are log files or automatically generated files that might not be interested in tracking. It will however be tedious to exclude them everytime during staging. In such cases, a `.gitignore` file can be created in the root of `git` repository to ignore those files. `.gitignore` use glob pattern to exclude file, and each pattern is specified in a new line. A collection of `.gitignore` templates for programming languages can be found [here](https://github.com/github/gitignore).

## Changes
To get the changes (or differences) of a files:

|State|`command`|
|-|-|
|Unstaged|`git diff`|
|Staged|`git diff --stage`|

## Commit
When a commit is done, all tracked changes in staging area will be included to produce a snapshot. To do so:

|`command`|Description|
|-|-|
|`git commit`|Commit (Text editor specified in `core.editor` will be opened)
|`git commit -m 'Message'`|Commit with a short message|
|`git commit -a -m 'Message'`|Commit with a short message (skipping staging)[^3]|

[^3]: Only modified and previously tracked files, newly created file must be staged.

A commit message must be meaningful and concise. An example guideline can be found [here](https://www.conventionalcommits.org/en/v1.0.0/).

# Installation
- [Windows/Mac](https://desktop.github.com)

- [Linux](https://git-scm.com)

`git` is installed by default in most of Linux distribution. Otherwise, it can be installed via most package manager (`sudo dnf install git` or `sudo apt-get install git`).

To know if `git` is installed successfully:

`git --version`

If installed successfully, it will tell you the version.

# Setting
There are 3 different configurations:

|Level|Config Location|Effect|`command`
|-|-|-|-|
|System|`/etc/gitconfig`|Whole system|`git config --system`|
|Global|`~/.gitconfig`|User|`git config --global`|
|Local|`.gitconfig`|Repository|`git config [--local]`[^1]|

[^1]: Local configuration can only be set inside a `git` repository, the `--local` flag is optional.

Useful flag:

|Flag|Description|
|-|-|
|-e| Open config file with editor|
|--list| List settings|

User information:

|Information|`command`|
|-|-|
|Username|`git config --global user.name "firstname lastname"`|
|Email|`git config --global user.email "example@github.com"`|
|Editor|`git config --global core.editor "gedit"`|
|Code Highlighting|`git config --global color.ui auto`|

## Private Email
The email in the config will be recorded in the commit history and used by Github to identify the commit user. This information will be available to anyone with access to the repository. To keep email address private, Github provides `no-reply` email in the form of `ID+username@users.noreply.github.com`. This information can be found in `Settings/Access/Email` tabs. See [here](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-github-user-account/managing-email-preferences/setting-your-commit-email-address).

# Help
The information here is not meant to be exhaustive. `git` has an official book [here](https://git-scm.com/book/en/v2).
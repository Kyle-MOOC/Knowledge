# History
To get a history of commit:

|`command`|Description|
|-|-|
|`git log`| Show log of commit|
|`git log --oneline`| Show simplified log of commit (one line per commit)|
|`git show [SHA-1]`| Show specified commit|

Note that each commit is associated with a single `SHA-1` hash. This `SHA-1` hash is used for ensuring data integrity and not for security feature. When refering to the commit, only the first 4 characters are required as long as there is no ambiguity.

# Path Changes
To properly track the path changes, use the `git` variant of command instead of `bash` command.

|Task|`command`|
|-|-|
|Move|`git mv`|
|Remove|`git rm`|
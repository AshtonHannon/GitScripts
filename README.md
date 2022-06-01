# GitScripts
---
Includes two Batch files 'gitinit.bat' and 'gitscript.bat' to help automate the creation of git repositories as well as common operations used to maintain git repositories.

All operations assume that SSH with the respective repository is initialized and setup properly.

### - gitinit.bat
Includes two commands: 'init' and 'clone'
- `init`: Used on FIRST TIME SETUP of a git repository to sync local repository with remote repository (main branch) and create an initial commit.
- `clone`: When provided with the SSH link to the given repository, it will clone the repository in the current directory that the `gitinit.bat` file resides.

### - gitscript.bat
Includes eight commands: 'add', 'commit', 'push', 'reset', 'default', 'clear', 'exit'
- `add`: Will ask if you want to add all files. If not, then it will ask for `git add` specific parameters to be applied.
- `commit`: Will ask if you want to include a short commit message. If 'FILE' is inputted, then it will prompt to be supplied with the name of a file in the current     working directory whos contens will be used as the commit message instead. For example, if `MyCommitMessage.txt` contains "Hello this is my commit message!", then the commit message will be "Hello this is my commit message!" when `MyCommitMessage.txt` is inputted as the filename.
- `push`: Will push whatever the current staged changes are. Will prompt for SSH password as normal.
- `reset`: Executes `git reset` which clears the current staged changes.
- `default`: Will prompt for commit message. The quick solution to add, commit, and push as it will add all files, commit with the inputted commit message, and push to the repository all in one command.
- `clear`: Clears the terminal
- `exit`: Exits the program

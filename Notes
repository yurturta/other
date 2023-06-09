Git


In my automatic jenkins job, launched daily, if there are no changes the git commit command returns 1. That will mark the build as failed. To solve this problem I use these two commands in my shell build step:

git add -A
git diff-index --quiet HEAD || git commit -m "Jenkins automatic update commit"

    the first will eventually add all unstaged files in the whole working tree (equivalent to git add --all);
    the second will perform the commit if and only if there are differences against the HEAD version of the working directory. If the git diff command has exit code zero then the git commit command is executed.


C# Programming + Git Command lines

* Static Properties Tests

--> Starting with Git command Lines
Learn Git Command Lines
https://git-scm.com/book/en/v2/Getting-Started-The-Command-Line
Help Online: https://freenode.net/ (Channels #git or #github)
https://www.git-tower.com/learn/git/faq/undo-last-commit


git add *
git rm * -f (force to remove)

git status
git status -s

git diff
git diff --staged
git diff --cached

git commit (without parameters, open a editor to write a commit message)
git commit -m "First Commit"

git rm --cached README

git rm log/\*.log
Note the backslash (\) in front of the *. This is necessary because Git does its own filename expansion in addition to your shell’s filename expansion. This command removes all files that have the .log extension in the log/ directory. Or, you can do something like this:

git rm \*~
This command removes all files whose names end with a ~.

* RENAME FILES AND ADD TO STAGE
git mv README.md README
OR
mv README.md README
git rm README.md
git add README

* COMMIT HISTORY (LOG)
https://git-scm.com/book/en/v2/Git-Basics-Viewing-the-Commit-History
git log
git log --stat
git log --since=2.weeks
git log -S "git rm"
git log -S function_name
git log --pretty="%h - %s" --author='Junio C Hamano' --since="2008-10-01" \
   --before="2008-11-01" --no-merges -- t/

* UNDOING (https://git-scm.com/book/en/v2/Git-Basics-Undoing-Things)
* See More in (https://git-scm.com/book/en/v2/Git-Tools-Reset-Demystified#_git_reset)
* Undo in Branches (https://git-scm.com/book/en/v2/Git-Branching-Branches-in-a-Nutshell#ch03-git-branching)
* Data Recovery (https://git-scm.com/book/en/v2/Git-Internals-Maintenance-and-Data-Recovery#_data_recovery)

$ git commit -m 'Initial commit'
$ git add forgotten_file
$ git commit --amend

TAGGING
$ git tag -a v0.1 -m "First version project"
$ git tag


1. Create a Repository from GitHub Website

2. git clone https://repository-url.git

3. git status
(Shows untracked files in working directory)
git add file
(Put file in staging area)

4. git commit -m "Commit message"

Local Repository:-
Working   -->  Staging   -->   Repository
Directory       Area         (.git folder)

|
|
v

Remote Repository:-
5. git push origin master (Push to remote repository)

---------------------------------------------------------
Git Branching:-

list all -> 
git branch -a

create branch -> 
git branch <branch-name>
git checkout -b <branch-name>

delete locally branch ->
git branch -d <branch-name>

delete remote  branch -> 
git branch origin --delete <branch-name> OR git branch origin: <branch-name>
# Fetch changes from all remotes and locally delete 
# remote deleted branches/tags etc
# --prune will do the job :-;
git fetch --all --prune
git fetch -p

switch to branch ->
git checkout <branch-name>


---------------------------------------------------
Git Tags:

git tag

git tag <tag-name(stable)/> <branch-name(master)/>
git tag <tag-name(unstable)/> <branch-name(develop)/>
git tag -a <tag-name(v0.1-alpha)/> -m "Release 0.1 (Alpha)" <id-hash>

git show <tag-name(v0.1-alpha)/>

git push origin <tag-name(stable)/>
git push --tags

git tag -d <tag-name(v0.2-alpha)/>
git push origin :<tag-name(v0.2-alpha)/>

------------------------------------------------------
Git Logs:

git log --oneline
git log --oneline --graph
git log --oneline --decorate
git log --stat
git reflog

------------------------------------------------------
GitHub Issues:

Labels, Milestones, and Issues.
Pull requests are a type of issue
Issues have #<number>
Example: #2 or #54

To close an issue simply type close #<number> in commit message
Example: git commit -m "..., close #<number>"

git push
---------------------------------------------------
##Git Flow:
-----------
###Feature:
git flow feature start <feature-name>

list ->
git flow feature

publish to remote ->
git flow feature publish <feature-name>

git push origin feature/<feature-name>

git flow feature finish <feature-name>

-----------------------------------------------------
Git Reset:

commited in master mistakenly
ok go to required branch by checkout and then
use git cherry-pick <commit-hash>
then go back to master branch
and reset -> soft, mixed, hard

git reset --soft <commit-hash>
-> have our files in staging area

git reset <commit-hash>
-> have our files in working directory(untracked)

git reset --hard <commit-hash>

git clean -df (directory, files)

Backup
git reflog
git checkout <commit-hash>
git log
git branch backup

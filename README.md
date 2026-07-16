# ai-based-sensor
An AI project solves a problem using data and machine learning algorithms rather than fixed, hardcoded rules. It typically goes through a standard lifecycle: defining the problem, gathering and cleaning data, selecting a model, training it, evaluating its performance, and deploying it into a live environment.Depending on your skill level and goals, AI projects generally fall into a few standard categories:Natural Language Processing (NLP): Building chatbots, summarizing large documents using Retrieval-Augmented Generation (RAG), or performing sentiment analysis.Computer Vision: Projects involving image classification, facial recognition, or autonomous vehicle simulations.Machine Learning & Predictive Analysis: Forecasting house prices, predicting stock market trends, or detecting credit card fraud.AI Agents: Multi-agent workflows that automate complex tasks like web research or content creation.For a curated list of top AI projects spanning different skill levels and domains:




















































































































































































































































































Experiment 1

git config --global user.name "YourName"
git config --global user.email "yourmail@example.com"

mkdir Exp1
cd Exp1
git init

echo "Hello Git" > file1.txt

git status

git add file1.txt

git commit -m "Initial Commit"

git status

git log
git log --oneline
git show <commit-hash>

------------------------------------------------------------------------------------------------------------------------------------------------
Experiment 2

Cloning the repo

navigate to the directory where you want to clone

git clone <repo_link>
cd repo_name
git remote -v
git pull origin main

Push changes to repo

mkdir Exp2
cd Exp2
git init

echo "project file">file.txt
git add .
git commit -m "first commit"

git remote add origin <link>
git remote -v
git branch -m main
git push -u origin main

--------------------------------------------------------------------------------------------------------------------------------------------------------------
Experiment 3

mkdir OriginalRepo
cd OriginalRepo
git init

echo "version1">file.txt
git add .
git commit -m "version1 added"

cd ..
git clone --bare OriginalRepo RemoteRepo.git
git clone RemoteRepo.git localrepo
git clone RemoteRepo.git devrepo

cd devrepo
echo "version2">>file.txt
git add .
git commit -m "second commit"
git push origin main

cd ..
cd localrepo
git fetch origin
git log origin/main --oneline
git diff main origin/main
git merge origin/main
git pull origin main

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Experiment 4

git branch
git branch feature-login
git checkout feature-login
echo "login credentials">file.txt
git add .
git commit -m "added login feature"

git checkout main
git merge feature-login
git branch -d feature-login

git checkout -b feature-conflict
echo "this is exp4">>file.txt
git add .
git commit -m "feature change"

git checkout main
echo "hello git">>file.txt
git add .
git commit -m "main change"

git merge feature-conflict
notepad file.txt   //resolve and make changes manually in the file
git add .
git commit -m "resolved conflicts"

git checkout -b feature-payment
echo "payment done">>file.txt
git add .
git commit -m "payment done"

git checkout main
echo "click Okay">>file.txt
git add .
git commit -m "main updated"
git checkout feature-payment
git rebase main

for rebase conflicts
git status
remove conflicts manualy
git rebase --continue

----------------------------------------------------------------------------------------------------------------------------------------------
Experiment 5

mkdir exp5
cd exp5
git init

echo "original content">file.txt
git add .
git commit -m "initial commit"

echo "temporary change">>file.txt
git status

git stash
git stash list

git checkout -b feature-login
git checkout main

git stash apply OR git stash pop
git status

git stash drop //to delete the stashed changes
git stash list

------------------------------------------------------------------------------------------------------------------------------------
Experiment 6

mkdir exp6
cd exp6
git init

echo "hello git">file.txt
git add .
git commit -m "initial commit"

git branch feature-login
git checkout feature-login
echo "login credentials">>file.txt
git add .
git commit -m "added login feature"

git push -u origin feature-login

git checkout main
git merge feature-login

git push origin main
git branch -d feature-login

---------------------------------------------------------------------------------------------------------------------------------------------
Experiment 7

for stashing it is same as experiment 5
mkdir exp7
cd exp7
git init

echo "version 1">file.txt
git add .
git commit -m "commit 1"

echo "version 2">file.txt
git add .
git commit -m "commit 2"

echo "version 3">file.txt
git add .
git commit -m "commit 3"

git log --oneline
git reset --hard HEAD~1
git reset --soft HEAD~1
git reset HEAD~1

git log --oneline
git rebase -i HEAD~3

git log --oneline
git revert HEAD
git log --oneline

git tag v1.0
git tag
git tag -a v2.0 -m "release version 2.0"
git tag
git push origin v1.0
git push --tags

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Experiment 8

mkdir exp8
cd exp8

echo "version1">file.txt
git add .
git commit -m "commit 1"

echo "version2">file.txt
git add .
git commit -m "commit 2"

echo "version3">file.txt
git add .
git commit -m "commit 3"

echo "version4">file.txt
git add .
git commit -m "commit 4"

echo "version5">file.txt
git add .
git commit -m "commit 5"

echo "version6">file.txt
git add .
git commit -m "commit 6"

git log -5
git log --oneline -5

git log -n 5 --pretty=format: "%h-%an,%ar:%s"

-----------------------------------------------------------------------------------------------------------------------------------------------------
Experiment 9

mkdir exp9
cd exp9
git init

echo "initial">file.txt
git add .
git commit -m "initial commit"

git checkout -b bugfix
echo "fix1">>file.txt
git add .
git commit -m "bug fix1"

echo "fix2">>file.txt
git add .
git commit -m "bug fix2"

git log --oneline
git cherry-pick <commid id>
git cherry-pick <start-commit>^..<end-commit>

----------------------------------------------------------------------------------------------------------------------------------------------------------
Experiment 10

mkdir exp10
cd exp10
git init

git config user.name "JohnDoe" 
git config user.email "john@example.com" 

echo "Version 1" > file.txt 
git add . 
git commit -m "Commit 1" 

echo "Version 2" >> file.txt 
git add . 
git commit -m "Commit 2" 

echo "Version 3" >> file.txt 
git add . 
git commit -m "Commit 3" 
 
git log -5 
 
git log --author="JohnDoe" 
 
git log --since="2026-06-016" 
 
git log --until="2026-06-17" 
 
git log --author="JohnDoe" --since="2026-06-16" --until="2026-06-17" 

git log --author="JohnDoe" --since="2026-06-16" --until="2026-06-17" –oneline 

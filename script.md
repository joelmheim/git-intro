Outline:

* Intro and overview of the topics
* Session Mechanics
* About me
* Introduction to git
  * History
  * Good SC practices
  * Common commands
  * Other useful commands
* Demo
  1. git init
  1. git status
  1. vim firstfile.txt
  1. git status
  1. git add firstfile.txt
  1. git status
  1. git commit -m "My first file"
  1. vim secretfile.secret
  1. git status
  1. create .gitignore with secret file
  1. git status
  1. git add .gitignore
  1. git status
  1. git commit -m "git ignore"
  1. git status
  1. create repo on github (gitdemoproject)
  1. git remote -v
  1. git remote add origin git@github.com:Statoil/gitdemoproject.git
  1. git push -u origin master
  1. Simulate second contributor
     1. git clone git@github.com:Statoil/gitdemoproject.git (show default naming)
     1. rm -rf gitdemoproject
     1. git clone git@github.com:Statoil/gitdemoproject.git secondcontributor
     1. vim secondfile.txt
     1. git status
     1. git add secondfile.txt
     1. git status
     1. git commit -m "The second file"
     1. git status
     1. git push
  1. Back to original contributor
     1. git status
     1. git pull
  1. Both change same file, automerge
     1. First contributor adds line above
     1. Second contributor adds line below
     1. Second: git status, git add, git commit, git push
     1. First: git status, git add, git commit -> error
     1. First: git pull, automerge
     1. First: git status
     1. First: git push
  1. Both change the first file in a different way, conflict
     1. First contributor changes middle line
     1. Second: git pull
     1. Second contributor changes middle line
     1. Second: git status, git add, git commit, git push
     1. First: git status, git add, git commit -> error
     1. First: git pull, manual failure
     1. First: git status
     1. First: manually edit file
     1. First: git add
     1. First: git commit -m "Merged manually"
     1. First: git push
  1. Demonstrate git stash by repeating the conflict scenario but first contributor stashes his changes in stead of merging.
     1. First contributor changes middle line
     1. Second: git pull
     1. Second contributor changes middle line
     1. Second: git status, git add, git commit, git push
     1. Second alerts first about change
     1. First: git stash, git pull
     1. First: git status
     1. First: git stash pop, merge conflict
     1. First: manually edit file
     1. First: git status
     1. First: git add
     1. First: git commit -m "Merged manually"
     1. First: git push

* Explain workspace / index / local repo / remote repo
  * Use cheat sheet
* Explain distributed version control vs centralized version control
  * Back to presentation
* Go through useful git shortcuts/aliases
* List of resources and further reading
*
* Multiple central repos github / gitlab / deploy to heroku / digitalocean
* Git fetch
* Cherry pick commit
* Git-flow
* Interactive cheat sheet
* Advanced problemsolving flowchart
* git add -p

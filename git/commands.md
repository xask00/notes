
## Concepts
Branch: for human: a branch is a “directed acyclic graph of development” rather than a line
        for machine: a branch is just a SHA1sum of the commit at the tip, since its a graph the history is the graph traversal in reverse
fast-forward: when merging if possible just move the "HEAD" pointer and do not create a "merge commit"
            example ?
            happens a lot when you are working on local repo and 

2-way merge: a merge algorithm: only diff 2 files and try to merge
3-way merge: a merge algorithm: diff the 2 files, and also diff 2 files against common original copy
             a lot of decisions can be automatically done by looking at common ancestor.        
            https://www.drdobbs.com/tools/three-way-merging-a-look-under-the-hood/240164902
            diff3 my old you



### working area
### staging area

## FAQ
git fetch vs git pull

git fetch - download changes from remote server and stores locally but do not merge then with your current branch, its "safe" as it does not "change" anything.
            It only changes .git/ and affects remotes/origin/master

git pull - downloads remote changes + merge it with local changes, can cause merge conflict,
           hence should only be done with clean local copy, or use git stash

        pull != fetch + merge.
         "I just fetched a change where only a remote branch pointer changes, and merge refuses to do anything. 
         pull fast-forwards my tracking branch
Usually what you want is:
  git pull --ff-only

## Internals  
Tree object: stores group of files or a single filename
Blob object: binary object
commit object: link to a tree object

git stores full files not diffs
git uses pack files, when you do a git gc to store diff to save space.
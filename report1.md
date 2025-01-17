# Daily Live Report (6 Months)
**Github Workshop Report**  
**Date:** 15/01/2025  
**Start Time:** 7:00 PM  
**End Time:** 9:00 PM

---

### Learnings from the Workshop:

I have learned the following things from this workshop:

. **Version Control System & Git:**
   - I learned about version control system
     
A version control system is a tool that keeps track of these changes for us, effectively creating different versions of our files. It allows us to decide which changes will be made to the next version (each record of these changes is called a commit), and keeps useful metadata about them. The complete history of commits for a particular project and their metadata make up a repository. Repositories can be kept in sync across different computers, facilitating collaboration among different people.
Version control also allows many people to work in parallel.

**Setting up git:-**
When we use Git on a new computer for the first time, we need to configure a few things. Below are a few examples of configurations we will set as we get started with Git:

   - our name and email address,
   - what our preferred text editor is,
   - and that we want to use these settings globally (i.e. for every project).


**Git Help and Manual**
- $ git config -h
- $ git config --help
 
**Creating repository**
- $ git init is used to create and initialize the repository

  **Tracking changes**
  1. If we check the status of our project a Git tells us that it’s noticed the new file:
    
  - $ git status
``` bash
On branch main

No commits yet

Untracked files:
   (use "git add <file>..." to include in what will be committed)

	file

nothing added to commit but untracked files present (use "git add" to track)
```

The “untracked files” message means that there’s a file in the directory that Git isn’t keeping track of. We can tell Git to track a file using git add:
- $ git add file-name
``` bash
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

	new file:   filename
```

Git now knows that it’s supposed to keep track of guacamole.md, but it hasn’t recorded these changes as a commit yet. To get it to do that, we need to run one more command:
BASH

- $ git commit -m "give any message"
 ```bash
[main (root-commit) f22b25e] 
 1 file changed, 1 insertion(+)
 create mode 100644 filename

 ```
 Push the file into repo
- $ git origin origin main
   
If we want to know what we’ve done recently, we can ask Git to show us the project’s history using git log:


- $ git log

  **Staging area**
  Git as taking snapshots of changes over the life of a project, git add specifies what will go in a snapshot (putting things in the staging area), and git commit then actually takes the snapshot, and makes a permanent record of it (as a commit). If you don’t have anything staged when you type git commit, Git will prompt you to use git commit -a or git commit --all, which is kind of like gathering everyone to take a group photo! However, it’s almost always better to explicitly add things to the staging area, because you might commit changes you forgot you made.


 (![image](https://github.com/user-attachments/assets/639861d6-1306-49ab-aaf7-1a2f81d5fa62)


**Conflicts**
Conflicts occur when two or more people change the same lines of the same file.

# Contact Module frappe     

 # DATE :-22/01/2025

**Start time:-8:30 am**


Issue:-When i push the file from terminal to repo this error occurs

```bash
bc12@debian:~/Documents/Manvir/Daily-Dairy$ git push origin main
To https://github.com/manvirsinghh/Daily-Dairy.git
 ! [rejected]    	main -> main (non-fast-forward)
error: failed to push some refs to 'https://github.com/manvirsinghh/Daily-Dairy.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
```

**Solution** :-
```bash
git pull --rebase origin main
```
Rebasing applies your local changes on top of the latest remote commits. 
When we rebase a branch, Git moves your changes (commits) on top of another branch
Paused at:11:12am

TASK:-Include bootstrap in web page 
Start time:-4:30pm


When i try to put files on github through terminal i get an 
ERROR:-abc12@debian:~/Documents/Manvir/fruitversion2$ git push origin main
``` bash

To https://github.com/manvirsinghh/html_css_js.git
 ! [rejected]    	main -> main (fetch first)
error: failed to push some refs to 'https://github.com/manvirsinghh/html_css_js.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

```



Sir, i got this solution 
- 1 Pull the latest changes from the remote repository:
First, ensure that your local branch is up to date with the remote main branch. Since you've already resolved conflicts, this should merge the changes properly:
```bash
git pull origin main --rebase
```
- 2 Resolve any conflicts (if necessary):
If there are any new conflicts during the pull, you'll need to resolve them just like before. After resolving conflicts, use git add to stage the resolved files.
- 3Push your changes:
Once the pull is successful and you've resolved any conflicts, push your changes:
I have tried these but not get solution
End time:-6:07pm
Task:-Prepare github tutorial workshop and do some modifications
Start time:-6:08pm
End time:-7:55pm
Break:7:56 pm to 8:27 pm to have a dinner 
Start time:-8:28pm
Solve error of pushing the code
End time:-11:45pm



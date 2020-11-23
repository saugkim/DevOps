GIT basic of the basic

| bit confusing between main and master(after github main branch)
| echo "# sphinx" >> README.md  
| git init  
| git add README.md  
| git commit -m "first commit"  
| git branch -M main  
| git remote add origin https://github.com/saugkim/sphinx.git  
| git remote add origin git@github.com:saugkim/sphinx.git  

| git push -u origin main  

| 
| // add and remove remote repo  
| git remote add origin  
| git remote rm origin  
| 
| // delete branch locally  
| git branch -d localBranchName  
| 
| // delete branch remotely  
| git push origin --delete remoteBranchName  
| 
| // delete file and folder in remote
| git rm file
| git rm -r folder
| git commit -m 'message'
| git push -u origin main
| 
| //If you want to delete a file from remote only
| git rm --cached file
| git commit -m 'message'
| git push -u origin branch
|

| https://readthedocs.org/projects/sphinx/downloads/pdf/master/
| https://docs.readthedocs.io/en/stable/intro/getting-started-with-sphinx.html
| https://towardsdatascience.com/5-reasons-to-use-yaml-files-in-your-machine-learning-projects-d4c7b9650f27


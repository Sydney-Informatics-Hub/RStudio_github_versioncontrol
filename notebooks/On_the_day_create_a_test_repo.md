---
fig-cap-location: top
from: markdown+emoji
editor: 
  markdown: 
    wrap: sentence
---

# **Create and update a new repository on GitHub**

::: questions
### **Questions** {.unlisted}

- How to  create your test repository? 
- How to clone the new repo to local machine?
- How to push the local changes back to github?
:::

### **Create a new repository**
For todays code-along session, you will need a test repository (or repo) on GitHub  
- Go to `https://github.com/`  
- Log in (if not logged in already)  
\
- Click on the `+` symbol on the right hand top corner  
- Select `New repository`
<img src="../fig/create_a_repo.png" style="width:120%; height:150%;"/>

This opens a new form as shown below. Please select the following options:  
- **Repository template**: No template  
- **Repository name**: `myrepo_masterclass_RStudio_github` or any other name of your choice  
- **Description**: `Repository for testing my Git/GitHub setup` or similar    
- Choose `Public`    
- Initialize this repository by checking the `Add a README file` option  
- Click on <img src="../fig/create_repo.png" style="width:20%; height:20%;"/>
<img src="../fig/new_repo_fillin_parameters.png" style="width:100%; height:80%;"/>
This creates a new repository called `myrepo_masterclass_RStudio_github` or whatever name you have provided
\
\

### **Clone the new repository to local machine**
- Click the big green button that says <img src="../fig/code.png" style="width:15%; height:15%;"/>  
- Copy the clone URL to your clipboard  
- Since we have created a PAT for HTTPS protocol , copy the HTTPS URL as shown below.
<img src="../fig/HTTPS_protocol_URL.png" style="width:100%; height:100%;"/>  

and type the following code on your terminal:  

`git clone HTTPS_URL`  
e.g. `git clone myrepo_masterclass_RStudio_github`

``` default
~/master_class % git clone https://github.com/Sydney-Informatics-Hub/myrepo_masterclass_RStudio_github.git
Cloning into 'myrepo_masterclass_RStudio_github'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (3/3), done.
```

I have named my repo as `myrepo_masterclass_RStudio_github`. Please do a few checks with the local copy of the repos

Make this new repo your working directory, list its files, display the README, and get some information on its connection to GitHub:

-   Make this new repo your working directory `cd myrepo_masterclass_RStudio_github`
-   list all files `ls`
-   Display the README `head README.md`
-   Get some information on its connection to GitHub `git remote show origin`

### **Make a local change, commit, and the push the changes**
- Add a line to README and verify that git notices the change  
- Open the README file with a text editor and add some words like *"I am adding a line in my local copy"*  
Go back to your terminal and type the command below:  

``` default
git status
```

``` default
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
    modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
```

Add the file with changes - README.md for commit step:

``` default
git add README.md
git commit -m "A commit from my local computer"`
[main 306de6f] A commit from my local computer
 1 file changed, 1 insertion(+)
```
> **Note** you always have to include a message with your commit. 

Push the changes to github `git push`.

The local changes should now be reflected into the `README.md` file on the github repo.
Please check them.

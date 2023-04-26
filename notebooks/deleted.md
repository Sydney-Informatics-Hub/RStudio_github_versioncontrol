
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


### **Confirm the local change propagated to the GitHub remote**
Go back to the browser. I assume we’re still viewing your new GitHub repo.

**Refresh**

You should see the new "I am adding a line in my local copy"  in the README.

The local changes should now be reflected into the `README.md` file on the github repo.
Please check them.

> Note that if `git push` asks for your GitHub username and password, you should use your
`Personal Access Token` as the password, not your GitHub password.

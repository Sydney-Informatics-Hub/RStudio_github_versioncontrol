---
fig-cap-location: top
from: markdown+emoji
editor: 
  markdown: 
    wrap: sentence
---

# **Is git connected to github?**

::: questions
### **Questions** {.unlisted}

-   Can you connect git and a remote git server such as github?
:::

You need to confirm that you can clone a repository from GitHub and establish two-way communications between the local git and the github - This is called `pull` and `push`.

When communicating with a remote server, git has two available protocols - HTTPS and SSH - each of which requires different credentials.

We will discuss how you can setup your credentials for the HTTPs protocol.

## **Personal access token for HTTPS**

**Personal access token (PAT)** is required by a remote git server such as github to confirm a users credentials.

> **Please note** that from 2021-08-13 GitHub is no longer accepting account passwords when authenticating Git operations.
> You need to add a **PAT (Personal Access Token)** instead, and you can follow the below method to add a PAT on your system.

### Create Personal Access Token on GitHub

Step 1 - Open GitHub and log in with your credentials.

Step 2 - Click on the **Setting** menu.

Step 3 - From the Setting menu click on **Developer Settings**

Step 4 - From the Developer Settings menu, click on **Personal access token**

Step 5 - From the Personal access token, click on the **Generate new Token button**.

Step 6 - Now fill up required details (select "repo", "user", and "workflow"). And then click on the **Generate Token** button.

Step 7 - After that, a new token has been generated. Copy that generated token and use this token to access Git with username and token.
It will be something like ghp_sFhFsSHhTzMDreGRLjmks4Tzuzgthdvfsrta.

You will need it the next time when a git operation asks for your password.

Now follow the below method based on your machine:

#### WindowsOS

Open **Control Panel** → **User Accounts** → **Manage your credentials** → **Windows Credentials**.

It will show all generic credentials. Find your GitHub URL and click on that. Now click on the edit button. And then add the personal access token generated from GitHub into the password field. And click on the Save button.

If you don't find git:https://github.com → Click on **Add a generic credential** → Internet address will be git:https://github.com and you need to type in your username and password will be your GitHub Personal Access Token → Click Ok

#### MacOS

Click on the Spotlight icon (magnifying glass) on the right side of the menu bar.
Type Keychain access then press the Enter key to launch the app → In Keychain Access, search for github.com → Find the internet password entry for github.com → Edit or delete the entry accordingly

#### Linux-based OS

For Linux, you need to configure the local GIT client with a username and email address:

```
$ git config --global user.name "your_github_username" 
$ git config --global user.email "your_github_email" 
$ git config -l
```

::: keypoints
### **Key points** {.unlisted}

If you're a new GitHub user and using HTTPS, you might be asked for your username and password.
<br>**Note** Use you PAT and not your login password.
:::

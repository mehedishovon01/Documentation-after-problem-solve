# "Git - remote: Repository not found"
The error message _"remote: Repository not found"_ is a common issue in _Git_ when trying to push or clone a repository. This problem can often be resolved by adjusting the repository's remote URL.

## Solutions
There are multiple ways to solve this issue, but we will provide a professional and systematic approach for both Windows and Linux users.

### For Windows

#### Solution 1: Manually Edit the Config File
User can edit the _config_ file manually like,

* Go to .git folder
* Open '_config_' file using any kind of editor
* Change the URL from https://github.com/mehedishovon01/repo_name.git to https://mehedishovon01:PERSONAL_ACCESS_TOKEN@github.com/mehedishovon01/repo_name.git
* Save and close the config file.

Done! the problem should be resolved, and you should be able to push to or clone the repository.

### For Linux

#### Solution 2: Remove and Add Remote URL
User can edit the _config_ file using the terminal like this.

We have to remove the existing url if already created. So, the command is,

    git remote rm origin

Now, add a new remote URL with your Personal Access Token. And run the following command,

    git remote add origin https://mehedishovon01:PERSONAL_ACCESS_TOKEN@github.com/mehedishovon01/REPO_NAME.git

Now, to push the current branch and set the remote as upstream, use

    git push -u origin main

##### _Note: Replace PERSONAL-ACCESS-TOKEN with your actual GitHub Personal Access Token and REPO-NAME with the name of your repository for both solutions._

<br/>

### What is done there actually?
This is firstly remove the existing URL and then add a new url where add _PERSONAL ACCESS TOKEN_ against the _username_.

These steps ensure that you have the correct remote URL configured. You should now be able to perform Git operations without encountering the "remote: Repository not found" error.

<br />

## Conclusions
By following these steps, you can effectively resolve the "Git - Remote: Repository Not Found" issue, ensuring a smooth Git workflow with your remote repository.
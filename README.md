# doi-exercise

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

This is a repository to train making a GitHub repository (project, data, code) public using a sandbox and following [instruction](https://coderefinery.github.io/github-without-command-line/doi/) which are part of this repository by coderefinery: https://coderefinery.github.io/github-without-command-line/doi/ (CC-BY 4.0).
The process is documented along these instructions and additional explanations are added along the way. 

As I am anyway doing this exercise right now, I decided to leave some comments target to others who 
- plan or have to do the same
- have already create and contributed to at least a simple GitHub repository
- have seen a LICENSE and .gitignore file before
- but are not very experienced with GitHub repositories so far over all.

Maybe this is useful for anybody.
Please note, links used here are as of January, 3rd, 2024 and might not be updated thereafter.

## Step 1 - Create an example repository

### Create the repository with a README.md
In the first step this public repository was created with a description ("About") and this [`README.md file`](./README.md):

![screenshot of the repository](./images/doi-exercise-screenshot.png)

### .gitignore
I added a [`.gitignore`](./\.gitignore) file to avoid pushing files into this public repository which are not relevant for its content. For this, I selected the Visual Studio `.gitignore` version.  

I also add the `.DS_Store` file to the repository's `.gitignore` file for macOS.  

### LICENSE & references
Moreover, I added a [LICENSE](./LICENSE) and referenced the instructions I used for this exercise in this README file - in particular including the repository in which these instructons reside.  
This was done, because the coderefinery repository has a CC-BY 4.0 license and, at least for this repository, I did not find another citation.  
Therefore, I want to ensure proper referencing and enable others to reuse content of this repository by knowing about the license.  

#### Adding a LICENSE
In my work, I often use the CC-BY 4.0 license. This license is not provided as a choice by GitHub when setting up the repository. Therefore, I simply add a text file named LICENSE into the root of my repository and copy the text of the CC-BY 4.0 license into it.  
In addition, to make it as easy as possible for others who might want to reuse any content of my repository, I add a CC_BY 4.0 badge right at the beginning of the repository's README file: 

```
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
```

**CC-BY 4.0**:
tbc

**root**:
tbc

### Upload example data
There are different ways to add data to a GitHub repository. For example, we can use the `Add file` button in the browser or adding a file to a local cloned version of the repository followed by the respective `git add`, `git commit -m "Added my_file."`and `git push`commands.
Also, you can just drag an drop a file in [VS Code](https://code.visualstudio.com/) into the directory structure of your repository of choice.

Here, I cloned the repository and continued as described above. If not just cloned before the following steps are conducted, it makes sense to first pull all remote changes: `git pull`. As I protected my main branch, at least in this example, I first created a branch for this (`git switch -c upload_example_data`) performed the different steps and pushed as follows: (`git push --set-upstream origin upload_example_data`).

Eventually, after checking that everything is as expected, I do the pull request (PR) and merged the upload_example_data branch into the main branch and eventually delete the upload_example_data branch.

## Step 2
As described [here](https://coderefinery.github.io/github-without-command-line/doi/), I headed over to the Zenodo Sandbox Instance. First, I logged into the Sandbox Instance of Zenodo which needs access to your public repository. If this is with another organization it will need access to the respective public repositories as well. You or the respective owner have to decide on this.  

Next, I activate it at Zenodo (sandbox) by selecting it in the overview of public repositories (set to "on").
After reloading the page, it should be shown under "Enabled Repositories".

## Step 3

## Step 4

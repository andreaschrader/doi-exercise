# doi-exercise

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

## DOI badge

**At the Zenodo sandbox instance:**  
[![DOI](https://sandbox.zenodo.org/badge/738481995.svg)](https://sandbox.zenodo.org/doi/10.5072/zenodo.19273)  

**At Zenodo:**  
[![DOI](https://zenodo.org/badge/738481995.svg)](https://zenodo.org/doi/10.5281/zenodo.10475392)

<br/>

Please note, most release versions of this repository were used for tests.

---

## Description
This is a repository to train making a GitHub repository (project, data, code) public using a sandbox and following [instruction](https://coderefinery.github.io/github-without-command-line/doi/) which are part of this repository by coderefinery: https://github.com/coderefinery/github-without-command-line (CC-BY 4.0).
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
Moreover, I added a [LICENSE](./LICENSE) and referenced the instructions I used for this exercise in this README file - in particular including the repository in which these instructions reside.  
This was done, because the coderefinery repository has a CC-BY 4.0 license and, at least for this repository, I did not find another citation. Therefore, I want to ensure proper referencing and enable others to reuse content of this repository by knowing about the license.  

#### Adding a LICENSE
In my work, I often use the CC-BY 4.0 license. This license is not provided as a choice by GitHub when setting up the repository. Therefore, I simply add a text file named LICENSE into the root of my repository and copy the text of the CC-BY 4.0 license into it.  
In addition, to make it as easy as possible for others who might want to reuse any content of my repository, I add a CC_BY 4.0 badge right at the beginning of the repository's README file: 

```
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
```

**CC-BY 4.0**:  
This is one of the Creative Commons licenses. Creative Commons is an international nonprofit organization enabling "sharing of knowledge and culture in the public interest" (https://creativecommons.org/mission/). In brief, [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/) allows you to share and adapt the material for any purpose given that you provide appropriate attribution and do not add additional restrictions as described [here](https://creativecommons.org/licenses/by/4.0/) (see [here](./LICENSE) for more details).  

**root**:  
This is the top-level directory of a repository. All other directories are sub-directories of it.


### Upload example data
There are different ways to add data to a GitHub repository. For example, we can use the `Add file` button in the browser or adding a file to a local cloned version of the repository followed by the respective `git add`, `git commit -m "Added my_file."`and `git push`commands.
Also, you can just drag an drop a file in [VS Code](https://code.visualstudio.com/) into the directory structure of your repository of choice.

Here, I cloned the repository and continued as described above. If not just cloned before the following steps are conducted, it makes sense to first pull all remote changes: `git pull`. As I protected my main branch, at least in this example, I first created a branch for this (`git switch -c upload_example_data`) performed the different steps and pushed as follows: (`git push --set-upstream origin upload_example_data`).

Eventually, after checking that everything is as expected, I do the pull request (PR) and merged the upload_example_data branch into the main branch and eventually delete the upload_example_data branch.

## Step 2 - Activating the GitHub repository at Zenodo
As described [here](https://coderefinery.github.io/github-without-command-line/doi/), I headed over to the Zenodo Sandbox Instance. First, I logged into the Sandbox Instance of Zenodo which needs access to your public repository. If this is with another organization it will need access to the respective public repositories as well. You or the respective owner have to decide on this.  

Next, I activate it at Zenodo (sandbox) by selecting it in the overview of public repositories (set to "on").
After reloading the page, it should be shown under "Enabled Repositories".

**sandbox**:  
A sandbox provides an isolated test environment in which the user can act without affecting the respective application or platform.

**Zenodo**:  
An open repository minting a doi for each submission. It is operated by [CERN](https://home.cern/) and developed within the [European OpenAIRE programme](https://www.openaire.eu/).

**DOI**:  
Digital Object Identifier, a persistent identifier usable by humans and machines.

## Step 3 - Publish a release version of the repository at GitHub

Going back to the doi-exercise repository, I selected `Releases` in the right sidebar and `Create a new release` on the next page.

Choose a tag: Here you can enter a version for your repository. For continuous development carefully select the format of the selected version.
I chose `v1.0`.  

Target: This is the branch of the repository selected for the release. 
I chose `main`.

Add a `Release title` and optionally a more detailed descriptions including differences e.g to a previous release in subsequent releases can be added.

Eventually conclude with `Publish release`.

I changed back to Zenodo (sandbox) and refreshed the page. In my case the Releases were directly updated:

![zenodo-release-screenshot](./images/zenodo-releases-screenshot.png)

## Step 4 - Add a DOI badge to the README at GitHub

A badge at the begin of the README of the respective repository can directly guide you to the citation at Zenodo and displays the doi (here it is only the sandbox version for the test).

To obtain the code that you have to insert into the README.md file, go to zenodo (sandbox) click on the badge for the repository and copy the line for `Markdown` - see also at the begin of this repository.

After committing the changes, it will be displayed like [here](https://github.com/andreaschrader/doi-exercise/tree/main#DOI-badge).

## Further optional steps

With this, your project is citable and you obtained a persistent identifier for it. However, you might want to add specific metadata which could not be captured by Zenodo or was not available from your GitHub account. You might also want to support the user with an easily extractable citation or update the version at Zenodo upon a new release. Below are some thoughts and suggestions on a supportive citation file.

## CITATIONS and other (transferred) metadata

I would like to clearly reference the instruction I followed and along which I wrote the text in this [README](./README.md):  
https://coderefinery.github.io/github-without-command-line/doi/  

The instructions worked smoothly in my hands. Thanks to the authors!  

**cff**:  
In addition to the persistent identifier, a citation file can be added to the root of the repository. Following the respective [GitHub CITATION.cff](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-citation-files) documentation, a respectively created cff file in the root [can be considered by Zenodo](https://github.com/citation-file-format/citation-file-format/issues/374) in order to read proper metadata with respect to authors, affiliations and e.g. licenses and is displayed in the right side-bar at GitHub.  

Here, I selected from the options described in the [citation file format (cff) repository](https://github.com/citation-file-format/citation-file-format/tree/main)'s (doi: 10.5281/zenodo.1003149) [schema-guide.md](https://github.com/citation-file-format/citation-file-format/blob/main/schema-guide.md) to create a [`CITATION.cff`](./CITATION.cff) file for this repository. Note, currently, only the types `software` and `dataset` can be selected and if non is selected, `software` is the default.

**zenodo.json**:  
However, if a [`.zenodo.json`](./\.zenodo.json) file was created as well, according to the [Zenodo FAQ on GitHub for CITATION.cff](https://help.zenodo.org/faq/#github), the `.zenodo.json metadata` is used for the Zenodo record.

The eventually used `.zenodo.json` in this repository was inspired by [this repository](https://github.com/zenodraft/metadata-schema-zenodo), keys were selected from [this file](https://github.com/zenodo/zenodo/blob/f091af8f2d0bfac2fdaf53222160f8e037d5a0e6/zenodo/modules/deposit/static/json/zenodo_deposit/deposit_form.json) and upon inspecting the metadata show in the Zendodo sandbox instance upon deposition.

## Experiences

**Mandatory keys - .zenodo.json:**  
As derived from this [file](https://github.com/zenodo/zenodo/blob/f091af8f2d0bfac2fdaf53222160f8e037d5a0e6/zenodo/modules/deposit/static/json/zenodo_deposit/deposit_form.json) the following keys are mandatory for a valid `.zenodo.json` file:

- publication_date
- title
- creators
- description
- access_right  
  Depending on the respective access rights additional keys are required:
  - open:
    - license
  - closed 
  - embargoed: 
    - license
    - embargo_date
  - restricted:
    - access_contitions
  
**"references" key:**. 
As I intended to cite relevant references used in this repository, a reference section was added to the [CITATION.cff file](./CITATION.cff). However, when creating a new release, the references were not extracted by zenodo from the CITATION.cff file.  

To solve this, the `CITATION.cff` file was converted to a .zenodo.json file using the [cffconvert tool](https://github.com/citation-file-format/cffconvert) (DOI 10.5281/zenodo.1162057).  

During conversion to a `.zenodo.json` file using cffconvert these were lost. The README of the repository also states that references are currently not converted.  

Therefore, a `.zenodo.json` file was created manually.  

>***Solution***  
>
>When adding a reference at zenodo, one string per reference is required. The only way to pass references in my hands was by creating references as strings beforehand and passing multiple references as a list of strings to zenodo.  
> 
>Optional: A reference string could be created from the CITATION.cff section.  
>
>The exemplary .zenodo.json file created for this repository as indicated above can be found [here](./\.zenodo.json).

**.zenodo.json "description" key:**

Some test were done to derive from where zenodo currently derives the content for the description field.
When no description is provided otherwise, in my hands the description of the respective release was displayed.
However, when a description is provided in the .zenodo.json file in the root of the repository at submission, this information is overwriting the release description.

>***Solution*** 
>
>I chose here to create a description in my .zenodo,json file which also contains a funding statement and thereby ensures that this is kept upon submission.
>
>If the description of the release should be added and an own .zenodo.json file is used, it needs to be added to this description.

**.zenodo.json "notes" key:**

The message provided in the CITATION.cff file was extracted by zenodo as a note.
When a .zenodo.json is used, this file is used instead of the CITATION.cff file if both are in the root.  

>***Solution***
>
>Information for the note field can be passed in the .zenodo.json file with the "notes" key.

**"type" key**  

The type of a Github repository submitted to Zendodo using the CITATION.cff file is per default "software". The only other option, currently, seems to be "dataset" leaving little room for differentiation.  

>***Solution***  
>
>This can be differentiated more when using the "type" key in the .zenodo.json file.

**.zenodo.json "references.scope" key:**

When providing specific references, it might be desireable to indicate for what these were used.

>***Solution***  
>
>Information on the individual references can be provided via the "scope" key in the "references" section of the `CITATION.cff` file. If both files are kept in the root of the repository, the .zenodo.json file is used for the Zenodo publication and the CITATION.cff file for the citation within the GitHub repository and holding additional information e.g. on the scope of a reference with respect to the respective repository.

<br/>

---

If chunks of text and collected information above were supportive for you, please ***cite and star ⭐ this repository*** :smile:  

Thanx!  

<br/>

---

Andrea Schrader - 01.2024  
Academic Expert in Data Science for CEPLAS at University of Cologne, Germany  
orcid: https://orcid.org/0000-0002-3879-7057  
  
[CEPLAS](https://www.ceplas.eu), the Cluster of Excellence on Plant Sciences, is funded by the Deutsche Forschungsgemeinschaft (DFG, German Research Foundation) under Germany's Excellence Strategy, EXC-2048/1'  

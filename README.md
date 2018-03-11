## Git Branching Policies:
# Git Flow

## Introduction:
If you are new to git and/or to repository management, you have probably never heard of branching policies or what a branching policy is.

A branching policy is a set of rules which help organise, keep everything in your repository working as intended, make parallel development easier and make solving any issue related to project structure easy to solve.

In this page we are going to talk about the 'Git Flow' model, which was depeloped from the [initial proposal by Vincent Driessen](http://nvie.com/posts/a-successful-git-branching-model/).

***

## Basic Structure:

### Master & Develop

The Git Flow workflow consists of two main branches: ```master``` and ```develop```.

These two branches will be existent from the start of the development and should not be worked on directly most of the time, instead, modifications and new features may be developed in separate branches (named with the prefix ```feature```) and, after they are finished and verified, merged into ```develop```.

In ```develop``` only core features and improvements on already existing ones should be developed.

### Features

Each new behaviour of our program should be developed in separate branches which branch off of ```develop```. These branches are called ```feature``` branches.

These branches are created to 

Once the feature is completed, it should be tested and validated before being merged with the main ```develop``` branch.

### Releases

Whenever we consider the state of the development ready for a certain release, a new branch named after the release should be created. From there the release must be validated, and any issues found should be fixed and commited to said release aswell.

Once the release is considered valid, it is merged into the ```master``` branch and tagged with its version number so that it can be easily tracked if needed. At the same time, all changes done on the ```release``` branch shall, aswell, be merged into ```develop``` for further development.

### Hotfixes

If by any circumstances an already released (live) build of our software have any critical issue that requires an urgent fix, a new branch called ```hotfix``` may be branched from said release (which can be found in the correspondent tag in the ```master``` branch).

In this new branch the issue must be fixed and validated before merging it back to both ```master``` -- Updating the already released build -- and ```develop``` -- To include the fix in future releases --. It should be noted that merging the fix back to the ```release``` branch is not needed, since that branch may very well be outdated by the time the hotfix rolls out, and should not be used in the development of the software after the release is completed anyway.


```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/marc094/GitFlowClass/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.

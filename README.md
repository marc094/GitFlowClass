## Git Branching Policies:
# Git Flow

## Introduction:
If you are new to git and/or to repository management, you have probably never heard of branching policies or what a branching policy is.
A branching policy is a set of rules which help organise and make it easy to keep everything in your repository working as intended.

In this page we are going to talk about the 'Git Flow' model, which was depeloped from the [initial proposal by Vincent Driessen](http://nvie.com/posts/a-successful-git-branching-model/).

***

### Basic Structure
The Git Flow workflow consists of two main branches: ```master``` and ```develop```.
These two branches will be existent from the start of the development and should not be worked on directly, instead, modifications and new features will be developed in separate branches (named with the prefix ```feature```) and, after they are finished and verified, merged into them.
Whenever we consider the state of the development ready for a certain release, a new branch named after the release is created. From there the release must be validated, any issues found should be fixed and commited to said release aswell.
Once the release is considered valid, it is merged into the ```master``` branch and tagged with its version number so that it can be easily recovered if needed. At the same time, all changes done to the release while on the ```release``` branch shall be merged into ```develop``` for further development.


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

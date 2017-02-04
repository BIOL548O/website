---
title: "Installation"
subtitle: "getting your software ready for class"
author: "Andrew MacDonald"
---


## Installing software

In this course, we're going to use open-source software to learn how to manage and share data. Our hope is to provide you with a basic level of comfort with all of these tools, which you can use in your future projects!

You will need five things during this course:

* a laptop
* git
* a GitHub account
* R
* Rstudio (an IDE for R)

Please see installation instructions below for all the different software tools you need. These are modified from several sources, mostly from [Jenny Bryan's](http://www.stat.ubc.ca/~jenny/) excellent [STAT545 website](http://stat545-ubc.github.io/)


## Git and Github

As you work on your data project, you will be creating a well-organized directory for sharing your project with other people. One of the best ways to share a complex project is via `git` and its companion website **Github**. Throughout this course we will be practicing interacting with both of these. 

### Do I already have git installed? 

You might want to know if you have these things installed already. R, and Rstudio, if present, are installed as regular programs on your OS. git, however, is a command line tool and may not be obvious. One way to check is by running `which git`

![which git](img/which_git.gif)

`git` is a command-line program for doing "version control" : that is, for tracking changes to a group of files all at once. We're going to use it to track changes to our research project (i.e. data and the code that manipulates the data).

### Git installation: Windows

We reccommend this approach, following [Software Carpentry](http://software-carpentry.org), an organization that "teaches lab skills for scientific computing" (and also STAT545):

  * Install [Git for Windows](https://git-for-windows.github.io/), previously known as `msysgit` or "Git Bash", to get Git in addition to some other useful tools, such as the Bash [shell](git09_shell.html). 
  * This approach leaves the Git executable in a conventional location, which will help you and other programs, e.g. RStudio, find it and use it. 

### Git installation: Mac

**Option 1** (*recommended*): Install Git from here: <http://git-scm.com/downloads>.


### Git installation: Linux

If Git is not already available on your machine you can install it via your distro's package manager (e.g. `apt-get` or `yum`).

Ubuntu or Debian Linux

```
sudo apt-get install git
```

Fedora or RedHat Linux

```
sudo yum install git
```

## Register a GitHub account

[Github](https://github.com/) is an increasingly popular website for sharing code and data. It is an excellent platform for collaborating on projects, including scientific manuscripts.

  * Register for a [free individual GitHub account](github.com) 
  * Request [the student discount](https://education.github.com). This should give you some free private repositories for a couple of years.

### Next steps

After installation, you still need to [introduce yourself to Git](01_git_introduce) and [get it to remember your GitHub username and password](01_git_cache). If your Git client guides you through this, seize that opportunity! Otherwise follow the links for some assistance.

## R and RStudio

  * Install [R, a free software environment for statistical computing and graphics](http://www.r-project.org) from [CRAN](http://cran.rstudio.com), the Comprehensive R Archive Network. Install the precompiled binary for your Operating system.

  * Install [RStudio's IDE](http://www.rstudio.com/products/rstudio) (i.e. an _**I**ntegrated **D**evelopment **E**nvironment_), a powerful user interface for R. Get the Open Source Edition of RStudio Desktop (free).

    - We strongly suggest you try out the [Preview version](https://www.rstudio.com/products/rstudio/download/preview/). You'll often find helpful new features in these! Remember to update frequently
    - RStudio comes with a __text editor__, so there is no immediate need to install a separate stand-alone editor.
    - RStudio can __interface with Git(Hub)__. However, we will have to set that connection up first.

### Add-on packages

R is an extensible system and many people share useful code they have developed as a _package_ via CRAN and GitHub. To install a package from CRAN, for example the [`dplyr`](https://cran.rstudio.com/web/packages/dplyr/vignettes/introduction.html)  package for data manipulation, here is one way to do it in the R console (there are others).

```
install.packages("dplyr", dependencies = TRUE)
```

By including `dependencies = TRUE`, we are being explicit and extra-careful to install any additional packages the target package, `dplyr` in the example above, needs to have around.

You could use the above method to install the following packages, all of which we will use:

  * `tidyr`, [package webpage](https://cran.r-project.org/web/packages/tidyr/index.html)
  * `ggplot2` [package webpage](http://docs.ggplot2.org/)
  * `EML` [package webpage](https://github.com/ropensci/EML)

### Updating

If you have already have R or Rstudio installed, I still **highly reccommend** that you update everything first!  

  * If you upgrade R, you will need to update any packages you have installed. Copy-and-paste this to get started:

```
    update.packages(ask = FALSE, checkBuilt = TRUE)
```

Note that you may need more arguments, for example if you have a custom library location.

Also note: Anything installed from GitHub will need to be manually updated, i.e. using `devtools::install_github()`.


### Further resources

The above will get your basic setup ready but here are some links if you are interested in reading a bit further.

  * How to Use RStudio
    - <https://support.rstudio.com/hc/en-us>
  * RStudio's leads for learning R
    - <https://support.rstudio.com/hc/en-us/articles/200717153-Getting-Help-with-R>
  * R FAQ:
    - <http://cran.r-project.org/doc/FAQ/R-FAQ.html>
  * R Installation and Administration
    - <http://cran.r-project.org/doc/manuals/R-admin.html>
  * More about add-on packages in the R Installation and Administration Manual
     - <https://cran.r-project.org/doc/manuals/R-admin.html#Add_002don-packages>


If you have a pre-existing installation of R and/or RStudio, we **highly recommend** that you reinstall and upgrade to the most recent version. It is very easy and RStudio, specifically, is changing rapidly and positively. If you upgrade R, you will need to also update any packages you have installed.
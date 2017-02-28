---
title: "Online Repositories"
---

### Sharing your data with the world!

There are several important online data repositories. Some are specialized for certain domains, others are for any and all data types. Here we're going to take a look at several different online repositories.

Excellent resources

* [British Ecological Society guide to data management](http://www.britishecologicalsociety.org/wp-content/uploads/Publ_Data-Management-Booklet.pdf)
* [Nine simple ways to make it easier to (re) use your data](http://ojs.library.queensu.ca/index.php/IEE/article/view/4608/4898) White _et al_ 2013

## Before we start: ROpenSci

Before we begin looking at data repositories, I wanted to show you an amazing organization called [ROpenSci](http://ropensci.org/). For years the programmers and scientists at ROpenSci have worked to make R packages to get data _off the internet_. Their packages are extremely useful and 

Data is often made public by websites, using a technique called an **API** (an Application Programming Interface). These are ways of transmitting information between computer programs. Some of the most useful ROpenSci packages will obtain public data in this way, reformat it, and present it directly into R for you! We will meet _some_ of these today, but there are so many more! I strongly encourage you to check out Ropensci for yourself, to see what is the most useful for you!

#### DOIs

a DOI is a Digital Object Identifier. They indicate unique things on the internet -- you have probably seen them on published scientific papers. Anything with a DOI can be cited -- it is stable and persistent over time. When data is given a DOI, multiple authors or users can reference it. The major source of DOIs for data is [DataCite](https://www.datacite.org/)

## a few data repositories

* [Figshare](https://figshare.com)
* [Dryad](http://datadryad.org)
* [Knowledge Network of Biocomplexity](https://knb.ecoinformatics.org/)

### Activity: searching for useful data!

As an in-class exercise, use Figshare, Dryad, Zenodo and/or the KNB to find some data that relevant to your personal data project. This could be a collaborator, coauthor or stranger. If you yourself have used one of these repositories, try out a different one and see what you can find!

Step2: see if you can download this data into R.

|repository|r package|
|--------|---------|
| Knowledge Network for Biocomplexity         |  `rdataone`          |
| figshare                                      | `rfigshare` | 
| Dryad                                     | `rdryad` | 
| Zenodo                                   | `zenodo` (?) |

## Final thought: re-archiving data

What happens when you have been using _published_ data, and you want to document your process? Do you re-publish what was originally sombody else's data? While this might seem useful -- this is after all the data for your paper, and it might be a bit different from its original format. It also has an undesirable side-effect, in that you have created a second "version" of the data -- one that might divert citations away from the original! To avoid this, publish your code only (which reads and, if necessary, modifies the data), and cite the original data in your work.  

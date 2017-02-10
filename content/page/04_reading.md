
## reading in data

If you have spreadsheet-based data, the two easiest ways to read in data are 

1. read directly from excel
2. read from a csv file

I suggest you choose the first option if you want to keep your .xls file (e.g. perhaps you are not able to capture **all** the information with a CSV.) This might happen if not all the data in your excel file _can_ be represented in a CSV -- for example, you might have some data represented not as values in a cell, but as the colour of the cell.

Here is an example of reading in an excel file (from the [lecture_4_exercises](https://github.com/BIOL548O/lecture_4_exercises/) repo):
```r
library(readxl)

germin <- readxl::read_excel("data-raw/Schiz germination record.xlsx", sheet = 2)
head(germin)
View(germin)
```

### reading in a csv

You may be familiar with the base functions `read.csv` and `read.delim`. These are flexible, handy functions. However it has been my experience that, especially with "untidy" data, there are advantages to using a more modern version of the same functions, from the package `readr`

```r
read_csv("data/gapminder_wide.csv")
```

`readr::read_csv` has several useful behaviours: it never creates factors (it leaves text as text) and it doesn't add rownames. It also doesn't complain if you give it unconventional column names. I find that all of these traits come in handy when the data needs to be reorganized. Read more about readr [here](https://github.com/tidyverse/readr)

## Writing out data

Write your data out to a clean and tidy CSV in in your `data/` folder. Again, I find that using `write_csv` from the `readr` package makes things simple:

```r
library(readr)
write_csv(germin, path = "data/germin.csv")

```

## A word about relative paths

Note that in the above R scripts, I was reading an writing files using "relative paths". This means that you write the name of the folder(s) containing the file you want before the filename itself, separated with a `/`:

```
data/file_name_of_data.csv
```

This will work automatically if your Rstudio project is set up the way we discussed: with a `data/` directory. 

Why don't you have to write the complete path? Something like (for a Mac) `/Users/amacdonald/Documents/Projects/BIOL548O/BIOL548O.github.io` or on a PC `c:\\amacdonald\Desktop\files\thesis_chapter\` etc? Both of these paths start at the "home folder" of your computer. But if we are working in an Rstudio project, such precision is not necessary. All we need to do is direct the computer to the `data` folder in _this_ project.

One way to think of relative paths is to read them as saying: "from here, go into the data folder", where "here" is assumed to be your project folder (i.e., wherever your `.Rproj` file lives). 
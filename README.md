# Homework 1: Data Analysis Basics

## Dataset
Obtain the CSV (comma separated variable) file containing the counts of
bicycles crossing the Fremont Bridge since 2012 (as described in
`https://data.seattle.gov/Transportation/Fremont-Bridge-Hourly-Bicycle-Counts-by-Month-Octo/65db-xm6k`).

## Folder Structure
```
.
├── ISSUE_TEMPLATE.md
├── LICENSE
├── README.md
└── project
    ├── README.md
    ├── analysis
    │   └── hw1.ipynb
    └── data
        └── bicycle_data.csv
```
Clone your git repository and create a directory called `project`. 

Inside `project`, create 2 subdirectories called `data` and `analysis` and 1 file `README.md` (files with `.md` format are [markdown files](https://www.markdownguide.org/cheat-sheet/) which GitHub renders for you). 

Download the data from
`https://data.seattle.gov/api/views/65db-xm6k/rows.csv?accessType=DOWNLOAD` and
put it in the `data` directory as `bicycle_data.csv`. 

Create a Jupyter notebook `hw1.ipynb` in `analysis` folder to analyze these data.

## Problem
In the notebook, please complete the following:
1. Read the CSV file into a pandas dataframe `1pt`
2. In a comment cell, describe the columns in the dataframe and what data types they should be. If the data types in the dataframe do not match what you think they should be, update them. `1pt`
3. Add columns to the dataframe containing:
   * The total (East + West) bicycle count `1pt`
   * The hour of the day `1pt`
   * The year `1pt`
4. Create a new dataframe with the subset of data from the year 2016 `1pt`
5. For the dataframe in `3.`, are there any time points with missing data? If so, do something to make sure missing data does not impact parts 6 and 7. `1pt`
6. For the dataframe in `3.`, use pandas + matplotlib to plot the counts by hour. (i.e. hour of the day on the x-axis, total daily counts on the y-axis) `1pt`
7. For the dataframe in `3.`, Lastly, use python (and pandas) programming to computationally determine what is (on average) the busiest hour of the day `1pt`

`Push your homework to GitHub. Please avoid uploading your data folder.` Extra cheer for people who use [.gitignore](https://git-scm.com/docs/gitignore) for this. 

Note that we fully expect this analysis to cover some unfamiliar ground, and
require teaching yourself a bit about Python and/or the Pandas package. Part of
the intent of this assignment is to give you practice seeking help via the web,
which (in our experience) is an essential part of using any data science
tool. For example, if you type a question about Pandas into search engine, you’ll
often find an existing answer to your question or something similar on the
website StackOverflow.

A couple other online resources that might be helpful as you work through this:

* [The Python Data Science Handbook](https://jakevdp.github.io/PythonDataScienceHandbook/) (free online) has a chapter devoted to Pandas
* [Jake’s Jupyter Workflow Video Series](http://jakevdp.github.io/blog/2017/03/03/reproducible-data-analysis-in-jupyter/) shows some examples of working with this particular dataset in a Jupyter notebook. 

## Hints
The “date” field is a string coded as “yyyy-mm-dd Thh” where “yyyy” is the
year, “mm” is the month, “dd” is the day, and “hh” is the hour. (You’ll need to
write python code to decode the string.)

## Bonus
If you're already familiar with pandas, convert the whole "Date" column to a
datetime format, e.g., `datetime.datetime` or `numpy`'s datetime or the default
Pandas datetime format. Write a little about the difference between these
formats in the `README.MD` file you created in the `project` folder. Extra learning points if your readme file uses
different kinds of markdown syntax.

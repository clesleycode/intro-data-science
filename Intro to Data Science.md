Intro to Data Science
==================

Brought to you by [Lesley Cordero](http://www.columbia.edu/~lc2958) and [ADI](https://adicu.com)

## Table of Contents

- [0.0 Setup](#00-setup)
    + [0.1 Python & Pip](#01-python--pip)
    + [0.2 R & R Studio](#02-r--r-studio)
    + [0.3 Other](#03-other)
- [1.0 Background](#10-background)
    + [1.1 What is Data Science?](#11-what-is-data-science)
        * [1.1.1 What do you mean by data?](#111-what-do-you-mean-by-data)
    + [1.2 Is data science the same as machine learning?](#12-is-data-science-the-same-as-machine-learning)
    + [1.3 Why is Data Science important?](#13-why-is-data-science-important)
    + [1.4 Data Roles](#14-data-roles)
        * [1.4.1 Data Analysis](#141-data-analyst)
        * [1.4.2 Data Engineer](#142-data-engineer)
        * [1.4.3 Data Scientist](#143-data-scientist)
- [2.0 Data Science Process](#20-data-science-process)
    + [2.1 What is a "Data Science" Problem?](#21-what-is-a-data-science-problem)
    + [2.2 ...So where do I begin?](#22-so-where-do-i-begin)
    + [2.3 Given Problem](#23-given-problem)
        * [2.3.1 Open Data](#231-open-data)
    + [2.4 Given Data](#24-given-data)    
- [3.0 Important Concepts](#30-important-concepts)
    + [3.1 Machine Learning](#31-machine-learning)
        * [3.1.1 Supervised Learning](#311-supervised-learning)
        * [3.1.2 Unsupervised Learning](#312-unsupervised-learning)
        * [3.1.3 Reinforcement Learning](#313-reinforcement-learning)
- [4.0 Tackling a Data Problem](#40-tackling-a-data-problem)
    + [4.1 Data Preparation](#41-data-preparation)
    + [4.2 Data Cleaning](#42-data-cleaning)
    + [4.3 Data Analysis](#43-data-analysis)
        * [4.4.1 Basics](#431-basics)
        * [4.4.2 Time Series Analysis](#432-time-series-analysis)
        * [4.4.3 Deep Learning](#433-deep-learning)
        * [4.4.4 Natural Language Processing](#434-natural-language-processing)
- [5.0 Final Words](#50-final-words)
    + [5.1 Resources](#51-resources)
    + [5.2 Mini Courses](#52-mini-courses)


## 0.0 Setup

This guide was written in Python 3.5 and R 3.2.3.

### 0.1 Python & Pip

Download [Python](https://www.python.org/downloads/) and [Pip](https://pip.pypa.io/en/stable/installing/).

### 0.2 R & R Studio

Install [R](https://www.r-project.org/) and [R Studio](https://www.rstudio.com/products/rstudio/download/).

### 0.3 Other

We'll soon get into the difference between packages in R and modules in Python. For now, let's install the ones we'll need for this tutorial. Open up your terminal and enter the following commands to install the needed python modules: 

```
pip3 install ggplot
pip3 install nltk
pip3 install itertools
pip3 install HTMLParser
pip3 install BeautifulSoup
pip3 install requests
```

Next, to install the R packages, cd into your workspace, and enter the following, very simple, command into your bash: 

```
R
```

This will prompt a session in R! From here, you can install any needed packages. For the sake of this tutorial, enter the following into your terminal R session:

```
install.packages("pdftools)
install.packages(ggvis) 
install.packages("heatmaply")
```

### 0.4 Virtual Environment

If you'd like to work in a virtual environment, you can set it up as follows: 
```
pip3 install virtualenv
virtualenv your_env
```
And then launch it with: 
```
source your_env/bin/activate
```

To execute the visualizations in matplotlib, do the following:

```
cd ~/.matplotlib
nano matplotlibrc
```
And then, write `backend: TkAgg` in the file. Now you should be set up with your virtual environment!

Cool, now we're ready to start! 

## 1.0 Background

Before we head into an actual data science problem demo, let's go over some vital background information. 

### 1.1 What is Data Science?

Data Science is the application of statistical and mathematical methods to problems involving sets of data. In other words, it's taking techniques developed in the areas of statistics and math and using them to learn from some sort of data source. 

#### 1.1.1 What do you mean by data? 

Data is essentially anything that can be recorded or transcribed - numerical, text, images, sounds, anything!

#### 1.1.2 What background do you need to work on a data science problem?

It depends entirely on what you're working on, but generally speaking, you should be comfortable with probability, statistics, and some linear algebra.  

### 1.2 Is data science the same as machine learning?

Well, no. They do have overlap, but they are not the same! Whereas the topic of machine learning involves lots of theoretical components we won't worry about, data science takes these methods and applies them to the real world. It's important to note that studying these theoretical components can be very useful to your understanding of data science, however!

### 1.3 Why is Data Science important? 

Data Science has so much potential! By using data in creative and innovative ways, we can gain a lot of insight on the world, whether that be in economics, biology, sociology, math - any topic you can think of, data science has its role. 


### 1.4 Data Roles

#### 1.4.1 Data Analyst

Data Analysts have a high range in role differences. They include analysts who focus on excel as well as engineers who code analytics with Python or R.    

#### 1.4.2 Data Engineer

Data Engineers are similar to your typical software engineering roles, but with a specialty in data science processes. 

#### 1.4.3 Data Scientist

Data Scientists require the highest level of specialty. It requires a high level of programming and statistic skills. 

### 1.5 Software

This section would vary depending on your choice of main tools you choose for data mining. There are generally three languages used in Data Science:

- R: R is great for statistical analysis. It has a high range of libraries very useful for different aspects of data science. 
- Python: Python is a dynamic language commonly used in the area of Data Science. 
- SAS: SAS (Statistical Analysis System) is a software suite developed for advanced analytics, multivariate analyses, business intelligence, data management, and predictive analytics.

## 2.0 Data Science Process

It might seem like data scientists concentrate on the statistical concepts to tackle a data science problem. But the reality is that the majority of data scientists' time is spect on data acquisition, preparation, and cleaning.

### 2.1 What is a "Data Science" problem?

If your problem involves the use of data in some capacity, then it's probably a data science problem! What type of data that is doesn't matter - all that matters is that you're using it, along with mathematical tools, to gain insight into whatever problem you happen to be focusing on. 

### 2.2 ...So where do I begin?

A big part of data science is figuring out what to work on. There are two ways of going about finding an interesting problem, in my experience. 

### 2.3 Given Problem

The first is you're given a problem (or you think of one yourself), and you have to find that data before beginning the process of finding insight. How hard or easy this problem is dependent on the data available to you. If you're working at a company, do they have this data for you to use already? If you're working on a side project, is the accumulated data available for public use? 

These are all questions you should be asking yourself when first starting a data science project: <b> Where will my data come from?</b>

One glorious thing about Data Science is<b> Open Data </b>, which you'll learn more about later. 

### 2.4 Given Data

The second is you're given data and you have to work with it until you find something interesting. If you figure out there's nothing interesting, move on a find a new project.

## 3.0 Important Concepts

### 3.1 Machine Learning

Generally speaking, Machine Learning can be split into three types of learning: supervised, unsupervised, and reinforcement learning. 

#### 3.1.1 Supervised Learning

This algorithm consist of a target / outcome variable (or dependent variable) which is to be predicted from a given set of predictors (independent variables). Using these set of variables, we generate a function that map inputs to desired outputs. The training process continues until the model achieves a desired level of accuracy on the training data. Examples of Supervised Learning: Regression, Decision Tree, Random Forest, KNN, Logistic Regression etc.


#### 3.1.2 Unsupervised Learning

In this algorithm, we do not have any target or outcome variable to predict / estimate.  It is used for clustering population in different groups, which is widely used for segmenting customers in different groups for specific intervention. Examples of Unsupervised Learning: Apriori algorithm, K-means.


#### 3.1.2 Reinforcement Learning

Using this algorithm, the machine is trained to make specific decisions. It works this way: the machine is exposed to an environment where it trains itself continually using trial and error. This machine learns from past experience and tries to capture the best possible knowledge to make accurate business decisions. Example of Reinforcement Learning: Markov Decision Process.


### 3.2 Data 

As a data scientist, knowing the different forms data takes is highly important. 

#### 3.2.1 Training vs Test Data

When it comes time to train your classifier or model, you're going to need to split your data into <b>testing</b> and <b>training</b> data. 

Typically, the majority of your data will go towards your training data, while only 10-25% of your data will go towards testing. It's important to note there is no overlap between the two. Should you have overlap or use all your training data for testing, your accuracy results will be wrong. Any classifier that's tested on the data it's training is obviously going to do very well since it will have observed those results before, so the accuracy will be high, but wrongly so. 


#### 3.2.2 Open Data 

What's open data, you ask? Simple, it's data that's freely  for anyone to use! Some examples include things you might have already heard of, like APIs, online zip files, or by scraping data!

You might be wondering where this data comes from - well, it can come from a variety of sources, but some common ones include large tech companies like Facebook, Google, Instagram. Others include large institutions, like the US government! Otherwise, you can find tons of data from all sorts of organizations and individuals. 

### 3.3 Overfitting vs Underfitting

In section 3.2.1, we mentioned the concept of overfitting your data. The concept of overfitting refers to creating a model that doesn't generalize to your model. In other words, if your model overfits your data, that means it's learned your data <i>too</i> much - it's essentially memorized it. This might not seem like it would be a problem at first, but a model that's just "memorized" your data is one that's going to perform poorly on new, unobserved data. 

Underfitting, on the other hand, is when your model is <i>too</i> generalized to your data. This model will also perform poorly on new unobserved data. This usually means we should increase the number of considered features, which will expand the hypothesis space. 

## 4.0 Tackling a Data Problem 

### 4.1 Data Acquisition

Data Acquisition will always be the first step. It's the part of the process that asks "where is my data coming from?" There are many ways to grab your data - APIs, webscraping, zipfiles, etc, but in this tutorial, we'll go through a web scraping example. 

Web Scraping tools are specifically developed for extracting information from websites. Web Scraping mostly focuses on the transformation of unstructured data (HTML format) on the web into structured data (database or spreadsheet).

#### 4.1.1 HTML 
While performing web scraping, we deal with html tags. Thus, we must have good understanding of them. Below is the basic syntax of HTML:

``` html
<!DOCTYPE html> 
<html>
    <body>
        <h1> First Heading </h1>
        <p> First Paragraph </p>
    </body>
</html>
```
Let's break down each of these tags:

1. `<!DOCTYPE html>`: This is the initial HTML declaration.
2. `<html>`: The HTML document is going to be contained within this tag.
3. `<body>`: This is where the visible portion of the HTML document is between. 
4. `<h1>`: This is an HTML heading.
5. `<p>`: HTML paragraphs are defined here. 

We've also got the following tags:

- `<a>`: These always define HTML links, such as with 
``` HTML
<a href="http://byteacademy.co">This is Byte Academy's website!</a>
```
- `<table>`: HTML tables are defined with this tag, such as:
*Note that the `<tr>`are rows and `<td>` defines columns. 
``` HTML
<table style="width:100%">
    <tr>
        <td>Lesley</td>
        <td>Cordero</td>
        <td>24</td>
    </tr>
    <tr>
        <td>Helen</td>
        <td>Chen</td>
        <td>22</td>
    </tr>
</table>
```
This will yield the following:
```
Lesley      Cordero     24
Helen       Chen        22
```
- `<li>` initializes the beginning of a list. `<ul>` and `<ol>` each define whether it's an unordered list or an ordered list. 


#### 4.1.2 BeautifulSoup

BeautifulSoup is used to parse the data.

``` python
import requests
from bs4 import BeautifulSoup
```

``` python
wiki = "https://en.wikipedia.org/wiki/List_of_states_and_territories_of_the_United_States"
page = requests.get(wiki)
html = page.content
```

``` python
soup = BeautifulSoup(html)
```

Now, let's explore this webpage! 

``` python
soup.title
```
This outputs the title of the wikipedia page: 
```
<title>List of states and territories of the United States - Wikipedia</title>
```

The string version of this can be obtained with:

``` python
soup.title.string
```
With `soup.a`, we can output the links under the `<a>` tag. We get the following:
```
<a id="top"></a>
```

But this only allows us to have one output. If we want to extract all the links within `<a>`, we will use `find_all()`, as the following:
``` python
all_links = soup.find_all("a")
for i in all_links:
    print(i.get("href"))
```

Since we're looking for the capital of each state, let's use `find_all` to retrieve the table tags:
``` python
all_tables = soup.find_all('table')
```

Now we have to identify the right table. We filter this by figuring out what the attribute class name is. In chrome, you can check the class name by right click on the table of web page. Then you click "Inspect" and copy the class name. You also go through the output of above command find the class name of right table.

``` python
right_table = soup.find('table', class_='wikitable sortable plainrowheaders')
```

And finally, we have scraped all the needed information. 

### 4.2 Data Preparation

#### 4.2.1 Pandas DataFrame

Once you have all your dataset, the next step will likely be data preparation. In the previous example, we'll be storing it to a pandas DataFrame.

We're now going to begin by storing the data from the website. We'll grab the first few columns, so we'll initialize a list for each of these here:

``` python
A=[]
B=[]
C=[]
```
Next, is to actually grab the needed data and add it to each list. We iterate through the scraped data, row by row:

``` python
for row in right_table.findAll("tr"):
    cells = row.findAll('td')
    states=row.findAll('th') 
    if len(cells) == 9 or len(cells) == 8: 
        A.append(cells[0].find(text=True))
        B.append(states[0].find(text=True))
        C.append(cells[1].find(text=True))
```
Here, we actually create the DataFrame with pandas: 

``` python
import pandas as pd
df=pd.DataFrame(A,columns = ['Number'])
df['State/UT'] = B
df['Admin_Capital'] = C
```

#### 4.2.2 PDFtools

Very often, your data might not be so easily accessible. If you're lucky, an API exists or it's in the form of a spreadsheet. But sometimes, you might be given something you have to work to get the data from. In the following example, we'll be working with data off a pdf. 

So we'll begin by scraping the text off this PDF in R, which has a great package for scraping data from pdfs (pdftools). 

``` R
library(pdftools)
download.file("http://undergrad.admissions.columbia.edu/sites/default/files/class_of_2016_profile.pdf", "eval.pdf", mode = "wb”)
eval <- pdf_text("eval.pdf")
```
Just to see that it works, let's try a couple of examples.

```
# first page text
cat(eval[1])
```
Here's page 1!

```
# second page text
cat(eval[2])
```

There's page 2! 

Pretty neat, huh? 

``` R
for (i in eval) {
    print(strsplit(i,"\n"))
}
```

### 4.3 Data Cleaning

Now we move onto the data cleaning portion of this tutorial. Not only might you have to scrape data off a website or pdf, but then your data might be in a completely different format than you wished. This is especially important when handling non-numerical data.

Consider a dataset consisting of text. There are a lot ways in which you might need to clean this data so that you're able to use it for future modeling or prediction. 

```
original_tweet = "I luv my &lt;3 iphone &amp; you’re awsm apple. DisplayIsAwesome, sooo happppppy http://www.apple.com"
```

HTMLParser is a Python module that allows you to convert entities to standard symbols. In the example above, &lt; and &amp; should really be < and &. 

``` python
from html.parser import HTMLParser
html_parser = HTMLParser()
tweet = html_parser.unescape(original_tweet)
```

Now we've got:

```
'I luv my <3 iphone & you’re awsm apple. DisplayIsAwesome, sooo happppppy http://www.apple.com'
```

 Sometimes words aren't in proper formats though. “I looooveee you” should be “I love you”, but we can use simple rules and regular expressions to fix these cases!

```python
import itertools
tweet = ''.join(''.join(s)[:2] for _, s in itertools.groupby(tweet))
```

Now we get: 

``` python
'I luv my <3 iphone & you’re awsm apple. DisplayIsAwesome, soo happy http://ww.apple.com'
```

The list goes on on all the possible ways in which you can clean your data. Consider spelling mistakes, grammar issues, etc!

### 4.4 Data Visualization 

Data Visualization is an important aspect of data science. It allows us to showcase the work we've done through visualizations, which can be stagnant or interactive. 

#### 4.4.1 Python Modules

[matplotlib](http://matplotlib.org/) is a 2D python plotting library which allows you to generate plots, histograms, power spectra, bar charts, errorcharts, scatterplots, etc, with just a few lines of code.

``` python
import matplotlib.pyplot as plt
plt.plot([1,2,3,4], [1,4,9,16], 'ro')
plt.axis([0, 6, 0, 20])
plt.show()
```

[bokeh](http://bokeh.pydata.org/en/latest/) is an interactive visualization library for modern web browsers presentation. 

[ggplot](http://ggplot.yhathq.com/) is a plotting system built for making professional-looking plots quickly with minimal code.

``` python
from ggplot import *

ggplot(aes(x='date', y='beef'), data=meat) +\
    geom_line() +\
    stat_smooth(colour='blue', span=0.2)
```

[seaborn](http://seaborn.pydata.org/introduction.html#introduction) is a library for making statistical graphics in Python. It's built on top of matplotlib and is tightly integrated with the PyData stack, including support for numpy and pandas data structures and statistical routines from scipy and statsmodels. 

#### 4.4.2 R Packages

[ggvis](http://ggvis.rstudio.com/) allows you to visualize interactive plots from the makers of ggplot2.

``` python
library(ggvis)
iris %>% ggvis(~Petal.Length, ~Petal.Width, fill = ~Species) %>% layer_points()
```

[ggplot2](http://www.statmethods.net/advgraphs/ggplot2.html) is one of the best static visualization packages in R. 

[heatmaply](https://mran.revolutionanalytics.com/package/heatmaply/) produces interactive heatmaps.

``` python
library(heatmaply)
heatmaply(cor(mtcars), 
k_col = 2, k_row = 2,
limits = c(-1,1)) %>% 
layout(margin = list(l = 40, b = 40))
```

[plotly](https://plot.ly/r/) allows you to convert ggplot2 figures to interactive plots easily.

### 4.5 Data Analysis

And of course, we have the analysis portion. We won't go into too many details, but we'll go over some basics.

#### 4.5.1 Basics

At a very basic level, you can get different numerical results from your text. You can count the number of verbs, the number of nouns, etc. You can also easily count the number of words in your text and the frequency of each word.

Like this: 

```python
from nltk.book import *
import string, re

fdist1 = FreqDist(text1)
```

From here, we'll move into the different areas supported by Programming Languages. 

#### 4.5.2 Time Series Analysis 

Time Series Analysis includes methods for analyzing time series data to extract meaningful statistics and characteristics. 

[Time Series Datasets](https://datamarket.com/data/list/?q=provider:tsdl)

#### 4.5.3 Deep Learning

Deep Learning is a branch of machine learning that involves pattern recognition on unlabeled and unstructured data. and uses a model of computing inspired by the structure of the brain. Hence we call this model a neural network. 

[Detexify](http://detexify.kirelabs.org/classify.html)

#### 4.5.4 Natural Language Processing

Natural Language Processing, or NLP, is an area of computer science that focuses on developing techniques to produce machine-driven analyses of text.

[Google Translate](https://translate.google.com/)

## 5.0 Final Words

### 5.1 Resources

If you liked any of what you saw, look below for more resources!

[Johns Hopkins Data Science Coursera](https://www.coursera.org/specializations/jhu-data-science) <br>
[List of Public Datasets](https://github.com/caesar0301/awesome-public-datasets)<br>
[The Art of R Programming](https://www.dropbox.com/s/cr7mg2h20yzvbq3/The_Art_Of_R_Programming.pdf?dl=0)<br>
[Python Data Visualization Cookbook](https://www.dropbox.com/s/iybhvjblkjymnw7/Python%20Data%20Visualization%20Cookbook%20-%20Milovanovic%2C%20Igor-signed.pdf?dl=0)<br>


### 5.2 Mini Courses

Learn about courses [here](www.byteacademy.co/all-courses/data-science-mini-courses/).

[Python 101: Data Science Prep](https://www.eventbrite.com/myevent?eid=31375137882) <br>
[Intro to Data Science & Stats with R](https://www.eventbrite.com/e/data-sci-109-intro-to-data-science-statistics-using-r-tickets-31375339485) <br>
[Data Acquisition Using Python & R](https://www.eventbrite.com/e/data-sci-203-data-acquisition-using-python-r-tickets-30980705123) <br>
[Data Visualization with Python](https://www.eventbrite.com/e/data-sci-201-data-visualization-with-python-tickets-30980827489) <br>
[Fundamentals of Machine Learning and Regression Analysis](https://www.eventbrite.com/e/data-sci-209-fundamentals-of-machine-learning-and-regression-analysis-tickets-30980917759) <br>
[Natural Language Processing with Data Science](https://www.eventbrite.com/e/data-sci-210-natural-language-processing-with-data-science-tickets-30981006023) <br>
[Machine Learning with Data Science](https://www.eventbrite.com/e/data-sci-309-machine-learning-with-data-science-tickets-30981154467) <br>
[Databases & Big Data](https://www.eventbrite.com/e/data-sci-303-databases-big-data-tickets-30981182551) <br>
[Deep Learning with Data Science](https://www.eventbrite.com/e/data-sci-403-deep-learning-with-data-science-tickets-30981221668) <br>
[Data Sci 500: Projects](https://www.eventbrite.com/e/data-sci-500-projects-tickets-30981330995)


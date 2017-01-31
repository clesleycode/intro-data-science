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
pip install ggplot
pip install nltk
pip install seaborn 
```

Next, to install the R packages, cd into your workspace, and enter the following, very simple, command into your bash: 

```
R
```

This will prompt a session in R! From here, you can install any needed packages. For the sake of this tutorial, enter the following into your terminal R session:

```
install.packages("pdftools”)
install.packages(“ggplot2”) 
install.packages("dplyr")
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

- R: R along with all the key libraries. RStudio is a good choice of environment.
- Python: iPython notebooks, Dato (Graphlab), vowpal-wabbit, import.io are some interesting additional libraries apart from other scientific libraries.
- SAS: Base SAS along with Enterprise Guide (for GUI driven interface) and Enterprise Miner and the modules depending on the license you have. It also offers TextMiner / JMP and a lot of industry specific modules.


## 2.0 Data Science Process

It might seem like data scientists concentrate on the statistical concepts to tackle a data science problem. But the truth is that Data Science is much more than the tools we use. It is the combined thought processes we engage with to come up with the best and most efficient solution to a data science problem.

You might have heard of the 80|20 rule in Economics? Data Science has its own version of the 80|20 rule, in that only 20% of your time as a data scientist is spent actually working on gaining insights from your data, whereas about 80% of it is spent managing, preparing, and cleaning the data.

### 2.1 What is a "Data Science" problem?

If your problem involves the use of data in some capacity, then it's probably a data science problem! What type of data that is doesn't matter - all that matters is that you're using it, along with mathematical tools, to gain insight into whatever problem you happen to be focusing on. 

### 2.2 ...So where do I begin?

A big part of data science is figuring out what to work on. There are two ways of going about finding an interesting problem, in my experience. 

### 2.3 Given Problem

The first is you're given a problem (or you think of one yourself), and you have to find that data before beginning the process of finding insight. How hard or easy this problem is dependent on the data available to you. If you're working at a company, do they have this data for you to use already? If you're working on a side project, is the accumulated data available for public use? 

These are all questions you should be asking yourself when first starting a data science project: <b> Where will my data come from?</b>

One glorious thing about Data Science is<b> Open Data </b>, which you'll learn more about in section 3. 

### 2.4 Given Data

The second, is you're given data and you have to work with it until you find something interesting. If you figure out there's nothing interesting, move on a find a new project. It happens to the best of us.


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

### 4.1 Data Preparation

As you can see, this data is in the form of a PDF, an incredibly source of data. How would you go about getting this data? Scraping it. 

This highlights an important obstacle in the data science process. Very often, your data might not be so easily accessible. If you're lucky, an API exists or it's in the form of a spreadsheet. But sometimes, you might be given something you have to work to get the data from. This is an example of one of those not so easy cases. 

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

### 4.2 Data Cleaning

Now we move onto the data cleaning portion of this tutorial. Not only might you have to scrape data off a website or pdf, but then your data might be in a completely different format than you wished. This is especially important when handling non-numerical data.

Consider a dataset consisting of text. There are a lot ways in which you might need to clean this data so that you're able to use it for future modeling or prediction. 

```
original_tweet = "I luv my &lt;3 iphone &amp; you’re awsm apple. DisplayIsAwesome, sooo happppppy http://www.apple.com"

```

HTMLParser is a Python module that allows you to convert entities to standard symbols. In the example above, &lt; and &amp; should really be < and &. 

``` python
import HTMLParser
html_parser = HTMLParser.HTMLParser()
tweet = original_tweet.decode("utf8")
tweet = html_parser.unescape(tweet)
```

Now we've got:

```
u'I luv my <3 iphone & you\u2019re awsm apple. DisplayIsAwesome, sooo happppppy http://www.apple.com'
```

 Sometimes words aren't in proper formats though. “I looooveee you” should be “I love you”, but we can use simple rules and regular expressions to fix these cases!

```python
tweet = ''.join(''.join(s)[:2] for _, s in itertools.groupby(tweet))
```

Now we get: 

``` python
u'I luv my <3 iphone & you\u2019re awsm apple. DisplayIsAwesome, soo happy http://ww.apple.com'
```

The list goes on on all the possible ways in which you can clean your data. Consider spelling mistakes, grammar issues, etc!


### 4.3 Data Visualization 

#### 4.3.1 Python Modules


[bokeh](http://bokeh.pydata.org/en/latest/) is an interactive visualization library for modern web browsers presentation. 

[ggplot](http://ggplot.yhathq.com/) is a plotting system built for making profressional-looking plots quickly with minimal code.

``` python
from ggplot import *

ggplot(aes(x='date', y='beef'), data=meat) +\
    geom_line() +\
    stat_smooth(colour='blue', span=0.2)
```

[matplotlib](http://matplotlib.org/) is a 2D python plotting library which allows you to generate plots, histograms, power spectra, bar charts, errorcharts, scatterplots, etc, with just a few lines of code.

[pygal](http://pygal.org/en/stable/) is a charting library that includes bar charts, line charts, XY charts, pie charts, radar charts, dot charts, pyramid charts, funnel charts, gauge charts. It also includes css features with pre-defined themes.

[python-igraph](https://pypi.python.org/pypi/python-igraph) is a collection of network analysis tools with the emphasis on efficiency, portability, and ease of use. 

[seaborn](http://seaborn.pydata.org/introduction.html#introduction) is a library for making statistical graphics in Python. It's built on top of matplotlib and is tightly integrated with the PyData stack, including support for numpy and pandas data structures and statistical routines from scipy and statsmodels. 
- seaborn allows you to choose color palettes to make plots that reveal patterns in your data. 
- seaborn contains functions for visualizing univariate and bivariate distributions.
- seaborn offers tools that fit and visualize linear regression models for different kinds of independent and dependent variables.
- seaborn contains functions that visualize matrices of data and use clustering algorithms to discover structures in those matrices.
- seaborn offers a function to plot statistical timeseries data.



#### 4.3.2 R Packages

### 4.4 Data Analysis

#### 4.4.1 Basics

At a very basic level, you can get different numerical results from your text. You can count the number of verbs, the number of nouns, etc. You can also very easily count the number of words in your text and the frequency of each word.

Like this: 

```python
from nltk.book import *
import string, re

fdist1 = FreqDist(text1)
```

From here, we'll move the different areas supported by Programming Languages. 

4.4.2 Time Series Analysis 

Time Series Analysis includes methods for analyzing time series data to extract meaningful statistics and characteristics. 

[Time Series Datasets](https://datamarket.com/data/list/?q=provider:tsdl)

4.4.3 Deep Learning

Deep Learning is a branch of machine learning that involves pattern recognition on unlabeled and unstructured data. and uses a model of computing inspired by the structure of the brain. Hence we call this model a neural network. The basic foundational unit of a neural network is the neuron, which is actually conceptually quite simple. 

[Detexify](http://detexify.kirelabs.org/classify.html)

4.4.4 Natural Language Processing

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

[Python 101: Data Science Prep](https://www.eventbrite.com/e/python-101-data-science-prep-tickets-30980459388) <br>
[Intro to Data Science & Stats with R](https://www.eventbrite.com/e/data-sci-109-intro-to-data-science-statistics-using-r-tickets-30908877284) <br>
[Data Acquisition Using Python & R](https://www.eventbrite.com/e/data-sci-203-data-acquisition-using-python-r-tickets-30980705123) <br>
[Data Visualization with Python](https://www.eventbrite.com/e/data-sci-201-data-visualization-with-python-tickets-30980827489) <br>
[Fundamentals of Machine Learning and Regression Analysis](https://www.eventbrite.com/e/data-sci-209-fundamentals-of-machine-learning-and-regression-analysis-tickets-30980917759) <br>
[Natural Language Processing with Data Science](https://www.eventbrite.com/e/data-sci-210-natural-language-processing-with-data-science-tickets-30981006023) <br>
[Machine Learning with Data Science](https://www.eventbrite.com/e/data-sci-309-machine-learning-with-data-science-tickets-30981154467) <br>
[Databases & Big Data](https://www.eventbrite.com/e/data-sci-303-databases-big-data-tickets-30981182551) <br>
[Deep Learning with Data Science](https://www.eventbrite.com/e/data-sci-403-deep-learning-with-data-science-tickets-30981221668) <br>
[Data Sci 500: Projects](https://www.eventbrite.com/e/data-sci-500-projects-tickets-30981330995)


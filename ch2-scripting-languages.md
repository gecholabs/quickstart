# CH 2 - **Scripting \(programming\) languages**

I found the Python language via R. Specifically, I did the analyses for dissertation exclusively in R. When I was trying to develop a web interface to my results \(pre R-Shiny\), I stumbled across Ruby on Rails and RSRuby. As I followed the trail, I realized it was a fork of R2Py and wham, discovered Python. My first experience of PyCon was like walking into Lothlórien. It felt like an epiphany at the time and I’ve never looked back.**              
**

![](/assets/image1.png)

## Python and R

### **Why Python \(my favorite language\)**

* It’s relatively easy to get started

* You get all the other languages you need with it \(e.g. R, Scala, C\)

* It’s a Swiss Army Knife: you can do everything from web development to natural language to video games to to robotics and hacking

* One ring to rule them all

### **What About R**

R \(another fantastic language\) was written initially by statisticians for statisticians; in that capacity it is excellent. Indeed my univeristy stats proffessor was an early adopter. He'd grown tired of developing methods only to have to pay a license so his students could use an outdated version of his method. Unfortuntely, from teaching and training colleagues and students, I've found the learning curve can be needlessly steep, it is mostly limited to analytics, the input/output is excruciating, and  the parts don’t quite work together. However, if you are doing an analysis it is THE definitive source of packages and the **dataframe** concept is pure genius. RShiny has made it easy to share your results online, RStudio is slick, and the stats libraries are industry standard.

**Installing R**

**Just the core**

`conda install -c r r-essentials`

**All the things**

```
brew tap homebrew/science 
brew install Rbrew install Caskroom/cask/rstudio
```

### **Python vs R \(moreso Python + R\)**

I consider Python to be more versatile for my use case as a full-stack data scientist. So, how does one get the benefits of R without the hassles of R,

1\) Embed R in Python code to access the libraries

2\) Use Pandas dataframes in Python

**Calling R from Python**

```
conda install rpy2Jupyter notebook
```

**In Jupyter**

Point your browser to ** **[http://localhost:8888/](http://localhost:8888/%29**%29 \)

Then enter this into the first cell and press CMD⌘ + Enter\`

```
%load_ext rpy2.ipython
%R X=c(1,4,5,7); sd(X); mean(X)
```

**  
This should return**

`array([ 4.25])`

## ![](/assets/image9.png)

**Pandas DataFrames**

Pandas Dataframes revolutionized the Python workflow and were an R-killer for me. Beyond dataframes, I find Pandas is THE most useful framework for analytics in Python. A DataFrame can be conceptualized like a souped up Excel spreadsheet. You have a grid with rows and columns of data, except the cells can contain diverse of types of information, beyond a simple value, e.g. arrays, lists, dictionaries. A DataFrame consists of 3 keys components: the data, the index, and the columns.

The definiative guide to Pandas is written by Wes Mckinney, the author of the package/concept. Here is a new 2nd edition available as of Sept 25, 2017. I can't recommend this book enough.

![](/assets/pandas.png)[Python for Data Analysis Book](http://wesmckinney.com/pages/book.html)

**Here’s an intro to DataFrames**

[**https://codingnetworker.com/2016/09/pandas-dataframes-101/**](https://codingnetworker.com/2016/09/pandas-dataframes-101/)

**And, an intro to Pandas**

[**https://pandas.pydata.org/pandas-docs/stable/10min.html**](https://pandas.pydata.org/pandas-docs/stable/10min.html)**              
**

Combining Python, DataFrames and R

Let’s graph a Python dataframe with R’s GGplot

`conda install -c r r-ggplot2`

Now run this code in a Jupyter notebook

**Cell \#1**

```
%load_ext rpy2.ipython 
import pandas as pd 
import numpy as np 
data = np.random.randn(5000,1) 
df = pd.DataFrame(data, columns=["value"])
```

Cell \#2

```
%%R -i df -w800-h480-u px 
library(ggplot2) 
ggplot(df) + geom_density(aes(x=value))
```

![](/assets/image11.png)

> Source** **[**https://ragrawal.wordpress.com/2016/08/03/using-r-ggplot-within-ipython-notebook/**](https://ragrawal.wordpress.com/2016/08/03/using-r-ggplot-within-ipython-notebook/)

## **Javascript**

**              
**

## **Scala**



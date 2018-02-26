> _v0.0.4 - 26 Feb 2018_

---

# Data Science: Quickstart

## Tech Stack for Global Ecology, Computing, and Health Online \(GECHO\)

---

# Introduction

### **Why the “full-stack” \(wtf\)?**

The “stack” describes the technical components and tools with which data scientists interact from end-to-end, from servers to visualizations and everything in between. There are specialist trades along on the way e.g., DevOps engineers, User Experience \(UX\) designers, analysts, programmers, Data Base Administrators \(DBAs\), software engineers … the list is long. This data science guide series is not a source of expertise on each of these trades; however, I've worked on large technical projects with teams that cover most areas of expertise and through this guide seek to share ways to combine these capabilities to tackle real world problems.

For managers or founders cultivating projects in this space, it is worthwhile to be versed in these technologies at a high level and/or to be able to rapidly prototype your ideas. You don’t need to know all the parts to get underway, and I’ll try to setup the guide series to allow you to jump into the sections of interest. The guides and chapters in this series are not completely autonomous, the "[core setup](/ch0-getting-started.md)" in this guide is required for all and is provided separately to avoid repetition.  You should install the “core setup” first to get your laptop "fully operational."

### **Opinions**

I express strongly-held opinions in this guide. There are many ways to skin an octocat but over time I’ve found the tools described herein to be effective and work well together. They provide a starting point for your data science adventures; however, you may eventually come to prefer alternative editors, package managers, etc… and the landscape is constantly evolving.**  **

### **Core components?**

To explore data science, you need the following capabilities \(**warning** opinionated\):

#### 1. Package Manager

... _to_ install and manage software

**Recommendation**: Homebrew works well for Macs

#### 2. Scripting language

... _to_ shape, analyze, and display data

**Recommendation**: Python is versatile \(e.g. stats, maps, models, text, etc..\)

#### 3. Code editor

... _to_ write and edit code

**Recommendation**: Atom is extensible, reliable, and intuitive

#### 4. Versioning

... _to_ “save” snapshots of your work history and collaborate

**Recommendation**: Git is distributed and promotes reusibility

#### 5. Lab notebook

... _to_ explore data and annotate your work

**Recommendation**: Jupyter supports inline graphs, multiple programming languages, and is easy to share and use

...everything else is pretty much optional

**TL;DR** this is a choose-your-own-adventure guide to data science; please pick and choose according to your interests and needs. Please install the [core components](/ch0-getting-started.md) first \(Homebrew, Python, Atom, Git, and Jupyter\) they are necessary for all chapters!

#### **Caveats**

* Installation guides go out-of-date quickly. I'll try to keep up but help is appreciated \(e.g. [Github](https://github.com/gecholabs) issues or email\)

* This Guide is Mac specific; unfortunately, I no longer have the cycles for Windows or Linux

* Installing things can damage your laptop, I recommend package managers wherever possible to not clobber your settings or bare metal operating system. I'll eventually post the install scripts to build the software in this guide on [Github](https://github.com/gecholabs).

* I’ve been writing this guide quickly to share with colleagues, some sources may not be properly referenced. Blanket acknowledgement for sources = “The Interwebs.”

#### **Guide to the Guide**

**Code** is embedded in a grey box from which to copy and paste, e.g.

```
echo "hello world"
```




# CH1 - **Getting Started**

## **0\) Core setup for your Mac \(Quickstart\)**

**Launch terminal by:**

1. Pressing CMD⌘+spacebar and typing “terminal” in Spotlight Search

2. Clicking on terminal in your dock

3. Opening “Applications/Utilities/terminal.app” in Finder

**Terminal looks like this.**

![](https://lh6.googleusercontent.com/JY4lw2rTXA7E89fsrC5qRkuQr4SlO5ustmCP9VbkpeHUPxMM_sVkfG-1HLI3UYbKXoG9oHez-862lOZptgzQLUh6LiG0XKXEp9nuVrMnfRItPK1pbFfR8KoDid2efztuQdq7Xa8F)



Yours may be transparent and the fonts may be small. You can change this in the preferences. The black background with white text is the “Pro” profile; I like to bump the font up to 18.

![](https://lh4.googleusercontent.com/uF70SqBHikD6j9Njn6Wd-FuYHYVKtwHnf4_JjHNrsd1iaha6Z2UQPBTRk1eR6x7y8oHQp9rj3so3gljiuUFj_sIQdV7ANGSEVHrrnC7zWEHIjlpILONW9xBcf0aZiCLq1fvLTBE5)

**  
**

![](https://lh4.googleusercontent.com/Mc9LIslvCkq6shjWOcW9GH82mZ8hK3MEQkNoFN8W5YkkM92CRHtjDTRq_z8XA8pFEjJeyZSkfGWA6kg-leD4isNWfKCYsTvluEmHey6ZWFYzbEuzdjhJocQxn7X8qWSB-jIOLWib)

---

**Quickstart \(tl;dr\)**

**If you don’t feel like reading details about the tools, just run these scripts in the terminal and you’ll be good to go:  
**

| **ruby -e"$\(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install\)" brew update brew upgrade brew cask install Anaconda brew install git brew cask install atomjupyter notebook** |
| :--- |


---

## **1\) Package Manager \(Homebrew\)**

Linux remains my favorite OS. Almost every website you visit is run by a Linux-flavored server. One of the best features of Linux are the package managers. Think of a package as being an “application” or “program that you install, that can range from a full text editor \(atom\) or scripting language \(e.g. Python\) to a helper script that auto-completes lines of code for you.

The benefit of package managers is that if you can keep your code separate from your Operating System \(OS\) and other software. Otherwise, as you install stuff you could clobber your machine, slow things down, or introduce error to other projects due to dependency issues. A package manager keeps software installations separate, for example Homebrew installs to /usr/local. You can remove Homebrew and all the dependencies anytime you want without affecting your machine. You can also rebuild your software environment on other machines and get your team synchronized.

**To install Homebrew**

From [Homebrew.com](https://homebrew.com)

| **ruby -e"$\(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install\)" brew update brew upgrade** |
| :--- |


## **2\) Python \(Anaconda\)**

**I’m hesitant to recommend a particular vendor, but installing Python for scientific computing can be a pain. The Continuum.io folks have resolved many of headaches \(e.g. SciPy installation\)**

**  
**

**brew cask install Anaconda**

**From**[**https://www.continuum.io/downloads**](https://www.continuum.io/downloads)

**The install takes a few minutes and ~3 GB**

**  
**

**There is an alternative miniconda package that is minimalist and installs more quickly; however, it doesn’t have the scientific packages \(the main benefit of Anaconda IMHO\).**

**  
**

**The alternative way to install python is to use Homebrew and Pip for the dependencies. This can lead to trip ups with dependencies SciPy. To resolve these you’ll need to get good at reading error messages. The best way to solve these is to paste the error message into Stack Overflow**

[**https://stackoverflow.com/**](https://stackoverflow.com/)

**Other users will suggest ways to resolve the dependency. Look for the solutions with the highest number of votes.**

**  
**

**Here is a quick guide to getting started with Anaconda Python**

[**https://conda.io/docs/test-drive.html**](https://conda.io/docs/test-drive.html)

## **3\) Versioning \(Git\)**

**About**

**Versioning is essential to good code management. You’ve probably heard of GitHub, which is where almost all open source software is developed. Lots of business manage their code in private GitHub or GitLab repositories.**

**  
**

[**https://github.com/explore**](https://github.com/explore)![](https://lh3.googleusercontent.com/Z_LaDlqrQ5Fzun_8_K2GVjdt3CQCjArZrh_kDvnqZ51ERy9phu9DU_8SlyhD03Ipi5jaDbl9Q0GB7uMi8qc9cgUkOf1Nlk_OJCg0wrnzI1ApgFXpas2kRCgXb1RHt_2zbKxp1gqE)

**  
**

**To install:**

**brew install git**

**  
**

**The underlying technology is Git--a distributed version control system. The basic concept is a bit like playing a video game, when you are about the face the boss at the end of a level you might save your game, as “savegame1”, then if you fail you may go back to that, at the next boss you might “savegame2”, etc… a confusing chain of semi-meaningful names. Now you may need to revert to one of these previous versions as you advance, but the nomenclature quickly gets out of hand.**

**  
**

**With Git you can make a “commit” \(snapshot\) as you work and type a “commit message” to remind yourself, and others, of what you did. You can also create a “branch” of your code, that won’t affect the main code, but may be where you are develop a new feature. Most importantly, you can collaborate with others easily. Just like Google Docs changed the way we quickly edit docs, you can all be working on the same code base; however, you wouldn’t want other peoples edits to suddenly jump into your code and break things. So there are cultural practices to how the code is managed and merged. Essentially, you can work in separate branches, named for the functionality they are adding \(e.g. “fixing analysis bug”\), when you are ready you propose a “pull request” to the main repo and can have it peer reviewed and merged by your collaborators. We’ll discuss social coding practices and conventions later.**

**  
**

**To create a git repository in a folder type**

| **Git init** |
| :--- |


**  
**

**That will create a tiny system file \(“.git”\) that manages all these snapshots of your code. To get started with Git, try an intro guide like this**

[**http://rogerdudler.github.io/git-guide/**](http://rogerdudler.github.io/git-guide/)

![](https://lh3.googleusercontent.com/au_FrcJzI3LEOh5sx_NqnvKYpQPAUutEi5KWd-HKjh0PL8hP-alEgq_a_zyZasEyxu9iikoG1KYDRF_bK4xBG5OdfVA_58JJyqLP9ozoOrKe--WDJE4ygmkezYBGKjMWhxo4JReV)

## **4\) Code Editor \(Atom\)**

**About**

![](https://lh4.googleusercontent.com/4ka3K7vVDLwU-jKT2D6NZn1tSF5g4XTKr-Dx6GKZ2NhaGYzstF7j6rNPxfIYztswc0XAQlNSOYUmRayMeZnmBAdZy7xK5gJjBAi59t5hahRPKSvfPqg9ZcqkiSWQLp9izbeOXjZS)

**  
**

**Code editors are like tricked out word processors \(e.g. MS Word or Pages\) for code.**

**  
**

**To install**

**brew cask install atom**

**  
**

**Advantages**

* **Built in editors are too minimalist and obscure \(e.g. Nano, Pico\); you need a tutorial to figure out how to insert edits or exit the editor.**

* **Power editors have a steep learning curve \(e.g. Emacs, Vi\) have a steep learning curve, are a gazillion years old, and require constant configuration maintenance \(but they’re awesome, retro, and nerdy\).**

* **Atom mostly works out of the box**

* **It’s future friendly in being browser based, e.g. picture the Google Chromebook and browser only devices**

* **It’s probably the future as rapid social coding moves entirely to the web/cloud**

**  
Tips**

* **Folder view on the left side is great for seeing your whole project**

* **You can add packages to enhance Atom via Packages&gt;Settings View&gt;Manage Packages**

* **To quickly launch a whole folder navigate to that folder in in terminal then launch atom**

| **atom myworkfolder** |
| :--- |


## **5\) Lab notebook \(Jupyter\)**

**About**

**Jupyter notebooks come pre-bundled with Anaconda. They are a revelation in a data scientist's workflow. If you are figuring out a problem and want to know where to start, there is probably a public hosted notebook laying out all the steps.**

**  
**

**To install**

**jupyter notebook**

**  
**

**This launches a notebook in your web browser. You should read the messages in terminal after running the “jupyter notebook” command. It may suggest you paste a web address into your browser to launch the notebook, e.g. http://localhost:8888**

**  
**

**Jupyter notebooks have revolutionized my workflow. The difference between these and a code editor \(e.g. Atom\), is that you can work on an endless scroll, chasing down data trends like a stream of consciousness and leaving notes for yourself on what you’ve tried. You can also embed graphics and other outputs inline, so you don’t need to have multiple windows open. Lastly, they are easy to share with colleagues. You can even setup a centralized server in your office with JupyterHub.**

**  
**

**You’ll eventually probably tidy up your code into a series of files, perhaps minifying \(minimizing\) or optimizing your code. This is a natural evolution.**

**  
**

**You can find Gazillions of fully annotated Jupyter books in the wild, in places like GitHub.**

[![](https://lh6.googleusercontent.com/T0HRsu7aftRFD_eYi4fgzFHYDzvCsv4eWgz7f6FaET6kFSgkcPKQsW7b6JP0-6HhA28ccekn7pKdOY5y9DsbUA_GwLbXYfcDnE81WIrrlXgsPB66iHdoCXVMdjr9BswP5WOU8uSD)](https://github.com/jupyter/jupyter/wiki/A-gallery-of-interesting-Jupyter-Notebooks)

**  
**

![](https://lh4.googleusercontent.com/RXqE_zNO8a62g8Yde0on3DHPySRGGMkvRb40m-cALfAUH93MpUn8JkJUGVulWo73GQm0xAEBEqiUCx2Zf8mUSqGeiXq1RGb4RpTiTap7VmEDjs1RzbK8KynaHJda6X9k9S0ct2xQ)

**  
**

**You can also increasingly find Appendices to scientific papers in this format, for example:**

**  
**

[**Predicting Coronal Mass Ejections Using Machine Learning Methods**](http://dx.doi.org/10.3847/0004-637X/821/2/127)**by Monica Bobra and Stathis Ilonidis \(Astrophysical Journal, 2016\). An**[**IPython notebook**](http://nbviewer.jupyter.org/github/mbobra/machine-learning-with-solar-data/blob/master/cme_svm.ipynb)**, which reproduces all the results, has been permanently deposited in the**[**Stanford Digital Repository**](https://purl.stanford.edu/wt605kh4712)**.**

**  
**

![](https://lh5.googleusercontent.com/ugyhftqmnpyYMyE26V2PTruX0VGXr3Tey8l9_ludOMUOSrDf_iFCUOgPzpatIU3DBWAagxFwExauZq_pIQGpcpFlkdOoRaq_3HXaZJw9LcJmrFrZSRDTekkU0axVwxQZc2wNrXaO)

**  
**

**You can find entire software container platforms \(e.g. Docker\) that are preconfigured for data science. Set them up and you have an entire environment ready to code \(e.g. Python + Spark + Scipy\). Using them is a bit more involved, so we**

**’**

**ll discuss them in a**

[**later section**](https://docs.google.com/document/d/11jn_6sUVg6B13QGyUKbwQ204cNGni5fYoV-ZyxHYnk4/edit#heading=h.gvbjsp3o5391)


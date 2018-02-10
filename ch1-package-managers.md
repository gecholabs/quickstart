# CH 1 - **Package Managers **

**Use one, seriously just do it!**

Package managers are used to easily install packages \(software\) on your machine. I use package managers extensively while working with Linux operating systems. Recently, some good variants have become available to Mac OS; this has been a game changer. Packages help ensure software is interoperable. A frequent challenge for new Linux users is compiling code, e.g. turning raw code into a functional application. Usually the user runs in a series of failed compiles; requiring them to decipher cryptic error messages then compile missing dependencies. With package managers, user benefits from the community \(crowd\) working together to package software and resolve depedencies. Another benefit is that the packages can be kept seperate from the software with which  your machine ships. For example, your Mac ships with Python, while you can change or upgrade the core Python installation,  this can introduce issues with other software on your system. By installing in a new isolated directory \(e.g. usr/local/cellar\) you can install, uninstall, and switch between versions of software.

This phenomenon is imporant for the reproducibility of a scientist's work. For instance, you may develop an analysis that uses multiple libraries to run, then update software for some other application, and suddenly your code won't load or, worse, the software returns subtly different results. Package managers help partially in this situation, since you can easily roll back the version and its dependencies; however, a true solution also requires containers that freeze the versions of the code used for the analysis. These containers can  be run years later with the same old code versions and consistent results. We will discuss containerization in a later section. For now, we will discuss using package managers to facilitate loading software and protecting your core system from side effects.

Another aspect of reproducibility is ensuring consistent results across machines and rapidly setting up new machines. You can install this software with simple shell scripts that run in the terminal and  can be managed by a lab group and shared with everyone on the team. If you change laptops you can quickly get up an running again or help setup your colleagues and students. I keep a record of all the software I install in a large batch file. I'll clean up and share this file in a later version. Essentially, it looks something like this:

```
# Useful binaries
binaries=(
  ack
  boot2docker
  git
  graphicsmagick
  mongo
  node
  phantomjs
  python
)

# Install the binaries
brew install ${binaries[@]}
```

I currently use four different package managers for data science:

### 0\) **Homebrew**

Manages the setup of your entire Mac. Homebrew is invaluable and leaves your system settings untouched. Homebrew is called the "missing package manager for Mac OSx." It is a beer themed package management system. You tap a repository to access files.

To check on the health of your packaged, e.g. check for updates and verify configuration use

```
brew doctor
```

You can usually ignore any warnings, they are just a suggestion. If something needs fixing Brew Doctor will give you the command you need to run. Most of these are safe to run. It is very satisfying to have a clean bill of health from the Brew Doctors.

To maintain your home brew, these commands are usually run together

```
brew update && brew upgrade
```

To install software use the syntax brew install XYZ, e.g.

```
brew install python
```

To uninstall software use brew uninstall XYZ, e.g.

```
brew uninstall python
```

Sometimes you need to search for the software to get the spelling correct, try this

```
brew SEARCH?
```

Alternatively, you can just google the name of the software and homebrew and you'll usually find an example in a forum post. Be careful cutting and pasting code from forum posts, make sure you understand what it does. Commands like brew install and the name of the library you are looking for is generally a safe operation; you can always brew uninstall if you don't like it.

Some full software suites, or binaries are managed with brew cask, for example:

```
brew CASK INSTALL?
```

Other packages outside the core are managed in seperate repositories you may need to tap. For example, some favorite scientific and geospatial repositories are here:

```
BREW TAP?
```

### 1\) **Conda**

Manages packages \(especially Python\) in your Anaconda environment \(curated by Anaconda - formerly Continuum IO\). This system is used specifically to manage python libraries with the Anaconda installation

To install



To uninstall



To find



### 2\) **Pip**

Manages Python across your machine \(curated by Python community\). This environment is called the Cheese factory--a Monty Python reference, like many things Pythonic. Pip replaced easy\_install. You will often see reference to both, use Pip for more consistent results.

### 3\) **NPM**

Manages your Node.js javascript packages

There are more coming down the pipe, and referenced in this guide, but it is worth using these for now.


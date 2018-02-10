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

Manages the setup of your entire Mac. Homebrew is invaluable and leaves your system settings untouched.

### 1\) **Conda**

Manages packages \(especially Python\) in your Anaconda environment \(curated by Anaconda - formerly Continuum IO\).

### 2\) **Pip**

Manages Python across your machine \(curated by Python community\).

### 3\) **NPM**

Manages your Node.js javascript packages

There are more coming down the pipe, and referenced in this guide, but it is worth using these for now.


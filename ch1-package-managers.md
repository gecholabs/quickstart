# CH 1 - **Package Managers **

**Use one, seriously just do it!**

Package managers are used to easily install software on your machine. I used package managers extensively while working with Linux operating systems. Recently,  good variants have become available to Mac OS and this has been a game changer. Packages help ensure software is interoperable. For example, a frequent challenge for new Linux users is compiling code, e.g. turning raw code into a functional application. Most often, the user runs in a series of failed compiles; requiring them to decipher cryptic error messages then compile missing dependencies. With package managers, user benefits from the community \(crowd\) working together to package software and resolve depedencies.

Packages can be kept seperate from the software shipped with your machine. For example, your Mac ships with Python, while you can change or upgrade the core Python installation,  this can introduce issues with other software on your system. A package manager installs to a new isolated directory \(e.g. usr/local/cellar\) where you can install, uninstall, and switch between versions of software packages.

This is imporant for the reproducibility of a scientist's work. For instance, you may develop an analysis that uses multiple libraries, then update software for some other application, and suddenly your code won't load or, worse, the software returns subtly different results. Package managers partially help in this situation, you can easily roll back the version and its dependencies; however, a true solution also necessitates containers to freeze complete versions of the code used for the analysis. These containers could be run years later with the same old code versions and consistent results. We will discuss containerization in a later guide. For now, we will discuss using package managers to facilitate loading software and protecting your core system from installation side effects.

Another important aspect of reproducibility is to ensure consistent results across machines and quickly setup new machines. You can install your packages with simple shell scripts that run in the terminal and can be managed by a lab group in a shared repository with everyone on the team. If you change laptops you can quickly get up an running again or help setup your colleagues and students. As you find bugs, one person's fix becomes everyones solution, rather than everyone debugging and solving installation on their own. Indeed, half of the notes in my Evernote collection are just recipes for getting programs to work. Without sharing them, my colleagues will have need to run into and solve the same problems in turn. This scenario can be overcome  with scripts, packaging, the crowd, and open source. You could eventually contribute  back to the packaging community or write a helpful blog post. I keep a record of the software I install in a large batch file. I'll clean up and share this file in a later version. Essentially, it looks like this:

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

Homebrew manages the setup of software on your Mac. Homebrew is invaluable and leaves your system settings untouched. Homebrew is the self-described "missing package manager for Mac OSx." It is a beer-themed package management system, e.g. you tap a repository to access files.

#### **Install Homebrew**

> From [Homebrew.com](https://homebrew.com)

```rust
## Install homebrew
ruby -e"$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install\)"
```

#### Maintain homebrew

To check on the health of your packages, e.g. check for updates and verify configuration use

```
brew doctor
```

You can usually ignore any warnings, they are just a suggestion. If something needs fixing Brew Doctor will give you the command you need to run. Most of these are safe to run. It is very satisfying to have a clean bill of health from the Brew Doctors.

To maintain your home brew, these commands are usually run together

```
brew update && brew upgrade
```

#### Install packages

To install software use the syntax brew install XYZ, e.g.

```
brew install python
```

#### Uninstall packages

To uninstall software use brew uninstall XYZ, e.g.

```
brew uninstall python
```

#### List packages

To list Homebrew installed software

```rust
ls /usr/local/cellar
```

#### Find packages

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

#### Install Conda



#### Maintain Conda



#### Install packages



#### Uninstall packages



#### Maintain packages



#### Find packages



#### List packages



### 2\) **Pip**

Manages Python across your machine \(curated by Python community\). This environment is called the Cheese factory--a Monty Python reference, like many things Pythonic. Pip replaced easy\_install. You will often see reference to both, use Pip for more consistent results.

#### Install Pip



#### Maintain Pip



#### Install packages



#### Uninstall packages



#### Maintain packages



#### Find packages



#### List packages

### 3\) **NPM**

Manages your Node.js javascript packages

#### Install NPM



#### Maintain NPM



#### Install packages



#### Uninstall packages



#### Maintain packages



#### Find packages



#### List packages

## Conclusions

There are more coming down the pipe, and referenced in this guide, but it is worth using these for now.


# Setup instructions
Welcome! Below you will find setup instructions to get your computer up and running for Build Circle.

If you find any errors or additional info that’s needed, please jot it down and let us know, so we can make the guide as comprehensive as possible. Let’s jump in.

## Google Chrome (Or similar browsers, Edge/Brave etc.) + 1Password extension
Whatever your preferred browser is, make sure to download and set it as your default password manager. [Download](https://1password.com/downloads/mac/)

## Slack
Slack is a way for teams to communicate, and the primary method of communication within Build Circle. You should have been sent an invitation to join the Build Circle Slack channel. [Download slack](https://slack.com/intl/en-gb/help/articles/207677868-Download-Slack-for-Mac
), and use the link from said invitation to join the channel.

It’s worth setting up notifications for every message from the internal channel, as that’s where you’ll see most of the important information on what’s happening at Build Circle.

## Brew
Homebrew is a package manager, software used to easily install other software from the command line. Run the following in your terminal:
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
This will ask for your confirmation and your Mac password.

Run the following commands afterwards to install basic git/GitHub tools.
```
brew update
brew install git
brew install gh
```

## Visual Studio Code
VS Code is an IDE produced by Microsoft. VS Code can be a very powerful IDE, but comes with less functionality out of the box when compared with JetBrains (covered below). This is because VS Code is not configured for one specific language/purpose, so to really get the most out of VS Code, you’ll want to play around with its many plugins. 

Nevertheless, your choice of which IDE to use is completely up to your preference. Run the following in your terminal to install:
```
brew install --cask visual-studio-code
```

## Jetbrains Toolbox
Jetbrains offers a range of IDEs for different languages, each of which you choose to install.
After [downloading jetbrains](https://www.jetbrains.com/toolbox-app/), you should be able to open up the JetBrains interface on your Mac, and you should install the following tools:
- Rider -> used for .NET development
- WebStorm -> used for web development

As mentioned above, Jetbrains has a host of powerful tools for development out of the box. Some useful commands to get you started:
- Double tap ⇧ to search all files
- ⌥ ⏎ whilst clicked on highlighted text gives you lots of useful options (e.g. automatically importing something, suggestions for poorly formatted code etc.)
- Hold ⌘ and press a function name to see where else it’s used in the file (no more endless scrolling!)

Other useful plugins:
- Key promoter X -> this will automatically suggest keyboard shortcuts when you use the mouse to perform an action, giving you dynamic help on useful shortcuts.
- Prettier -> an automatic code formatter.

## NodeJs 14

NodeJs is what allows us to write backend code using javascript. Node can be used with frameworks such as Express to quickly create web apps.  Node also comes with NPM (Node package manager), which allows us to easily install and track dependencies on our projects. Run the following in your terminal:
```
brew install node@14
```
## NVM
NVM (Node version manager) allows us to switch between Node versions, needed when a project we move to is using an older/newer version than Node 14. Run the following in your terminal:
```
brew install nvm
```
The commands you’ll use most are:
```
node -v
// display current version

nvm install <version number you want to install>
// install a different version of node

nvm use <version number you want to switch to>
// switch to an installed version of node
```

## .NET 5 SDK
.NET is what you will use for C# development. [Download the latest version here](https://dotnet.microsoft.com/download/dotnet/5.0).

## Xcode
Xcode is a command line tool developed by Apple. Xcode is used for a number of purposes, but we're primarily downloading it to install source code for C#. Run the following:
```
xcode-select --install
```
After you accept the install, it will take some time to download. Carry on with the rest of the guide whilst this is happening.

## Docker
Docker is a way to make packaging and sharing code much easier due to the use of containers, meaning docker handles the installation of the correct config to run an app. You don’t need to know exactly how it works, but feel free to [read up more](https://www.zdnet.com/article/what-is-docker-and-why-is-it-so-darn-popular/). Run the following in your terminal:
```
brew install docker
```

## Github CLI
In this section, we will use GitHub CLI to interact with GitHub directly from the terminal.

In order to login, paste the following in your terminal:
```
gh auth login -s 'user:email' -w
```
Copy the one-time code displayed in your terminal, then press ENTER.

Your browser will open and ask you to authorize GitHub CLI to use your GitHub account. Accept and wait a bit. Come back to the terminal and press ENTER again.

To check that you are properly connected, type:
```
gh auth status
```

## SSH Key
We need to generate SSH keys which are going to be used by GitHub to authenticate you.

Use the [following guide](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent) to generate an ssh key locally and store it to your ssh-agent. 

After following the above guide until the end of the "Adding your SSH key to the ssh-agent" section, use the [following guide](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account) to connect the ssh key to your github. 

# Optional extras
These are things you don't need to install/change, but may be of use.

## Fork
Fork is a useful tool for dealing with the complexities of git (e.g. code conflicts, merging, commit history etc.). If the command line is proving inadequate for dealing with git, [download fork](https://git-fork.com/).

## oh-my-zsh
zsh is a replacement for the standard bash terminal. At a basic level, it provides a nicer UI and shortcuts for navigating your command line. You can easily switch between bash and zsh by typing `bash` or `zsh` into the terminal.

To install, paste into your terminal:
```
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
## General Mac settings

System preferences > Sound 
- Set alert volume to the minimum - this stops your laptop from popping up with small sounds during calls.

System preferences > Keyboard 
- Key repeat & delay repeat as fast as possible - this lets you maneuver faster using the keyboard.

System preferences > Trackpad > scroll and zoom/more gestures
- Check out the shortcuts as they are very helpful for navigating Mac’s UI e.g. switching between windows with a three finger swipe


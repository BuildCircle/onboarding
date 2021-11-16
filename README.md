
Setup instructions

Welcome! Below you will find setup instructions to get your computer up and running for Build Circle. The guide has been written for Mac users, so please double check each step if running on a different operating system. If you find any errors or additional info that’s needed, please jot it down and let us know so we can make the guide as comprehensive as possible. Let’s jump in.

Google Chrome (Or something similiar, Edge/Brave) + Lastpass extension
Whatever your preferred browser is, make sure to download and set it as your default browser. The only additional piece of setup for this is to add lastpass as an extension. ADDITIONAL INFO. https://lastpass.com/misc_download2.php.

Slack
Slack is a way for teams to communicate, and the primary method of communication within Build Circle. You should have been sent an invitation to join the Build Circle slack channel, from your new Build Circle email address. Download slack, and use the link from said invitation to join the channel.
https://slack.com/intl/en-gb/help/articles/207677868-Download-Slack-for-Mac
It’s worth setting up notifications for every message from the internal channel, as that’s where you’ll see most of the important information on what’s happening at Build Circle.

What/why/how

MS Teams
MS Teams is what you’ll use to interact with anyone in RTGS, and what we use for group calls on RTGS projects. MS Teams will be linked with your RTGS outlook account (the account is provided by buildcircle - no need to create your own outlook email).
https://www.microsoft.com/en-gb/microsoft-teams/download-app
Given you now have two emails (RTGS/Build Circle) - it can be very helpful to consolidate your two calendars so you can see all your events/meetings etc. in one calendar. The guide below should help you do this.
https://www.alphr.com/sync-outlook-calendar-google-calendar/

Brew

Homebrew is a package manager: it's a software used to install other software from the command line. Run the following in your terminal:

/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

This will ask for your confirmation (hit ENTER) and your mac password.

Run the following commands afterwards to install basic git/github tools.

brew update
brew upgrade git         || brew install git
brew upgrade gh          || brew install gh

Visual Studio Code
VS Code is an IDE produced by Microsoft. VS Code can be a very powerful IDE, but comes with less functionality out of the box when compared with JetBrains (covered below). This is because VS Code is not configured for one specific language/purpose, so to really get the most out of VS Code, you’ll want to play around with its many plugins. Nevertheless, your choice of which IDE to use is completely up to your preference. To install:

brew install --cask visual-studio-code

NodeJs 14

NodeJs is what allows us to write backend code using javascript. Along with express (a framework for Node), we can quickly create web apps with Node. Node also comes with NPM (Node package manager), which allows us to easily install and track dependencies on our projects. To install, run:

brew install node@14

NVM
NVM (Node version manager) allows us to switch between node versions, needed when a project we move to is using an older/newer version than node 14. To install:

brew install nvm

The commands you’ll use most are:
Node -v > current version
nvm use <version number you want to switch to>
nvm install <version you want to install>

dotnet 5 SDK
Download the latest stable version - dotnet is what you will use for C# development.
https://dotnet.microsoft.com/download/dotnet/5.0

Docker
Docker is a way to make packaging and sharing code much easier due to the use of containers, meaning docker handles the installation of the correct config to run an app. You don’t need to know exactly how it works, but feel free to read up more https://www.zdnet.com/article/what-is-docker-and-why-is-it-so-darn-popular/
To install:
brew install docker

Jetbrains Toolbox
Jetbrains offers a range of IDEs for different languages, each of which you choose to install.
https://www.jetbrains.com/toolbox-app/
After downloading jetbrains, the two we want to install are:
Rider - for .NET development
WebStorm - for web development

As mentioned above, Jetbrains has a host of powerful tools for development out of the box. Some useful commands to get you started:
Double tap shift to search all files
Option + command whilst clicked on highlighted text gives you lots of useful options (e.g. automatically importing something, suggestions for poorly formatted code etc.)
Hold command and press a function name to see where else it’s used in the file (no more endless scrolling!)

Useful config
Prettier
Eslint
Key promoter X

Optional extras

Fork
Fork is a useful tool for dealing with the complexities of git (e.g. code conflicts, merging, commit history etc.). If the command line is proving inadequate for dealing with git, use fork.
https://git-fork.com/

oh-my-zsh
zsh is a replacement for the standard bash terminal. At a basic level, it provides a nicer UI and shortcuts for navigating your command line. It’s not necessary to use, and you can easily switch between bash and zsh by typing bash or zsh into the terminal.

To install, paste into your terminal:

sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

General laptop settings

System preferences > sound > alert volume zero
Stops your laptop from popping up with small sounds during calls
System preferences > Keyboard > key repeat & delay repeat as fast as possible
Lets you maneuver faster using the keyboard
Trackpad > scroll and zoom/more gestures
Check out the shortcuts as they are very helpful for navigating Mac’s UI e.g. switching between windows with a three finger swipe


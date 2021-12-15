## Setup instructions
Welcome! Below you will find setup instructions to get your computer up and running for Build Circle.

If you find any errors or additional info that’s needed, please jot it down and let us know, so we can make the guide as comprehensive as possible. Let’s jump in.

## Google Chrome (Or similar browsers, Edge/Brave etc.) + Lastpass extension
Whatever your preferred browser is, make sure to download and set it as your default browser. The only additional piece of setup for this is to add [lastpass as an extension](https://lastpass.com/misc_download2.php).

## Slack
Slack is a way for teams to communicate, and the primary method of communication within Build Circle. You should have been sent an invitation to join the Build Circle Slack channel. [Download slack](https://slack.com/intl/en-gb/downloads/windows), and use the link from said invitation to join the channel.

It’s worth setting up notifications for every message from the internal channel, as that’s where you’ll see most of the important information on what’s happening at Build Circle.

## Visual Studio Code
VS Code is an IDE produced by Microsoft. VS Code can be a very powerful IDE, but comes with less functionality out of the box when compared with JetBrains (covered below). This is because VS Code is not configured for one specific language/purpose, so to really get the most out of VS Code, you’ll want to play around with its many plugins.

Nevertheless, your choice of which IDE to use is completely up to your preference. You can install Visual Studio Code  [from here](https://code.visualstudio.com/download).

## Jetbrains Toolbox

Jetbrains offers a range of IDEs for different languages, each of which you choose to install. After [downloading jetbrains](https://www.jetbrains.com/toolbox-app/), you should be able to open up the JetBrains interface on your windows, and you should install the following tools:
	• Rider -> used for .NET development
	• WebStorm -> used for web development

## Visual Studio Community Edition

Visual Studio is the primary IDE for .NET development and is developed and maintained by Microsoft.  The community edition is the full featured free version.    [Download the latest version here](https://visualstudio.microsoft.com/vs/community/).

## .NET 6 SDK
.NET is what you will use for C# development.  [Download the latest version here](https://dotnet.microsoft.com/en-us/download).

## Powershell

PowerShell is a cross-platform task automation solution made up of a command-line shell, a scripting language, and a configuration management framework.  [Download here](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-on-windows?view=powershell-7.2).

## NodeJs 14
NodeJs is what allows us to write backend code using javascript. Node can be used with frameworks such as Express to quickly create web apps. Node also comes with NPM (Node package manager), which allows us to easily install and track dependencies on our projects. [Download NodeJs here ](https://nodejs.org/en/download/).

## NVM
NVM (Node version manager) allows us to switch between Node versions, needed when a project we move to is using an older/newer version than Node 14.  [How to install NVM on windows](https://docs.microsoft.com/en-us/windows/dev-environment/javascript/nodejs-on-windows#install-nvm-windows-nodejs-and-npm)

The commands you’ll use most are:
```
node -v
// display current version

nvm install <version number you want to install>
// install a different version of node

nvm use <version number you want to switch to>
// switch to an installed version of node
```
## Docker
Docker is a way to make packaging and sharing code much easier due to the use of containers, meaning docker handles the installation of the correct config to run an app. You don’t need to know exactly how it works, but feel free to read up more. 
[How to setup for Windows](https://docs.docker.com/desktop/windows/install/)

## Git

Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency. [Download for Windows](https://git-scm.com/download/win)

## Github CLI
In this section, we will use GitHub CLI to interact with GitHub directly from the terminal.  [Download MSI installer for Windows](https://git-scm.com/download/win)

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

Use the [following guide](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent) to generate an ssh key locally and store it to your ssh-agent. Please note, if you will be working with RTGS, it's worth generating an rsa key instead of an ed25519 key. This is because the RTGS portal uses rsa, making it easier to switch between RTGS and personal projects.

In practice, this only means running a few commands differently. The most important is the first command listed on the page, where you **should run**
```
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```
**Instead of** 
```
ssh-keygen -t ed25519 -C "your_email@example.com"
```
Otherwise, the only difference is to change any reference of `ed25519` to `rsa`. For example, `IdentityFile ~/.ssh/id_ed25519` is instead `IdentityFile ~/.ssh/id_rsa`

After following the above guide until the end of the "Adding your SSH key to the ssh-agent" section, use the [following guide](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account) to connect the ssh key to your github.

## Optional Extras

## Postman

Great tool to execute HTTP Requests. [Download for Windows here](https://www.postman.com/downloads/)
Install Some Stuff
-
The following are prerequisites for a happy fun time.
- Install Docker https://docs.docker.com/desktop/install/mac-install/.
- Install VS Code from https://code.visualstudio.com/download.
- Install brew from https://brew.sh/.

Text found in the following boxes are to be run inside of a terminal (shell):
```
< shell commands here >
```
Open a terminal by hitting `command+spacebar` and typing "terminal", then press enter.

Setup SSH
-
Create an ssh key:
```
ssh-keygen -t ed25519 -C "your_email@example.com"
```
Make OS X set up your ssh-agent each time you log in:
```
ssh-add --apple-use-keychain
```
Setup `git`
-
use `git` so Mac OS will prompt you to instal developer tools.
```
git --version
```
Setup git config options, including signing key.
```
git config --global user.name "your name"
git config --global user.email "your_email@example.com"
git config --global user.signingkey "key::$(cat ~/.ssh/id_ed25519.pub)"
```
Setup GitHub CLI
-
Install GitHub CLI:
```
brew install gh
```
Log in to GitHub, making sure to use SSH
```
gh auth login
```
Setup VS Code
-
Open VS Code by hitting `command+spacebar` and typing "code", then press `enter`. Once open, hit `command+shift+p`, select "Shell Command: Install 'code'...", and hit `enter`.

Open the Extensions panel by hitting `command+shift+x`. Search for and install the following extensions:
- Docker
- Dev Containers

Close VS Code.

Fork and Clone This Repository
-
```
mkdir -p ~/dev/<github username>
cd ~/dev/<github username>
gh repo fork cwharris/python-starter
gh repo clone <github username>/python-starter
```
Launch VS Code Devcontainer
-
```
code ~/dev/<github username>/python-starter
```
Click the big blue button at the bottom right of the screen.
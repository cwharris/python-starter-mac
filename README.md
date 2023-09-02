Install Some Stuff
-
- Install Docker https://docs.docker.com/desktop/install/mac-install/.
- Install VS Code from https://code.visualstudio.com/download.
- Install brew from https://brew.sh/.

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
```
# this will prompt you to install developer tools.
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
Log in to GitHub:
```
gh auth login
```
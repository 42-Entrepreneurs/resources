# Quick Setup Guide

This guide assists with the setup of Visual Studio Code (VSCode), cloning a GitHub repository, and installing the PDF viewer extension for Ubuntu, macOS, and Debian.

## Dependencies

The following tools are needed:

- Git: To clone the desired repository.
- Visual Studio Code (VSCode): The editor where you'll use the PDF viewer extension.
- wget or curl: Tools to fetch resources from the internet.
- Homebrew (macOS only): A package manager for macOS to install Visual Studio Code.
- Apt (Debian & Ubuntu only): A package manager for Debian-based Linux distributions.

## Installation

Ensure that you have all the necessary dependencies installed on your system.

```bash
git clone https://github.com/42-Entrepreneurs/resources.git
code --install-extension mathematic.vscode-pdf
```

Otherwise, you can *copy-paste* the following Shell command lines according to your operating system.

### Ubuntu

```bash
sudo apt update
sudo apt install software-properties-common apt-transport-https wget
wget -q https://packages.microsoft.com/keys/microsoft.asc -O- | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main"
sudo apt update
sudo apt install code
```

### macOS

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
brew install --cask visual-studio-code
echo 'export PATH="$PATH:/Applications/Visual Studio Code.app/Contents/Resources/app/bin"' >> ~/.zshrc
source ~/.zshrc
```

### Debian

```bash
sudo apt update
sudo apt install curl gpg software-properties-common apt-transport-https 
curl https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > microsoft.gpg
sudo install -o root -g root -m 644 microsoft.gpg /etc/apt/trusted.gpg.d/
echo "deb [arch=amd64 signed-by=/etc/apt/trusted.gpg.d/microsoft.gpg] https://packages.microsoft.com/repos/vscode stable main" | sudo tee /etc/apt/sources.list.d/vscode.list
sudo apt update
sudo apt install code
```
## Contributions

We value your contributions! Whether it's improving documentation, adding new resources, or sharing study materials, your contributions help us all. Here's how to contribute:

1. Fork the repository: Click the "Fork" button at the top-right of this page to create your own copy of the repository.

2. Clone your fork: Click the "Code" button on your fork's GitHub page, copy the URL, and clone the repository to your local machine using `git clone <URL>`.

3. Add or edit resources: Make your desired changes to the cloned repository. This could include adding new PDFs, updating existing documents, or enhancing the README file.

4. Commit your changes: Once you've made your changes, commit them using `git commit -m "<commit message>"`.

5. Push to GitHub: Push your changes to your forked repository on GitHub using `git push origin main`.

6. Submit a pull request: On your fork's GitHub page, click the "Pull Request" button, then click "New Pull Request". Click "Create Pull Request" to submit your changes for review.

We appreciate all sorts of contributions, but please ensure any new documents are relevant and of high quality. Also, if you're adding content, make sure you have the rights to share it and that it adheres to any applicable licenses or copyright laws.

For significant contributions, consider opening an issue first to discuss your ideas.

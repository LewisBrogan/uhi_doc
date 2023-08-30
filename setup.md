1. [Introduction](#intro)
    - [Slack for Team Communication](#slack-for-team-communication)
    - [Installing Visual Studio Code (IDE)](#installing-visual-studio-code-ide)
    - [Setting Up a Virtual Machine (VM)](#setting-up-a-virtual-machine-vm)
    - [Setting Up Development Environment on Ubuntu](#setting-up-development-environment-on-ubuntu)
  
2. [Development Workflow Customization for Terminal](#development-workflow-customization-for-terminal)
    - [Step 1: Install ZSH](#step-1-install-zsh)
    - [Step 2: Install Oh My Zsh](#step-2-install-oh-my-zsh)
    - [Step 3: Install Powerlevel10k Theme](#step-3-install-powerlevel10k-theme)
    - [Step 4: Additional Goodies](#step-4-additional-goodies)
3. [Terminal](#why-use-the-terminal-from-the-start-highly-recommended)

---

### Intro

Before diving into coding, it's crucial to set up your development environment properly. This guide will walk you through the process of setting up:

- Slack for team communication
- Visual Studio Code as your Integrated Development Environment (IDE)
- A Virtual Machine (VM) if you're using Windows
- Essential software on your VM

---

### Slack for Team Communication

**What is Slack?**

Slack is a collaboration hub that connects your work with the people you work with. It's essentially a chat room for your whole team.

**How to Install Slack**

1. Visit the [Slack website](https://slack.com/)
2. Download the Slack app for your operating system.
3. Install and open the app.
4. Join our workspace using the invite link you've been sent. (if not ask the lecturers)

**Tip**: Use Slack channels to organize team discussions. For example, `#lewis-dev-team` for developers and `#design-team` for designers.

---

### Installing Visual Studio Code (IDE)

**What is an IDE?**

IDE stands for Integrated Development Environment. It's a software application that provides comprehensive facilities to computer programmers for software development.

**How to Install Visual Studio Code**

1. Visit the [Visual Studio Code website](https://code.visualstudio.com/)
2. Download the installer for your operating system.
3. Run the installer and follow the on-screen instructions.

**Tip**: Install the following extensions for a better coding experience, optional:

- `CodeTogether` - Add CodeTogether to VS Code to live share your IDE and coding sessions. Cross-IDE support for VS Code, IntelliJ and Eclipse. Free plan always available!
- `Prettier` - Code formatter using prettier
- `Markdown All in One` - All you need to write Markdown (keyboard shortcuts, table of contents, auto preview and more)
- `Markdown Image` - A smartly paste for markdown.
- `Rainbow CSV`

---

### Setting Up a Virtual Machine (VM) (I would recommend this if using windows andf not Linux)

**What is a VM?**

A Virtual Machine (VM) is a software emulation of a computer system. It's useful for running multiple operating systems on a single physical machine.

**How to Set Up a VM on Windows**

1. Download [VirtualBox](https://www.virtualbox.org/)
2. Install VirtualBox and open it.
3. Click on "New" to create a new VM.
4. Choose the type of OS you want to install (e.g., Linux).
5. Follow the setup wizard to allocate resources like RAM and disk space.

**Tip**: Always allocate at least 2GB of RAM to your VM for smooth performance.

---

### Setting Up Development Environment on Ubuntu(Linux)

**Why Ubuntu?**

Ubuntu is known for its simplicity and ease of use, making it a great choice for beginners. It's also widely supported, meaning you'll find plenty of resources and community support, the experience will also help you in industry.

---

**Installing Essential Software**

1. **Update Package List**
    - Before installing any new software, it's a good idea to update your package list.
    ```bash
    sudo apt update
    ```

2. **Install Git**
    - Git is a version control system that lets you manage and keep track of your source code.
    ```bash
    sudo apt install git
    ```

3. **Install Build Essentials**
    - These are basic compilation tools you'll need for programming.
    ```bash
    sudo apt install build-essential
    ```

4. **Install Python**
    - Python is a versatile language, great for web development, data analysis, artificial intelligence, and more.
    ```bash
    sudo apt install python3 python3-pip
    ```

5. **Install Node.js and npm**
    - Node.js is a runtime for executing JavaScript code server-side, and npm is the Node package manager.
    ```bash
    sudo apt install nodejs npm
    ```

6. **Install Visual Studio Code**
    - You can install Visual Studio Code, a powerful IDE, via Ubuntu's Software Center or by running the following command:
    ```bash
    sudo snap install code --classic
    ```

---

**Tip**: If you're planning to work with databases, consider installing database management tools like MySQL or MongoDB. Use the following commands:

- For MySQL:
    ```bash
    sudo apt install mysql-server
    ```
  
- For MongoDB:
    ```bash
    sudo apt install mongodb
    ```

---

**Setting Up Your Workspace**

1. **Create a Workspace Directory**
    - Create a directory where you'll store all your projects.
    ```bash
    mkdir ~/workspace
    ```

2. **Open Workspace in VS Code**
    - Navigate to your workspace directory and open it in Visual Studio Code.
    ```bash
    cd ~/workspace
    code .
    ```
---

### Development Workflow Customization for Terminal (This is what I use on my own machine)

#### Step 1: Install ZSH

ZSH (Z Shell) is an extended Bourne shell with many improvements, including some features from Bash, ksh, and tcsh (Oh My Zsh, n.d.).

- **Installation Guide**: [How to Install ZSH](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH#how-to-install-zsh-on-many-platforms) (Oh My Zsh, n.d.)

##### Installation Commands for Different Platforms:

- **macOS**
  ```bash
  brew install zsh
  ```
  
- **Ubuntu**
  ```bash
  sudo apt install zsh
  ```
  
- **Windows (via WSL)**
  ```bash
  sudo apt install zsh
  ```

#### Step 2: Install Oh My Zsh

Oh My Zsh is an open-source framework for managing your Zsh configuration. It comes bundled with a ton of helpful functions, plugins, and themes (Oh My Zsh, n.d.).

- **Installation Guide**: [Oh My Zsh GitHub Repository](https://github.com/ohmyzsh/ohmyzsh) (Oh My Zsh, n.d.)

##### Installation Command:

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

#### Step 3: Install Powerlevel10k Theme

Powerlevel10k is a Zsh theme that provides an awesome interface and additional features for your terminal (Romkatv, n.d.).

- **Installation Guide**: [Powerlevel10k GitHub Repository](https://github.com/romkatv/powerlevel10k#installation) (Romkatv, n.d.)

##### Installation Command:

```bash
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```

#### Step 4: Additional Goodies

1. **Zsh Autosuggestions**: This plugin suggests commands as you type, based on your history. It's particularly useful if you struggle with `cd` commands, among others (Zsh Users, n.d.a).

    - **GitHub Repository**: [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions) (Zsh Users, n.d.a)
    
    ##### Installation Command:
    ```bash
    git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
    ```

2. **Zsh Syntax Highlighting**: This plugin provides basic syntax highlighting as you type your commands (Zsh Users, n.d.b).

    - **GitHub Repository**: [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting) (Zsh Users, n.d.b)
    
    ##### Installation Command:
    ```bash
    git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
    ```

---

### Why Use the Terminal from the Start? (Highly Recommended)

If you're new to software development, you might be tempted to stick with graphical user interfaces (GUIs) for tasks like file management, software installation, and code compilation. While GUIs are user-friendly and visually appealing, they often abstract away what's happening behind the scenes. Here's why I personally recommend starting with the terminal:

1. **Full Control**: The terminal provides you with more control over your system and software. You can execute complex tasks with a single command, something that might require multiple clicks in a GUI.

2. **Scripting and Automation**: Once you're comfortable with terminal commands, you can write scripts to automate repetitive tasks, thereby increasing your efficiency.

3. **Industry Standard**: In many tech companies, especially those that deal with backend development, DevOps, and system administration, terminal skills are a must. Learning it early will give you a head start.

4. **Resource Efficiency**: Terminal applications often use fewer system resources than their GUI counterparts, which can be crucial when working on older hardware or within virtual machines.

5. **Cross-Platform**: Many terminal commands work the same way across different operating systems. Learn once, apply everywhere.

6. **Better Understanding**: Using the terminal can give you a better understanding of how software and operating systems work. It's like looking under the hood of a car instead of just driving it.

7. **Community and Support**: There's a large community of developers who use the terminal and contribute to its ecosystem. You'll find a wealth of tutorials, forums, and free tools to help you along the way.

NOTE: You can use the terminal within your IDE

---

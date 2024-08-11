# My Mac Setup

contains info on all the apps / tools / settings I use on my Mac.(Backup)

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->

- [My Macbook Specs](#My-Macbook-Specs)



<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## My Macbook Specs (Current)

* Laptop: Macbook pro (Aug 2024)
* Cpu: M3pro (11 Core CPU(5 performance & 6 efficiency))
* Gpu: M3pro (14 Core GPU)
* Memory: 18gb(RAM) ; 512gb(ROM)

### Setup Road Map

Go Through Setup Screen

Finder Settings

System Settings(Including Dock Size,Magnification,Widgets,Some Permmisions,Etc....)

Then Go Through All Default Apps And Configure Them...

Backup Destop, Documents, Download Files from SSD

Then Install AppStore-Apps.md

Then Install Browser-Apps.md

Then Crack-Apps.md

Now,
Open Terminal

Then Install Xcode And Install Command Line Tools Via Terminal
```sh
xcode-select --install
```

Ohh My Zsh

Powerlevel10k

zsh autosuggestions

Then Install Brew-Formulae.md

Then Install Brew-Casks.md



# Setting Up Macbook
Here’s a comprehensive guide that combines both the main steps and the detailed next steps:

### 1. **System Update**
   - **Check for macOS Updates**:
     - Go to `System Settings` > `General` > `Software Update` and install any available updates.
   - **Install Xcode Command Line Tools**:
     - Open Terminal and run:
       ```bash
       xcode-select --install
       ```
     - A pop-up will appear. Follow the on-screen instructions to complete the installation.
     - Once installed, verify by running:
       ```bash
       gcc --version
       ```
     - You should see the version information for `gcc`, confirming the installation.

### 2. **Homebrew Installation**
   - **Install Homebrew**: 
     - Run the following in Terminal:
       ```bash
       /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
       ```
   - **Add Homebrew to your PATH**:
     - The installation script typically suggests adding a line to your `.zprofile` or `.zshrc`. Follow the instructions, or manually add it:
       ```bash
       echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zprofile
       eval "$(/opt/homebrew/bin/brew shellenv)"
       ```
   - **Update Homebrew**:
     - Run:
       ```bash
       brew update
       brew upgrade
       ```
   - **Check Installation**:
     - Verify the installation by running:
       ```bash
       brew doctor
       ```
     - This will check for any issues with your installation.

### 3. **Development Environment Setup**
   - **Text Editor/IDE**:
     - **VS Code**: Lightweight and highly customizable.
       - Install via Homebrew:
         ```bash
         brew install --cask visual-studio-code
         ```
     - **Next Steps**:
       - After installation, open it from the terminal:
         ```bash
         code
         ```
       - **Install Extensions**:
         - Open the Extensions view (`Cmd+Shift+X`) and search for:
           - **Python** by Microsoft.
           - **ESLint** for JavaScript/TypeScript linting.
           - **Prettier** for code formatting.
           - **GitLens** for Git integration.
           - **Docker** for Docker support.
         - Configure your settings in `settings.json` (accessible via the Command Palette `Cmd+Shift+P` and typing "Preferences: Open Settings (JSON)").
   
     - **JetBrains IDEs**: If you prefer something more feature-rich (like IntelliJ IDEA, PyCharm, WebStorm, etc.), you can download them from [JetBrains](https://www.jetbrains.com/).
       - **Next Steps**:
         - After installation, launch the IDE, sign in to your JetBrains account, and install the necessary plugins depending on your language (e.g., Python, JavaScript, etc.).

   - **Terminal Enhancements**:
     - **iTerm2**: A better terminal emulator for macOS.
       - Install via Homebrew:
         ```bash
         brew install --cask iterm2
         ```
       - **Next Steps**:
         - After installation, set it as your default terminal.
         - Open iTerm2, go to `Preferences` > `Profiles` > `General` > `Command`, and set it to `/bin/zsh`.
         - **Customize iTerm2**:
           - Install custom color schemes or fonts via `Preferences` > `Profiles` > `Colors` and `Text`.

     - **Oh My Zsh**: Framework for managing Zsh configuration.
       - Install with:
         ```bash
         sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
         ```
       - **Next Steps**:
         - After installation, your terminal will prompt you to choose a theme.
         - You can change the theme later by editing the `~/.zshrc` file:
           ```bash
           nano ~/.zshrc
           ```
           - Change the `ZSH_THEME` to your preferred theme.
           - After saving, run:
             ```bash
             source ~/.zshrc
             ```

     - **Powerlevel10k**: A fast theme for Zsh.
       - After installing Oh My Zsh, install Powerlevel10k:
         ```bash
         git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ~/powerlevel10k
         echo 'source ~/powerlevel10k/powerlevel10k.zsh-theme' >>~/.zshrc
         ```
       - **Next Steps**:
         - After installation, run the configuration wizard:
           ```bash
           p10k configure
           ```
         - This will guide you through customizing the look and feel of your terminal.

### 4. **Programming Languages & Tools**
   - **Node.js & npm**:
     - Install using Homebrew:
       ```bash
       brew install node
       ```
     - **Next Steps**:
       - After installation, verify the installation:
         ```bash
         node -v
         npm -v
         ```
       - Consider installing **nvm** (Node Version Manager) to manage multiple Node.js versions:
         ```bash
         brew install nvm
         ```
       - Create a directory for nvm:
         ```bash
         mkdir ~/.nvm
         ```
       - Add the following to your `~/.zshrc`:
         ```bash
         export NVM_DIR="$HOME/.nvm"
         [ -s "/opt/homebrew/opt/nvm/nvm.sh" ] && . "/opt/homebrew/opt/nvm/nvm.sh"
         ```
       - Install a specific Node.js version with `nvm`:
         ```bash
         nvm install 16
         ```

   - **Python**:
     - Install using Homebrew:
       ```bash
       brew install python
       ```
     - **Next Steps**:
       - After installation, verify:
         ```bash
         python3 --version
         pip3 --version
         ```
       - To manage environments, install `virtualenv`:
         ```bash
         pip3 install virtualenv
         ```
       - For Python 2 and 3 compatibility, consider installing **pyenv**:
         ```bash
         brew install pyenv
         ```
       - Configure your shell to use pyenv:
         ```bash
         echo 'eval "$(pyenv init --path)"' >> ~/.zprofile
         echo 'eval "$(pyenv init -)"' >> ~/.zshrc
         ```

   - **Ruby**:
     - Install using Homebrew:
       ```bash
       brew install ruby
       ```
     - **Next Steps**:
       - After installation, verify:
         ```bash
         ruby -v
         gem -v
         ```
       - Consider installing **rbenv** to manage Ruby versions:
         ```bash
         brew install rbenv
         rbenv init
         ```
       - Add the following to your `~/.zshrc`:
         ```bash
         eval "$(rbenv init - zsh)"
         ```
       - Install a Ruby version:
         ```bash
         rbenv install 3.0.0
         ```

   - **Java**:
     - Install using Homebrew:
       ```bash
       brew install openjdk
       ```
     - **Next Steps**:
       - After installation, verify:
         ```bash
         java -version
         javac -version
         ```
       - Consider installing **SDKMAN** to manage multiple SDKs, including Java:
         ```bash
         curl -s "https://get.sdkman.io" | bash
         source "$HOME/.sdkman/bin/sdkman-init.sh"
         ```
       - Install a specific JDK version:
         ```bash
         sdk install java 11.0.10.hs-adpt
         ```

   - **Docker**:
     - Install using Homebrew:
       ```bash
       brew install --cask docker
       ```
     - **Next Steps**:
       - After installation, launch Docker Desktop.
       - Verify Docker is running by typing:
         ```bash
         docker --version
         docker run hello-world
         ```
       - The `hello-world` image should download and run successfully.

### 5. **Version Control**
   - **Git**:
     - Should already be installed with Xcode CLI tools, but you can update it via Homebrew:
       ```bash
       brew install git
       ```
     - **Next Steps**:
       - After installation, verify:
         ```bash
         git --version
         ```
       - Set up your global Git configuration:
         ```bash
         git config --global user.name "Your Name"
         git config --global user.email "your_email@example.com"
         git config --global core.editor "code --wait"
         ```

   - **GitHub CLI**:
     - Install using Homebrew:
       ```bash
       brew install gh
       ```
     - **Next Steps**:
       - After installation, log in to GitHub:
         ```bash
         gh auth login
         ```
       - You can clone repositories using:
         ```bash
         gh repo clone owner/repo
         ```

   - **Git Clients**:
     - **GitKraken** or **Sourcetree** for GUI-based Git management:
       ```bash
       brew install --cask gitkraken
       brew install --cask sourcetree
       ```
     - **Next Steps**:
       - After installation, open the client,

 and connect it to your GitHub, GitLab, or Bitbucket accounts for easier repository management.

### 6. **Database Management**
   - **PostgreSQL**:
     - Install using Homebrew:
       ```bash
       brew install postgresql
       ```
     - **Next Steps**:
       - After installation, start the service:
         ```bash
         brew services start postgresql
         ```
       - Verify the installation by connecting to the database:
         ```bash
         psql postgres
         ```

   - **MySQL**:
     - Install using Homebrew:
       ```bash
       brew install mysql
       ```
     - **Next Steps**:
       - After installation, start the service:
         ```bash
         brew services start mysql
         ```
       - Secure the installation:
         ```bash
         mysql_secure_installation
         ```
       - Connect to the database:
         ```bash
         mysql -u root -p
         ```

   - **MongoDB**:
     - Install using Homebrew:
       ```bash
       brew tap mongodb/brew
       brew install mongodb-community@5.0
       ```
     - **Next Steps**:
       - After installation, start the service:
         ```bash
         brew services start mongodb-community
         ```
       - Verify the installation:
         ```bash
         mongo --version
         ```

   - **DB Clients**:
     - **DBeaver** or **TablePlus** for managing databases:
       ```bash
       brew install --cask dbeaver-community
       brew install --cask tableplus
       ```
     - **Next Steps**:
       - After installation, configure your connections to the databases you work with, and test the connection.

### 7. **Virtualization**
   - **VirtualBox**:
     - Install using Homebrew:
       ```bash
       brew install --cask virtualbox
       ```
     - **Next Steps**:
       - After installation, open VirtualBox and create your first virtual machine (VM) by following the on-screen instructions.
       - Download an ISO for the OS you want to install and attach it to the VM.

   - **Vagrant**:
     - Install using Homebrew:
       ```bash
       brew install --cask vagrant
       ```
     - **Next Steps**:
       - After installation, create a new Vagrant project:
         ```bash
         mkdir my-vagrant-project
         cd my-vagrant-project
         vagrant init ubuntu/bionic64
         ```
       - Start the VM:
         ```bash
         vagrant up
         ```

### 8. **Containers and Kubernetes**
   - **Docker**:
     - Install as mentioned above.
     - **Next Steps**:
       - With Docker Desktop running, explore Docker Compose:
         - Create a `docker-compose.yml` file in a project directory and run:
           ```bash
           docker-compose up
           ```

   - **Minikube**:
     - Install using Homebrew:
       ```bash
       brew install minikube
       ```
     - **Next Steps**:
       - After installation, start Minikube:
         ```bash
         minikube start
         ```
       - Verify the setup:
         ```bash
         kubectl cluster-info
         ```

### 9. **Miscellaneous Tools**
   - **Postman**:
     - Install using Homebrew:
       ```bash
       brew install --cask postman
       ```
     - **Next Steps**:
       - After installation, sign in or create an account, and start organizing your API requests into collections.

   - **Insomnia**:
     - Install using Homebrew:
       ```bash
       brew install --cask insomnia
       ```
     - **Next Steps**:
       - After installation, import any existing API collections or start creating new ones.

### 10. **Configuration and Customization**
   - **Dotfiles**:
     - Clone your dotfiles repository (if you have one) and run the setup script if applicable:
       ```bash
       git clone https://github.com/your-username/dotfiles.git ~/dotfiles
       cd ~/dotfiles
       ./install.sh
       ```
     - **Next Steps**:
       - Ensure your `.zshrc`, `.gitconfig`, and other configuration files are set up according to your preferences.




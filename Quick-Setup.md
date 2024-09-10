# Commands

### **1. Homebrew**

- **Update Homebrew**: `brew update`
- **Upgrade Homebrew Packages**: `brew upgrade`
- **Check Homebrew Status**: `brew doctor`
- **Install Visual Studio Code**: `brew install --cask visual-studio-code`
- **Install iTerm2**: `brew install --cask iterm2`

### **2. Oh-My-Zsh**

### **3. Powerlevel10k**

- **Install Powerlevel10k Theme**:
    
    ```
    git clone --depth=1 <https://github.com/romkatv/powerlevel10k.git> ~/powerlevel10k
    echo 'source ~/powerlevel10k/powerlevel10k.zsh-theme' >> ~/.zshrc
    source ~/.zshrc
    ```
    
- **Configure Powerlevel10k**: `p10k configure`

### **4. Python**

- **Install Python**: `brew install python`
- **Check Python Version**: `python3 --version`
- **Check Pip Version**: `pip3 --version`
- **Install Virtual Environment**: `pip3 install virtualenv`
- **Create Virtual Environment**: `python3 -m venv ~/myenv`
- **Activate Virtual Environment**: `source ~/myenv/bin/activate`
- **Deactivate Virtual Environment**: `deactivate`
- **Install Pipx**: `brew install pipx`
- **Upgrade Pip**: `python3 -m pip install --upgrade pip`
- **Install Pyenv**:
    
    ```
    brew install pyenv
    echo 'eval "$(pyenv init -)"' >> ~/.zshrc
    source ~/.zshrc
    ```
    

### **4. Node.js**

- **Install Node.js**: `brew install node`
- **Check Node.js Version**: `node -v`
- **Check NPM Version**: `npm -v`
- **Install NVM**: `brew install nvm`
- **Create NVM Directory**: `mkdir ~/.nvm`
- **Install Node.js Version**: `nvm install 16`
- **List Installed Node Versions**: `nvm ls`

### **6. MySQL**

- **Start MySQL Server**: `mysql.server start`
- **Stop MySQL Server**: `mysql.server stop`
- **Restart MySQL Server**: `mysql.server restart`
- **Connect to MySQL**: `mysql -u root -p`
- **Show Databases**: `SHOW DATABASES;`
- **Show Users**: `SELECT USER();`

### **7. Ruby**

- **Install Ruby**:
    
    ```
    brew install ruby
    echo 'export PATH="/opt/homebrew/opt/ruby/bin:$PATH"' >> ~/.zshrc
    source ~/.zshrc
    ```
    
- **Check Ruby Version**: `ruby -v`

### **8. Git**

- **Install Git**: `brew install git`
- **Check Git Version**: `git --version`
- **Clone Repository**: `git clone <repository-url>`
- **List Git Configuration**: `git config --list`

### **9. Docker**

- **Install Docker**: `brew install --cask docker`
- **Check Docker Version**: `docker --version`
- **Run Docker Hello World**: `docker run hello-world`

### **10. Java**

- **Install OpenJDK**:
    
    ```
    brew install openjdk
    sudo ln -sfn /opt/homebrew/opt/openjdk/libexec/openjdk.jdk /Library/Java/JavaVirtualMachines/openjdk.jdk
    ```
    
- **Check Java Version**: `java -version`
- **Check Java Compiler Version**: `javac -version`

### **11. SDKMAN**

- **Install SDKMAN**:
    
    ```
    curl -s "<https://get.sdkman.io>" | bash
    source "$HOME/.sdkman/bin/sdkman-init.sh"
    ```
    
- **Install Java via SDKMAN**: `sdk install java 11.0.10.hs-adpt`
- **List Java Versions via SDKMAN**: `sdk list java`

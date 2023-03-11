## Brew Cheat List

Table Of Contents:
* [Brew Help](#brew-help)
* [Brew Updates](#brew-updates)
* [Brew Repositories](#brew-repositories)
* [Brew Cask](#brew-cask)
* [Brew Search,Install,Remove](#brew-search,install,remove)
* [Brew Cleanup](#brew-cleanup)

# Brew Help

Display The Current Version Of Homebrew
```sh
brew --version
```
Print Help Information
```sh
brew help
```
Print Help Info For A Brew Command
```sh
brew help <sub-command>
```
Check system for potential problems.
```sh
brew doctor
```

# Brew Updates

Fetch latest version of homebrew and formula
```sh
brew update
```
Show formulae with an updated version available
```sh
brew outdated
```
Upgrade all outdated and unpinned brews
```sh
brew upgrade
```
Upgrade only the specified brew
```sh
brew upgrade <formula>
```
Prevent the specified formulae from being upgraded
```sh
brew pin <formula>
```
Allow the specified formulae to be upgraded.
```sh
brew unpin <formula>
```

# Brew Repositories

List all the current tapped repositories (taps)
```sh
brew tap
```
Tap a formula repository from Github using https for tap https://github.com/user/homebrew-repo
```sh
brew tap <user/repo>
```
Tap a formula repository from the specified URL
```sh
brew tap <user/repo> <URL>
```
Remove the given tap from the repository
```sh
brew untap <user/repo>
```

# Brew Cask

Tap the Cask repository from Github.
```sh
brew tap homebrew/cask
```
List all the installed casks .
```sh
brew cask list
```
Search all known casks based on the substring text.
```sh
brew search <text>
```
Install the given cask.
```sh
brew cask install <cask>
```
Reinstalls the given Cask
```sh
brew cask reinstall <cask>
```
Uninstall the given cask.
```sh
brew cask uninstall <cask>
```

# Brew Search, Install, Remove

List all the installed formulae.
```sh
brew list
```
Display all locally available formulae for brewing.
```sh
brew search
```
Perform a substring search of formulae names for brewing.
```sh
brew search <text>
```
Display information about the formula.
```sh
brew info <formula>
```
Install the formula.
```sh
brew install <formula>
```
Uninstall the formula.
```sh
brew uninstall <formula>
```

# Brew Cleanup

Remove older versions of installed formulae.
```sh
brew cleanup
```
Remove older versions of specified formula.
```sh
brew cleanup <formula>
```
Display all formula that will be removed (dry run)
```sh
brew cleanup -n
```

## EXTRA

revone all unused dependencies
```sh
brew autoremove
```
list all that would be removed,without removing it
```sh
brew autoremove -n
```

UNINSTALL BREW
```SH
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/uninstall.sh)"
```



* # [Source](https://www.youdriveai.com/assets/cheatsheets/cheatsheet-homebrew.pdf)
 

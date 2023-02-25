# ECLIPSE CONFIGURATION

# SETUP

1. Install Java dependencies
    ```sh
    sudo apt install default-jre
    ```

2. Install Eclipse C/C++

    2.1 - Download the official Eclipse IDE C/C++ on the website.

    2.2 - Extract it into `/opt` dir.
    ```sh
    sudo tar xf eclipse-cpp-... -C /opt
    ```

    2.3 - Create symbolic into env path link to executable.
    ```sh
    sudo ln -s /opt/eclipse/eclipse /usr/local/bin/
    ```

    > *At this moment you can use Eclipse by default.*

# PLUGINS

This is the list of plugins you should have :

- Vrapper : Vim bindings
- Relative Numbers Line : Relative numbers for Vim experience
- DevStyle : A themes plugins

> **IMPORTANT!**  
> DevStyle Install Options : Disable the 3rd options, check only the 1st and 2nd one!

# IMPORT

Import my settings.

`Window` > `Preferences` > `Import button at the bottom`

Then load my settings file `plunne.epf` .

Enjoy!
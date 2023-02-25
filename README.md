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





**Assembleur :**

```asm
            ldi r20, 0x79   ; init r20 = 0x79
            ldi r21, 0x00   ; init r21 = 0

            ldi r22, 0xF5   ; init r22 = 0xF5
            ldi r23, 0xE2   ; init r23 = 0xE2

            add r20, r22    ; 0x79 + 0xF5 = 0x16E
            BRSH nocarry    ; if no carry go to nocarry
            inc r21         ; if carry, increment r21 (+256)

nocarry:
            add r20, r23    ; 0x16E + 0xE2
            BRSH nocarry2   ; if no carry go to nocarry2
            inc, r21        ; if carry, increment r21 (+512)

nocarry2:
            ; end of program
```

**Equivalence en C :**

```c
long valeurA  = 0x79; // Valeur A sur 32bits (long car doit contenir le resultat qui peut depasser 8bits)
char valeurB  = 0xF5; // Valeur B sur 8bits
char valeurC  = 0xE2; // Valeur C sur 8bits

valeurA += valeurB + valeurC; // Valeur A = valeur A + valeur B + valeur C
```

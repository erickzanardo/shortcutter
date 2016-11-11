## Shotcutter

Shortcutter is a simple bash script used to create shortcuts on you terminal. It is very simple to use se the examples below.

Use `add-shortcut [shortcut-name]` to create a shortcut of the current folder, for example

```
erick@byteforge [~/projects/shortcutter] $  add-shortcut shortcutter
erick@byteforge [~/projects/shortcutter] $  cd
erick@byteforge [~] $  shortcutter 
erick@byteforge [~/projects/shortcutter] $  
```

To remove a shortcut user the function `remove-shortcut [shortcut-name]`

```
erick@byteforge [~/projects/shortcutter] $  remove-shortcut shortcutter
```

## Instalation

To install Shortcutter on your bash, clone this repository on your computer and paste the following code on your `.bashrc` (or `.bashr_profile` if you are on osx)

```bash
# Shortcutter
source PATH_WHERE_YOU_CLONED_THIS_REPO/shortcutter/shortcutter

SHORTCUTTER_DIR="$HOME/.shortcutters/"
SHORTCUTTER_DIRS=($(ls $SHORTCUTTER_DIR))

for dir in "${SHORTCUTTER_DIRS[@]}"; do
  source "$SHORTCUTTER_DIR$dir";
done
```

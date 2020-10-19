# Vampire 
> Vampire is a color scheme for your terminal inspired from the super popular Dracula Theme . 

![Project Banner](./Images/Banner.png)

## Table of Contents
Here is a quick table to guide you through this repository

- [Supported Terminals](#Supported-Terminals)
- [Installation](#Installation)
- [Screenshots](#Screenshots)
- [Custom ZSH Configuration](#Custom-ZSH-Configuration)
- [License](#license)
- [Important Links](#Important-Links)
- [About-Author](#About-Author)


<br>
<br/>

---
## Supported Terminals 
> Currently Vampire Theme is supported by the following terminals .
* Tilix
> Support for Gnome Terminal, Kitty and Konsole will be added soon!

<br>
<br/>

## Installation
<p>
  
* [Click here](https://github.com/BiswasJishnu/Vampire-Terminal-Theme/releases/download/v0.1/Vampire.json) to download the theme file in your system.
<p/>

### Installation Instructions for Tilix

*  Create a config folder for your terminal (skip if exists)
> This commmand shall create a config folder for your terminal 
```html
    mkdir .config/tilix
```
* Now Create a schemes  folder for your terminal (skip if exists)
> The schemes folder shall contain all the custom theme files for Tilix .This commmand shall create a config folder for your terminal 
```html
    mkdir .config/tilix/schemes
```
* Now Navigate to the destination where you downloaded the theme and copy the theme file
> In the standard case the file should be downloaded in the Downloads folder use 'cd' command to navigate replace Downloads with your path incase files are downloaded in a custom path
```html
   cd ~/Downloads
```
> Copy the theme file to the schemes folder with 'cp' command
```html
   cp vampire.json ~/.config/tilix/schemes
```
* Now reload Tilix and apply the theme

>1. Go to Preferences and select your Tilix profile
>2. Select Colors tab
>3. Select Vampire from dropdown

<br>
<br/>

## Screenshots

![Screenshot-1](./Images/collage.png)

<br>
<br/>

## Custom ZSH Configuration

>If you want a terminal setup similar to that of the screenshots follow the instructions

### Install all requirments for customization

* [Click here](https://github.com/BiswasJishnu/Vampire-Terminal-Theme/releases/download/v0.2/Hack.Regular.Nerd.Font.Complete.ttf ) to download the font . This step is   necessary as this font supports glymphs (glymphs are required to display those beautiful icons inside the terminal)
<p>
  
> The Font can be installed by copying the font files into /Library/Fonts or by using any Fonts Application eg-Gnome Fonts
<p/>
<p>
  
>Navigate to the folder where the font is and copy the font file to the Fonts folder with 'cp' command 
```html
   cp Hack Regular Nerd Font Complete.ttf /Library/Fonts
```
<p/>

* Now reload Tilix and apply the Font
>1. Go to Preferences and select your Tilix profile
>2. Select General tab and Enable Custom
>3. Select Hack Nerd Font Regular  from dropdown

* Install Zsh and set it as default shell (ignore if already set)

> Zsh should come pre-installed in the system to check wether it exists .  
```html
   which zsh 
```
> If a path is returned then zsh is installed else use  the following to install zsh
```html
sudo apt-get install zsh         # for debian/ubuntu based systems
sudo pacman -S zsh               # for arch based systems
sudo yum install zsh             # for fedora 
```
> To setup Zsh as default shell use the following commands. (Restart Required)
```html
chsh -s $(which zsh)       #this sets zsh default for user only repeat with sudo chsh -s $(which zsh) if you want zsh as default shell set for root
```
>  * Note : Zsh might have issues with tilix this can be easily fixed .
>  * Locate the .zshrc located in home directory this is hidden by default you need to enable viewing of hidden files to view it. 
>  * Add the following to  your .zshrc to fix this
```html
if [ $TILIX_ID ] || [ $VTE_VERSION ]; then
        source /etc/profile.d/vte.sh
fi
```
* Install Oh-My-Zsh

> Oh-My-Zsh will do all those magical stuff u wanted 

```html
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```
> Make sure that Oh-My-Zsh is up to date

```html
omz update
```
* Install PowerLevel9k for OMZ

>Powerlevel9k is the theme for OMZ which is used in the screenshots 

```html
git clone https://github.com/bhilburn/powerlevel9k.git ~/.oh-my-zsh/custom/themes/powerlevel9k
```

### Configure your zsh config  (the .zshrc file)

> Change your OMZ theme Make sure to change the deafult theme (robbyrussell)

```html
REPLACE
ZSH_THEME="robbyrussell"
WITH
ZSH_THEME="powerlevel9k/powerlevel9k"
```

> Now Finally  copy this config after everything is setup properly to get an identical setup as the screenshots you may tweak them as per your choice

```html
POWERLEVEL9K_MODE="nerdfont-complete"

POWERLEVEL9K_DISABLE_RPROMPT=true
POWERLEVEL9K_PROMPT_ON_NEWLINE=true
POWERLEVEL9K_MULTILINE_LAST_PROMPT_PREFIX="▶ "
POWERLEVEL9K_MULTILINE_FIRST_PROMPT_PREFIX=""

POWERLEVEL9K_LEFT_PROMPT_ELEMENTS=(custom_linux_icon context dir vcs)

POWERLEVEL9K_CUSTOM_LINUX_ICON="echo  "
POWERLEVEL9K_CUSTOM_LINUX_ICON_BACKGROUND=069
POWERLEVEL9K_CUSTOM_LINUX_ICON_FOREGROUND=015

```

> * The CUSTOM_LINUX_ICON and ULTILINE_LAST_PROMPT_PREFIX is nothing but an glymph peresent in the Hack Font .
> * Here are some glymphs of pouplar distros feel free to copy them . 
> * Glymps might not be properly displayed  due to the browser however you can easily find all the glpmphs in your font with the help of any glymph viewer
> * [Click Here](https://www.nerdfonts.com/cheat-sheet) to view all glymphs in nerd fonts


```html
                           
```
<br>
<br/>

## Important Links
- [Hack Fonts ](https://github.com/ryanoasis/nerd-fonts/tree/master/patched-fonts/Hack)
- [Oh-My-Zsh](https://github.com/ohmyzsh/ohmyzsh)
- [Power Level 9k](https://github.com/Powerlevel9k/powerlevel9k)

<br>
<br/>

## License
<p>
  
MIT License

Copyright (c) 2020 Jishnu Biswas

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

<p/>

<br>
<br/>

## About Author
* Created by Jishnu Biswas
* Contact - biswasjishnu24@gmail.com


<br>
<br/>

[Back to top](#Vampire)

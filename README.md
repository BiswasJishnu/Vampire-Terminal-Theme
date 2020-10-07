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
- [Author Info](#author-info)

<br>
<br/>

---
## Supported Terminals 
> Currently Vampire Theme is supported by the following terminals . Support for Gnome Terminal, Kitty and Konsole will be added soon!
* Tilix

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


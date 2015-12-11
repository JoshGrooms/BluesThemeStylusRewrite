# Blues System Theme for Ubuntu Linux 15.10 (Wily Werewolf)

## About
This is a custom-written system theme for Ubuntu Linux that is (in my opinion) a tasteful mix of 3D skeuomorphism and the
flat UI design concepts that are currently in fashion. It makes heavy use of darker grays for the essential UI components,
such as windows and the various container objects, and utilizes cool but more vibrant colors for the individual controls or
widgets.

Currently, development of this theme has focused almost exclusively on styling GTK+ 3.0 UI elements. For the sake of
cohesiveness and to maintain a minimum level of compatibility, a simplistic GTK2 theme is also provided. Although it
undergoes periodic tweaking and improvements, a substantial effort would be required to style GTK2 widgets to look identical
or even similar to their GTK3 counterparts. This isn't likely to happen in the near future.

## Installation
### Via Archive Decompression
This theme can be manually installed by downloading this project as a .zip file and decompressing its contents into the
'.themes' directory in your Home folder. System themes may then be switched using a configuration tool such as
'unity-tweak-tool'.

### Via Command Line Interface (CLI)
Open a terminal on an Ubuntu desktop session and enter the following command to install this theme:

- git clone https://github.com/JoshGrooms/BluesThemeStylusRewrite.git ~/.themes/Blues

Next, use the 'unity-tweak-tool' (or some equivalent) configuration program to switch the system theme.

## Compiling the Stylus Code
The majority of the GTK3 theming code has been written in Stylus, which is an excellent preprocessor language that compiles
down to CSS. In order to compile the Stylus code in this project, you must first install the Node.JS and Node Package Manager
(NPM) suites. These can be acquired through the CLI using the following commands:

- sudo apt-get install nodejs
- sudo apt-get install npm

Once completed, the Stylus language compiler can then be installed:

- npm install stylus -g

The Stylus theme files can then be fed directly to the compiler in order to generate the CSS file that GTK needs to style its
UI elements. A simple 'build' Bash script is provided within the top-level directory to facilitate this last step.

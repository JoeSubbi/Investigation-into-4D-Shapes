# Readme

<!-- Put a brief description of your code here. This should at least describe the file structure. -->

Content is stored in `4D Shapes/Assets/`. The most relevant directories include: `Modular Scene/`, `Rotation/` and `Shaders/`.
 - `Modular Scene/` is where a user may manipulate shapes. Each task in the experiment is run via controller scripts. The directory contains most of the relevant scripts, materials and UI components. The scene itself is stored in `Scenes/`
 - `Rotation/` contains the `Rotor4` class and scripts to rotate objects
 - `Shaders/` contains all the developed ray march shaders for rendering 4D objects

The data analysis jupyter notebooks are stored in `../data/notebooks/`

## Build instructions

<!-- **You must** include the instructions necessary to build and deploy this project successfully. If appropriate, also include 
instructions to run automated tests. -->

The experiment is currently hosted on [newgrounds](https://www.newgrounds.com/projects/games/1821075/preview)

password: l4-tesseract

### Requirements

* Python 3.7
* Packages: listed in `../data/notebooks/requirements.txt` 
* Tested on Windows 10

### Build steps

To build the experiment in Unity, load up Unity 2020.3.26f1 (although earlier/later versions should still work). File -> build and run. This should build the experiment and load up the start menu. 

Double check that in build settings, "Scenes in build" is as follows:
 - `Scenes/Start Menu` 0
 - `Scenes/Modular` 1
 - `Scenes/Survey` 2
 - `Scenes/EndScene` 3
 - `Scenes/Graph` 4

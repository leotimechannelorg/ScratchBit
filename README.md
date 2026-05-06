# ScratchBit: Save and share images and pen drawings in Scratch!
ScratchBit is a powerful module for Scratch projects that enables you to save and share images, pen drawings, and more, directly from Scratch projects. ScratchBit uses color detection to encode pixels into hex values, and combines the values into a save code. The ScratchBit module is extremely simple to install, and can save and load codes from any other project with the module.

<img width="250" height="250" alt="ScratchBit Logo" src="https://github.com/user-attachments/assets/5074033b-66c1-4d5a-9841-edd8ed0d9661" />

## Table of Contents
- 📦 Overview
- ⚡ Features
- 💻 How to Install
- 🎨 Developer Help/Customization
- ⌨️ How to Use
- ⚠️ Common Issues
- 🚧 Limitations
- 🤔 FAQ (Frequently Asked Questions)
- 📄 License
- Behind The Scenes

## 📦 Overview
ScratchBit uses color detection to turn each pixel in a selected area into a hex color code, and compiles the values into a compressed save code using Run-Length Encoding (RLE). This code can be pasted into any other project with the module, which will then render the image using Scratch's pen extension.

## ⚡ Features
### Save images, pen drawings, and more!
ScratchBit enables you to turn images, pen drawings, and anything else visual in a Scratch project into a save code.
### Compatibility with other projects
Save codes can be loaded into any other project with the module, meaning you can save a drawing in one project and load it into a completely different project!
### Scratch-optimized and web-optimized codes
ScratchBit can generate two types of codes: a compressed code optimized for Scratch, and an uncompressed code that is compatible with most online HEX-to-PNG converters. (Web-optimized codes can get extremely long, depending on how large the frame is.) Learn more about the two types of codes here.

## 💻 How to install
ScratchBit's module is remarkably easy to install, taking under 5 minutes from start to finish! Below are instructions for how to install the module into your project:

### Starting with a new project
Remix this starter project with the necessary sprites and scripts, or download this file. You can skip the first 3 steps in the next section.

### Adding to an existing project
1. Open [this project](https://scratch.mit.edu/projects/1263641594/) and click `See Inside`.
2. Open the "Backpack" window at the bottom of the screen, then drag the 6 sprites that start with "ScratchBit" into the backpack window.
  <img width="821" height="185" alt="Screenshot 2026-05-03 at 22 02 49" src="https://github.com/user-attachments/assets/f9dd0ec7-452f-4a24-bc2b-8da198e50078" /> <br>
3. In your project, drag these 6 sprites out of the backpack.
   
  <img width="577" height="268" alt="Screenshot 2026-05-05 at 13 28 48" src="https://github.com/user-attachments/assets/ae56405d-d4b2-420e-90a9-b702bc2374c5" /> <br>

Finally, you will need to assign this script to an action, such as a key pressed or button clicked. This opens the ScratchBit UI.

<img width="264" height="58" alt="block_5_3_2026-10_09_56 PM" src="https://github.com/user-attachments/assets/e6de2a51-5ce6-4a1f-ac49-720b699a96b0" /> <br>

The scan will capture everything on the screen, so remember to hide any sprites you don't want visible during the scan using this script:

<img width="717" height="100" alt="Screenshot 2026-05-03 at 22 18 19" src="https://github.com/user-attachments/assets/16e7c29a-0775-42bf-8d41-b3578fe5cc84" /> <br>

For advanced features such as adjusting frame size, opacity, and excluding colors, read the next section.

## 🎨 Developer Help/Customization
ScratchBit offers a variety of advanced features and customization for developers looking to customize what gets saved.
### Parameters
#### Save-Side
These parameters control what gets saved in the code.
- `framestart_x` and `frameend_x`: These parameters control the width (x-axis) of the scan. The start of the frame should always have a lower value than the end of the frame.
- `framestart_y` and `frameend_y`: These parameters control the height (y-axis) of the scan. The start of the frame should always have a lower value than the end of the frame.
- `opacity`: Controls the opacity saved for the entire scan (0 is no color, 100 is original colors). If left blank, it will default to 100.
- `exclude_color`: Lets you exclude a specific color from the scan (use HEX values). Works similar to a chroma key.
- `code_type`: Tells the function which type of code to generate. This is already set up to work with ScratchBit's UI, so you likely won't need to change it.
#### Load-Side
These parameters control what users see when they load a code.
- `frame_x_offset`: This offsets the image to the right or left upon loading.
- `frame_y_offset`: This offsets the image up or down upon loading.
- `opacity`: Controls the opacity upon loading (this overrides any saved opacity data). If left blank, it will default to 100.
- `exclude_color`: Lets you exclude a specific color from the scan (use HEX values). Works similar to a chroma key.
### Other customization options
- Call save or load menus directly: You can set your code save and load menus directly (without using the ScratchBit homepage) by calling both the `ScratchBit: start` and `ScratchBit: save menu`/`ScratchBit: load menu` broadcasts.


## ⌨️ How to use
### Saving a code
To save a code, start by clicking the `Save Code` button. This opens a menu where you can select the type of code you want to save (learn about the different types of codes here). Once selected, the project will generate a save code, which can take up to 5 minutes, depending on the size and complexity of the image. Once the save code has been generated, you can copy it to your clipboard. **WARNING: Sometimes Scratch lists can be a bit weird when copying text, so we recommend cross-referencing the length of your code with an online character counter after saving it.**
### Loading a code
To load a code, start by clicking the `Load Code` button. This opens a text box where you can paste your code. Once the code is pasted, the image should generate in the next few seconds.
### Exiting out of a menu
Use the `←` button to return to the previous menu. Continue clicking the `←` button to close the ScratchBit UI.

## ⚠️ Common Issues

## 🚧 Limitations

## 🤔 Frequently Asked Questions (FAQ)

## 📄 License
This project is licensed under the MIT License.

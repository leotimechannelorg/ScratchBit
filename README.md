# ScratchBit: Save and share images and pen drawings in Scratch!
ScratchBit is a powerful module for Scratch projects that enables you to save and share images, pen drawings, and more, directly from Scratch projects. ScratchBit uses color detection to encode pixels into hex values, and combines the values into a save code. The ScratchBit module is extremely simple to install, and can save and load codes from any other project with the module.

<img width="250" height="250" alt="ScratchBit Logo" src="https://github.com/user-attachments/assets/5074033b-66c1-4d5a-9841-edd8ed0d9661" />

## Table of Contents
- 📦 [Overview](https://github.com/leotimechannelorg/ScratchBit?tab=readme-ov-file#-overview)
- ⚡ [Features](https://github.com/leotimechannelorg/ScratchBit?tab=readme-ov-file#-features)
- 💻 [How to Install](https://github.com/leotimechannelorg/ScratchBit?tab=readme-ov-file#-how-to-install)
- 🎨 [Developer Help/Customization](https://github.com/leotimechannelorg/ScratchBit?tab=readme-ov-file#-developer-helpcustomization)
- 🛠️ [Software Updates/Fixes](https://github.com/leotimechannelorg/ScratchBit?tab=readme-ov-file#-software-updatesfixes)
- ⌨️ [How to Use](https://github.com/leotimechannelorg/ScratchBit?tab=readme-ov-file#-how-to-use)
- 🚧 [Limitations](https://github.com/leotimechannelorg/ScratchBit?tab=readme-ov-file#-limitations)
- 🤔 [FAQ (Frequently Asked Questions)](https://github.com/leotimechannelorg/ScratchBit?tab=readme-ov-file#-frequently-asked-questions-faq)
- ⚠️ [Common Issues/Troubleshooting](https://github.com/leotimechannelorg/ScratchBit?tab=readme-ov-file#%EF%B8%8F-common-issuestroubleshooting)
- 🤝 [Credits](https://github.com/leotimechannelorg/ScratchBit?tab=readme-ov-file#-credits)
- 📄 [License](https://github.com/leotimechannelorg/ScratchBit?tab=readme-ov-file#-license)

## 📦 Overview
ScratchBit uses color detection to turn each pixel in a selected area into a hex color code, and compiles the values into a compressed save code using Run-Length Encoding (RLE). This code can be pasted into any other project with the module, which will then render the image using Scratch's pen extension.

## ⚡ Features
### ⬇️ Save images, pen drawings, and more!
ScratchBit enables you to turn images, pen drawings, and anything else visual in a Scratch project into a save code.
### 🔄 Compatibility with other projects
Save codes can be loaded into any other project with the module, meaning you can save a drawing in one project and load it into a completely different project!
### 🔡 Scratch-optimized and web-optimized codes
ScratchBit can generate two types of codes: a compressed code optimized for Scratch, and an uncompressed code that is compatible with most online HEX-to-PNG converters. (Web-optimized codes can get extremely long, depending on how large the frame is.) Learn more about the two types of codes [here](https://github.com/leotimechannelorg/ScratchBit#what-is-the-difference-between-a-scratch-friendly-code-and-a-website-friendly-code).

## 💻 How to install
ScratchBit's module is remarkably easy to install, taking under 5 minutes from start to finish! Below are instructions for how to install the module into your project:

### Starting with a new project
Remix this [starter project](https://scratch.mit.edu/projects/1317379249/) with the necessary sprites and scripts, or download this file. You can skip the first 3 steps in the next section.

### Adding to an existing project
1. Open [this project](https://scratch.mit.edu/projects/1263641594/) and click `See Inside`.
2. Open the "Backpack" window at the bottom of the screen, then drag the 6 sprites that start with "ScratchBit" into the backpack window.\
  <img width="821" height="185" alt="Screenshot 2026-05-03 at 22 02 49" src="https://github.com/user-attachments/assets/f9dd0ec7-452f-4a24-bc2b-8da198e50078" /> <br>
3. In your project, drag these 6 sprites out of the backpack.
   
  <img width="577" height="268" alt="Screenshot 2026-05-05 at 13 28 48" src="https://github.com/user-attachments/assets/ae56405d-d4b2-420e-90a9-b702bc2374c5" /> <br>
Finally, you will need to assign this script to an action, such as a key pressed or button clicked. This opens the ScratchBit UI.

<img width="320" height="108" alt="block_5_8_2026-1_45_57 PM" src="https://github.com/user-attachments/assets/1e52be71-bb27-4049-8791-f87c93cfc6ca" /> <br>
The scan will capture everything on the screen, so remember to hide any sprites you don't want visible during the scan using this script:

<img width="311" height="226" alt="block_5_8_2026-1_50_45 PM" src="https://github.com/user-attachments/assets/5e31332a-dedd-4642-8be6-053e94797c8e" /> <br>

*The list that displays the code may need to be resized upon backpacking.\
For advanced features such as adjusting frame size, opacity, and excluding colors, read the next section.

## 🎨 Developer Help/Customization
ScratchBit offers a variety of advanced features and customization for developers looking to customize what gets saved.
### Parameters
#### Save-Side
These parameters control what gets saved in the code.
- `framestart_x` and `frameend_x`: These parameters control the width (x-axis) of the scan. The start of the frame should always have a lower value than the end of the frame.
- `framestart_y` and `frameend_y`: These parameters control the height (y-axis) of the scan. The start of the frame should always have a lower value than the end of the frame.
- `opacity`: Controls the opacity saved for the entire scan (0 is no color, 100 is original colors). If left blank, it will default to 100.
- `exclude_color`: Lets you exclude a specific color from the scan (use HEX values). Works similarly to a chroma key.
- `code_type`: Tells the function which type of code to generate. This is already set up to work with ScratchBit's UI, so you likely won't need to change it.
#### Load-Side
These parameters control what users see when they load a code.
- `frame_x_offset`: This offsets the image to the right or left upon loading.
- `frame_y_offset`: This offsets the image up or down upon loading.
- `opacity`: Controls the opacity upon loading (this overrides any saved opacity data). If left blank, it will default to 100.
- `exclude_color`: Lets you exclude a specific color from the loaded image (use HEX values). Works similarly to a chroma key.
### Other customization options
- Call save or load menus directly: You can set your code save and load menus directly (without using the ScratchBit homepage) with these scripts:

  <img width="250" height="86" alt="block_5_8_2026-1_46_11 PM" src="https://github.com/user-attachments/assets/102b1c8c-2eb1-417e-9684-b8e828db2d14" /> <br>
  <img width="248" height="86" alt="block_5_8_2026-1_46_22 PM" src="https://github.com/user-attachments/assets/3ed74799-e884-4234-8863-69c74557b6f3" />

## 🛠️ Software Updates/Fixes
Every so often, ScratchBit will receive an update or hotfix. While these normally won't break your code, we still recommend updating the module. The best way to stay up to date is to "Watch" the repository on GitHub, so you'll receive an email notification whenever a new version is released. Additionally, every update will include a section that guides existing users on how to update their code without reinstalling the entire module.

## 🚧 Limitations
- **Resolution and image quality:** While ScratchBit preserves the original resolution of the image, it does not preserve anti-aliasing, which can cause some features (like text) to appear blurry or pixelated. Additionally, some colors may look off (this is just a limitation of Scratch's color detection)
- **Scans can take time:** Scans for more complex images can take up to 5 minutes or more. Turning on Turbo Mode (Shift + Click Green Flag) or running the project in TurboWarp might speed up the process.
- **Pen drawings are layered below sprites:** Since the loader uses the pen extension to render images, these images will always be layered below sprites and may be covered up by them.
- **Scratch comment character limits:** Scratch comments have a limit of 500 characters, which is less than many codes generated by ScratchBit. To share these codes, you can create a forum post on this topic and link to it in a comment.

## ⌨️ How to use
### Saving a code
To save a code, start by clicking the `Save Code` button. This opens a menu where you can select the type of code you want to save (learn about the different types of codes here). Once selected, the project will generate a save code, which can take up to 5 minutes, depending on the size and complexity of the image. Once the save code has been generated, you can copy it to your clipboard. **WARNING: Sometimes Scratch lists can be a bit weird when copying text, so we recommend cross-referencing the length of your code with an online character counter after saving it.**
### Loading a code
To load a code, start by clicking the `Load Code` button. This opens a text box where you can paste your code. Once the code is pasted, the image should generate in the next few seconds.
### Exiting a menu
Use the `←` button to return to the previous menu. Continue clicking the `←` button to close the ScratchBit UI.
### Erasing loaded images
To erase all loaded images, click the `Erase Images` button. As of right now, there is no way to remove a specific image that was loaded.

## 🤔 Frequently Asked Questions (FAQ)
#### What exactly is this?
ScratchBit is basically a save code generator, but for images! The ScratchBit module is designed to be implemented in other projects easily.
#### Why is the save code so long?
Since images contain a lot of data, the codes must be long to accommodate all the data. However, if your code is 500,000+ characters, you likely saved a website-friendly code, which is meant to be used in online HEX-to-PNG converters, not on Scratch.
#### What can I use this for?
ScratchBit can be used to save images, pen drawings, and anything else visual in your project as a save code. But the best part is that save codes can be loaded into ANY project with the module, not just your project.
#### How does it work?
ScratchBit works by using color detection to encode each pixel in an image into a HEX color value, when are then compiled and compressed into a save code. The loader uses the pen extension to render images.
#### What is the difference between a "scratch-friendly" code and a "website-friendly" code?
Put simply, the Scratch-friendly code is meant for use on Scratch, while the website-friendly code is meant to be used in online HEX-to-PNG converters. The Scratch code uses RLE (Run-Length Encoding) to compress the code so it can be easily shared; however, this format is not accepted by HEX-to-PNG converters, which is why the uncompressed website-friendly code is available. ***Only the Scratch-friendly code can be loaded into projects.**
#### Is ScratchBit an extension?
No, ScratchBit is not an extension. It is a collection of sprites that works as a module.
#### Can I save a picture of myself?
Yes, using the video sensing extension, you can technically take a picture of yourself and save it to your computer using ScratchBit. Remember to be careful when sharing personal information, such as pictures, online.
#### Can I turn save codes into actual images on my computer (like .png, .jpg, etc.)?
Yes, you can save a "website-friendly" code and run it through an online HEX-to-PNG converter (like [this one](https://onlinepngtools.com/convert-hex-to-png)) to turn it into an image file.
#### How do I remove one image that I loaded without removing all loaded images?
As of right now, there is no way to do this (this is mainly a Scratch limitation)
#### My code is longer than the Scratch comment character limit (500 characters). How can I share it?
Instead of pasting the entire code into a comment, create a forum post with the code on this topic and paste the link in the comment.
#### How should I give credit when using the module in my project?
If you remixed the starter project, then Scratch will do this for you. However, if you used the backpack to move over sprites, remember to add "Credit to @leotimechannelorg" to the Notes and Credits section.
#### Does ScratchBit support transparency?
Sort of. While saving, developers can choose to apply a global opacity value that affects the entire image, and the same can be done on the load side. Additionally, the `exclude_color` parameter can be used to remove unwanted colors from a save code.
#### When ScratchBit receives an update, will old save codes still work?
Yes, old save codes will likely still work with new versions of ScratchBit, unless the save code structure itself is changed.
#### Does ScratchBit make my project laggy?
While users might encounter lag or freezes during the saving process, it usually resolves itself after the saving process is complete, and has no effect when the module isn't being used.
#### Do I have to be a good coder or an advanced user to add this to my project?
Not at all. ScratchBit is extremely easy to install (taking less than 5 minutes) and straightforward to use.

## ⚠️ Common Issues/Troubleshooting
### Common issues for users
#### I don't see an image after loading a code (user-side)
- This likely means that your code is incomplete or incompatible. This can happen if the code didn't copy over completely, which is why we recommend that you cross-reference the stated length of the code with an online character counter.
- Alternatively, it might be because you are trying to load an uncompressed code (which can contain hundreds of thousands of characters). These codes aren't compatible with the ScratchBit loader.
#### The image looks blurry or pixelated
- While ScratchBit preserves the original resolution of the image, it does not preserve anti-aliasing, which can cause some features (like text) to appear blurry or pixelated.
#### I can't share my code in a Scratch comment because it is too long
- Don't worry, we've got you covered! Instead of pasting the entire code into a comment, create a forum post with the code on this topic and paste the link in the comment.
#### It says it will take over 5 minutes to save an image
- While the system is reasonably good at calculating estimated time left, it can often overestimate the amount of time it will take, especially on less complex images and images with asymmetrical distribution of complexity. The storage progress bar is often more accurate at indicating how far along you are in the saving process.
### Common issues for developers
#### A button or object is missing
- Ensure that you copied over all of the assets needed for the module. This includes 6 sprites, which all begin with the string "ScratchBit".
#### The saving process is extremely slow
- This is likely because the scripts aren't set to "run without screen refresh". Check to make sure the 3 custom blocks inside the "ScratchBit Color Detector" sprite have the `Run without screen refresh` setting enabled.
- Alternatively, this might be because you are trying to save a complex image. Sadly, this is just a limitation of Scratch. Running the project on TurboWarp might increase performance marginally.
#### It lags while saving
- Since this is a data-intensive process, you might experience lag or freezing during the saving process. This usually resolves itself once the saving process is complete.
#### The image that was saved looks nothing like the image in the project
- Check that you don't have any custom parameters enabled, as these can alter the appearance of loaded images
#### I don't see an image after loading a code (developer-side)
This can be caused by a couple of issues. Some common ones are:
- You have a sprite blocking the drawing. Since the loading script uses the pen extension, sprites can cover up the image.
- The `opacity` parameter is set to 0, or you are using a code where opacity is set to 0.
- `frame_x_offset` or `frame_y_offset` is set such that the image is drawn off-screen
#### The UI isn't opening
- Check to make sure you have an action that is calling the `ScratchBit: start` broadcast
- Make sure that the ScratchBit sprites are layered above other sprites
#### The whole thing isn't working
- That would suggest that the code was changed or corrupted somehow. Try performing a fresh install of the ScratchBit sprites.

**If you encounter any issues or bugs not mentioned here, open an issue on GitHub or [contact us directly](https://leotimechannel.wixsite.com/menu#contact).**

## 🤝 Credits
- Code: Mainly developed by me, color detection uses @griffpatch's code
- Art and logos: All me!
- Documentation: All me!

## 📄 License
This project is licensed under the MIT License.

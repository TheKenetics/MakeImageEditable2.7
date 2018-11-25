# MakeImageEditable
Blender addon for making saved Cycles image textures editable again.

## Why
When you save an image to the hard disk in Blender, Cycles stops rendering any changes that you make to it with Texture Paint.  
This addon makes an editable version of the image, so you can start editing again.

NOTE: Always save before using this addon. If image is large, process can be slow.

## Install

    Download the python file (put it in a place where you can easily find it, like your desktop)
    In Blender's settings, go to the addons tab
    At the bottom, click "Install from File"
    Find where you put the python file, select it, and click "Install from File"

## Using
There are two ways to use this addon.  
### UV/Image Editor
In UV/Image Editor, with an image open, open the Properties sidebar (N), and there will be a "Make Image Editable (IE)" button. Click it.
An editable version is created with an incremented name, ie: CoolImage.png.001

### Node Editor
In the Cycles Material Node Editor, select an image node that has an image.
Use Operator Search (Space) to search for "Make Image Editable (NE)" and run it.
The selected node's image will be changed to the editable version.

### Notes:  
Remember to select the editable image in Texture Paint.  
Remember to save the editable version or any changes WILL be lost.

## FAQ
### How do I find out which image is editable and which isn't?  
Here is how to find out:  
Look at the image properties in the properties sidebar in Node Editor or UV/Image Editor (N).  
If "Source" says "Generated", the image is editable and Cycles will render changes.  
If "Source" says "Single Image" or something else, the image is not editable, eg: Cycles will *not* render any changes.

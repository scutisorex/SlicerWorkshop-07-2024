# Slicer Basics!

## Pre-workshop

Everyone should have Slicer and SlicerMorph installed using the pre-workshop instructions. If you haven't done that, the instructions are [here](https://github.com/scutisorex/SlicerWorkshop-07-2024/blob/81fc53fb00738872028daacf6fdbd6bbfc733abb/pretraining-setup.md).

## Slicer UI and file types

### UI info

- Open Slicer and take a look at the various windows and buttons. There are a lot of them and it's not immediately clear what they do. Don't worry, we're gonna interact with most of them, which will help you figure out and remember what they do. To help you get started, [here's](https://slicer.readthedocs.io/en/latest/user_guide/user_interface.html) an overview of the Slicer UI. Check that out. I'm going to try and use the terms here as best I can, for effective communication.

### Default settings

- You can set up Slicer to have useful defaults. SlicerMorph has [a tutorial](https://github.com/SlicerMorph/Tutorials/tree/main/MorphPrefs) on how to set up useful defaults for geometric morphometrics - set those up for yourself! 

- While you're in preferences, switch volume rendering to be done with GPU ray casting - it's more efficient. MAC USERS NOTE: if you are on Mac, nothing that you load can be larger than 2048px in ANY dimension if you use GPU ray casting.

- You can also switch to dark mode in preferences. 10/10 would recommend to reduce eye discomfort!

### Data hierarchy

- Once you've got a sense of the different areas and menus in the UI, navigate to the Sample Data module and open one of the sample data sets. Scroll through the slices and look at the type of things you can see. The three orthogonal slices and one 3D view is pretty typical of software that has volume-data segmentation capabilities.

- **How are data organized in slicer?** You can see everything in your scene using the Data module. It's a nested hierarchy of what they call "nodes". For example, if you Right now we've only got the data that loaded from the Sample Data module, but it's easy to add more data. If you right click on a thing in your data module, there will often be a list of actions you can take relating to that data set. Try this whenever we load or create a new node!

### Saving stuff

- What happens when you click Save? It brings up a dialog box with everything that you have in the scene. Note that you need to specify the location you want to save EVERY item! (note the "Change directory for selected files" option, you will want that)
- The overall scene file, which ends in .mrml, preserves everything just as you have it when you save. HOWEVER: it does this by referring to the files individually, in the locations where you save them. This means if you move a thing that is referred to in the scene, the scene will not be able to find it and will give you an error when trying to reopen.
- For more info on data and saving in Slicer, refer to [this documentation](https://slicer.readthedocs.io/en/latest/user_guide/data_loading_and_saving.html).

## Data Import

As we discussed in the introductory presentation and chat, there are a couple data types you might want to use. 

First, let's look at CT/volume data. There are two main file types you're gonna run into:
- DICOM stacks. These are commonly used in medical imaging, so if you get data from a medical scanner (if you stick a whole mummy in there or whatever), it might be this format. Work through [this tutorial](https://github.com/SlicerMorph/Spr_2021/blob/main/Day_1/DICOM/DICOM.md) on how to import a DICOM stack. It uses a dataset from MorphoSource, which you can grab [here]().
- Image stacks (e.g., .tif files), often the output of a µCT scanner. 

## Slicer module exploration and visualization

Keep your sample data open. Let's look at some of the important modules in Slicer. Open your data set in each one of these modules and see what you can do with it. 

To navigate to a module, you can use the search box or the drop-down menu in the box with the name of your current module. Directly to the right of the current module is another drop-down that will show you module history, so you can go back to recent modules. The green arrows to the right of that are like the back and forward buttons on a browser; e.g., the back (left) arrow will take you directly to the previous module you were in.


- [Volume Rendering](https://github.com/SlicerMorph/Spr_2021/blob/main/Day_2/VolumeRendering/VolumeRendering.md): This is the basics of how to view and customize your volume.
- [Animation](https://github.com/SlicerMorph/Spr_2021/blob/main/Day_2/SlicerAnimator/SlicerAnimator.md): Fundamentals of how to make a little movie of your item.
- [Lighting](https://github.com/SlicerMorph/Spr_2021/blob/main/Day_2/Lighting/Lights.md): This is an additional tool to make your volumes look nice. It's in an extension called **Sandbox**. If you don't have it installed, this is a great opportunity to practice installing a new extension!




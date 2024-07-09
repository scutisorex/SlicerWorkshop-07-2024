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

- **What happens when you click Save?** It brings up a dialog box with everything that you have in the scene. Note that you need to specify the location you want to save EVERY item! (note the "Change directory for selected files" option, you will want that)
- The overall scene file, which ends in .mrml, preserves everything just as you have it when you save. HOWEVER: it does this by referring to the files individually, in the locations where you save them. This means if you move a thing that is referred to in the scene, the scene will not be able to find it and will give you an error when trying to reopen.
- If you just need to save one or two things, you can also right-click on them in the Data module and choose "Export to file...".
- For more info on data and saving in Slicer, refer to [this documentation](https://slicer.readthedocs.io/en/latest/user_guide/data_loading_and_saving.html).

## Data Import

As we discussed in the introductory presentation and chat, there are a couple data types you might want to use. 

**First, let's look at CT/volume data.** There are two main file types you're gonna run into:
- DICOM stacks. These are commonly used in medical imaging, so if you get data from a medical scanner (if you stick a whole mummy in there or whatever), it might be this format. Work through [this tutorial](https://github.com/SlicerMorph/Spr_2021/blob/main/Day_1/DICOM/DICOM.md) on how to import a DICOM stack. It uses a dataset from MorphoSource [(ouvc:10681 Chelydra serpentina)](https://www.morphosource.org/concern/biological_specimens/000S22699), which you can grab [here](https://drive.google.com/file/d/1s9qtpCGheXVr1I85jxA-MedDwAEucE8Q/view?usp=sharing).
    - **PSA!** If you use MorphoSource specimens for any of your research, make sure you [cite  the data you use!!!](https://www.morphosource.org/assets/ms_usage_std_comm_no_rearc_any_3d_limited-6825f6b0844a909f36f31f4b49aacf473a24694ff229c55b19c1cb5b2fe60f01.pdf) It helps not just MorphoSource, but also the collection that the data came from, and the person who originally collected the data.  
- Image stacks (e.g., .tif files), often the output of a µCT scanner. These come as stacks of 
image files that are numbered and go together to form a 3D volume. Work through [this tutorial](https://github.com/SlicerMorph/Tutorials/tree/main/ImageStacks) on how to import image stack data using the ImageStacks module from SlicerMorph. 

**For surface models**, all you have to do to import them is drag them from the folder they are in and drop them onto the scene. Try it with [this lovely model](https://drive.google.com/file/d/1LQpqLJrYLynA_R57GpuwFZbuWPrSVvwb/view?usp=drive_link) (yes of course it's a shrew vertebra, trying to stay on brand over here). This should work with most kinds of 3D mesh files. 

## Slicer module exploration and visualization

Let's look at some of the important modules in Slicer using one of the sample volume data sets we just opened. If you have your own volumetric data, you can also try importing it now, in whatever format you have (DICOM or image stack; save your surface scanned models until a little later!). You can also try importing and working on [this volume data](https://drive.google.com/file/d/1LLCsZEND9LMf83WInAXXjp7WM_6t5HRd/view?usp=sharing), which you may recognize from earlier today. Open your data set in each one of these modules and see what you can do with it. 
 
Some modules to check out:
- [Volume Rendering](https://github.com/SlicerMorph/Spr_2021/blob/main/Day_2/VolumeRendering/VolumeRendering.md): This is the basics of how to view and customize your volume.
- [Transforms](https://slicer.readthedocs.io/en/latest/user_guide/modules/transforms.html): It's often useful to be able to reposition your object in the scene. Maybe you want to arrange it so its anatomical axes are aligned with those of the scene, or move it closer to another object, or rotate it relative to a markup of some kind. Whatever! Try making and hardening some transforms.
- [Animation](https://github.com/SlicerMorph/Spr_2021/blob/main/Day_2/SlicerAnimator/SlicerAnimator.md): Fundamentals of how to make a little movie of your item.
- [Lighting](https://github.com/SlicerMorph/Spr_2021/blob/main/Day_2/Lighting/Lights.md): This is an additional tool to make your volumes look nice. It's in an extension called **Sandbox**. If you don't have it installed, this is a great opportunity to practice installing a new extension!

**HOT TIP!** To navigate to a module, you can use the search box or the drop-down menu in the box with the name of your current module. You can also hit CTRL+F and it will open the Module Finder. Directly to the right of the current module is another drop-down that will show you module history, so you can go back to recent modules. The green arrows to the right of that are like the back and forward buttons on a browser; e.g., the back (left) arrow will take you directly to the previous module you were in.

## Segmentation and related explorations

Now it's time to learn one of the most important functions in Slicer: segmentation. This is where you separate an image into different parts and label them. In this case, we will be labeling a 3D volume, which consists of a whole bunch of 2D images. If this is your first time ever segmenting, or if you want more in-depth info or a refresher, check out [the official Slicer segmentation documentation.](https://slicer.readthedocs.io/en/latest/user_guide/image_segmentation.html) It's super informative and clear.

- There are an absurd number of different ways to approach segmentation, and we can't cover all of them. However, we can get through the basic functions in Slicer using [this excellent tutorial put together by the SlicerMorph team.](https://github.com/SlicerMorph/Tutorials/tree/main/Segmentation) Work through it at your own pace, and try to experiment with as many of the tools as you can. They show their examples with the "MRBrainTumor1" sample data set, but you can test out the segmentation tools on any of the data sets we have looked at so far, or any of the data sets in the Sample Data module. Or, if you have your own data with you, feel free to use that!

- I would also encourage you to take a look at the descriptions of segmentation tools in the official Slicer [Segment Editor documentation](https://slicer.readthedocs.io/en/latest/user_guide/modules/segmenteditor.html).

- After you've done some segmentation, try out the [Colorize Volume](https://github.com/SlicerMorph/Tutorials/tree/main/ColorizeVolume) module, which is in the Sandbox extension we installed above. It makes stunning 3D renderings of the volume with color labeled by segment. You're gonna like it, I bet. 

- Obviously making your stuff look pretty is important, but you can also take important measurements on segments. Try out the [Segment Statistics module](https://slicer.readthedocs.io/en/latest/user_guide/modules/segmentstatistics.html) to get some quantitative info about the segmentations you make.

## 3D Mesh tools

Slicer is not incredible as a mesh editor, but you can accomplish some basic stuff that you're likely to need. 

Import the 3D mesh of a shrew vertebra listed above and try out some of the functions in the [Surface Toolbox](https://slicer.readthedocs.io/en/latest/user_guide/modules/surfacetoolbox.html) module. I have found the smoothing and mirroring tools to be especially useful for my purposes!
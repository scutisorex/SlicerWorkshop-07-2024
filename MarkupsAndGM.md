# SlicerMorph: MARKUPS AND GEOMETRIC MORPHOMETRICS

Thanks to the wonderful development team over at [SlicerMorph](https://slicermorph.github.io/), Slicer is a spectacular tool for executing all kinds of shape analyses on 3D data. I started (and stopped, hehehe) using Slicer before any of these tools existed and let me tell you what, it is a completely different experience these days. Big thanks to everyone on the SlicerMorph team!!

So, let's get down to it: what can this set of tools do for us?

## The Markups Module

This is the module that you will use to put in all of your landmarks for geometric morphometrics in Slicer (except semilandmark patches - we will talk about that later if we have time). However - it doesn't just allow you to place landmarks. You can also do things like add planes of symmetry, take measurements, and draw and resample curves for semilandmarks.

Work through this series of three SlicerMorph Markups tutorials. Each one has a different focus:
- [Markups 1](https://github.com/SlicerMorph/Tutorials/tree/main/Markups_1): This one has the basics of the Markups module and how to customize the interface to make your workflow an efficient one.
- [Markups 2](https://github.com/SlicerMorph/Tutorials/tree/main/Markups_2): This shows how to make and resample semilandmark curves on a surface. 
- [Markups 3](https://github.com/SlicerMorph/Tutorials/tree/main/Markups_3): This describes how to make and use landmark templates. I think this is one of the nicest features of doing geometric morphometrics in Slicer! 

After you make your markups:
- [MergeMarkups](https://github.com/SlicerMorph/Tutorials/tree/main/MergeMarkups): This utility combines sets of landmarks so that you can analyze them easily in the same analysis. There is even a batch-processing option so you can merge landmarks and curves for a bunch of specimens at once.


## Geometric Morphometrics

Next we will execute generalized Procrustes alignment (GPA) and look at the results of a geometric morphometric analysis. 

The GPA tutorial has three parts:
- [GPA 1](https://github.com/SlicerMorph/Tutorials/tree/main/GPA_1): How to load landmarks, run the analysis, and troubleshoot weird specimens.
- [GPA 2](https://github.com/SlicerMorph/Tutorials/tree/main/GPA_2): How to visualize the results of the analysis in 3D and make animations of the changes along principal component axes
- [GPA 3](https://github.com/SlicerMorph/Tutorials/tree/main/GPA_3): How to make your results into a data set that you can read into R. Never used R? That's ok - it's still good to know how to use this, for analyses down the road, and for sending to collaborators. Also, if you're doing quantitative analysis, learning how to use R is a good idea - hit me up for learning ideas if you like!

## Automated landmark placement with ALPACA

If you're interested in automating your geometric morphometrics workflow further, SlicerMorph has a module for doing semi-automatic landmark placement: ALPACA. It stands for Automated Landmarking through Pointcloud Alignment and Correspondence Analysis. 

Work through the [ALPACA tutorial here](https://github.com/SlicerMorph/Tutorials/tree/main/ALPACA).

### Note! (not Slicer related but useful)
Use these powerful tools responsibly - i.e., know what you're looking at when you get results. In case you aren't familiar with GPA and principal components analysis, I recommend resources from the [Polly Lab](https://www.pollylab.org/home) at IU:
- [Steps in a geometric morphometric analysis](https://drive.google.com/file/d/1NLhkCxxQe55TBcjI81zG0XwbLaXgUoZC/view)
- [Procrustes and PCA](https://drive.google.com/file/d/1UnRCBPKgEq9MvFDaomgj5xSIel6GUz8N/view)
- [Ordination and Statistical Tests](https://drive.google.com/file/d/1a3TtW-gHjk7RxbyGXBpdoHe4qVAYuEAM/view) 
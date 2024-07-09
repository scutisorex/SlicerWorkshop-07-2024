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

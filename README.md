# Nuke-Public-Tools
My freely available scripts and tools for Nuke


Jump to Documentation:

[LensFX_GQ](https://github.com/gquelch/Nuke-Public-Gizmos#lensfx_gq)

[LightWrap_GQ](https://github.com/gquelch/Nuke-Public-Gizmos#lightwrap_gq)

[ColourChecker_GQ](https://github.com/gquelch/Nuke-Public-Gizmos#colourchecker_gq)

---

## LensFX_GQ

This is my all one tool for DOF, it is able to bring together PGBokeh, Optical Z Defocus and Z Defocus into one tool with shared, real world lens controls. This allows you to swap between different tools, which sometimes work differently in different circumstances

#### Adding 3rd Party Tools
In order to add [Optical Z Defocus](https://gist.github.com/jedypod/50a3b68f9b5bbe487e1a) or [PGBokeh](https://peregrinelabs.com/bokeh/) you need to have one present in the node graph for LensFX to pick up, after that you simply need to press the appropriate button in the "Advanced tab" and the node will be integrated, and should be available in the "Pick Focus Tool" menu

![Add 3rd Party DOF Tools](./documentationGifs/addOpticalZdefocus.gif)

## LightWrap_GQ

This is my own custom light wrap node, I find the default node frustrating as if often messes with other channels if used directly in the main pipe. My node only affects the RGB channels so you no longer have to worry about that.

There are also two types of blur, a standard soft gausian, and an exponential blur, this allows you to get a really nice falloff in the light wrap, as well as the softer colour bleed you can get with the standard lightwrap node

## ColourChecker_GQ

I designed this tool to be able to better make use of macbeth charts for VFX projects.

The idea was having a more stremlined way of compare your Render and Reference colour checkers, being able to view either one on top of the other, so you can closely match up the colours.

Correct digital MacBeth charts can be found [here](http://www.nukepedia.com/gizmos/draw/x-rite-colorchecker-classic-2005-gretagmacbeth) in many colourspace's, as EXR download or Nuke Gzimo.

You'll want to move the 4 controls in Reference and Render dropdowns to the corners of your Reference and Render colour checkers, then you have 3 options (Merged, Ref / Render, Render / Ref)

With this workflow you can simply copy the grade nodes over to your CG elements and use them as a starting point for the grade.

I have written up a detailed workflow guide for this process, which you can find [here](https://gquelch.github.io/2020/05/14/Colour-Checker-Nuke-Workflow-d6e754f150584b09ba230bf43706539d/)

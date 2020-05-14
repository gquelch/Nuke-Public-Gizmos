# Nuke-Public-Tools
My freely available scripts and tools for Nuke


Jump to Documentation:

[GQ_Tools](https://github.com/gquelch/Nuke-Public-Gizmos#gq_tools)

[LightWrap_GQ](https://github.com/gquelch/Nuke-Public-Gizmos#lightwrap_gq)

[ColourChecker_GQ](https://github.com/gquelch/Nuke-Public-Gizmos/blob/master/README.md#colourchecker_gq)

---

## GQ_Tools
A collection of smaller scripts and tools I use regularly

The top set of tools have some quick actions that let you select nodes by class, you just write each class you want to select, seperated by spaces

E.g

"Blur Grade Defocus"

You can also set up your own list of heavy nodes, which you can then disable all of in your script with one button, soon I will add a UI for defining this list.

### Disable Tools

There are two tools here. The first let's you link up the disable of any selected nodes, to the GQTools node, allowing it to become a master disable for any nodes in your script.

Linking the write node, will set the GQTools node to enable on specific write nodes, so when you render it will become enabled. This allows you to work with nodes always disabled, and you don't have to remember to turn them back on before you render.

### Read Properties

These are fairly self explanatory, allowing you to change properties of all the read nodes you have selected.

### Grade Convert

Sometimes I find myself working on a grade node, and deciding I want to use Saturation. Instead of creating an additional colour correct, you can copy over gamma and gain to a colour correct, and keep working. Please note this will not work with Black point and White point

### Open Read Path

This will open up a file browser at the file path for any read nodes you have selected


## LightWrap_GQ

This is my own custom light wrap node, I find the default node frustrating as if often messes with other channels if used directly in the main pipe. My node only affects the RGB channels so you no longer have to worry about that.

There are also two types of blur, a standard soft gausian, and an exponential blur, this allows you to get a really nice falloff in the light wrap, as well as the softer colour bleed you can get with the standard lightwrap node

## ColourChecker_GQ

I designed this tool to be able to better make use of macbeth charts for VFX projects.

The idea was having a more stremlined way of compare your Render and Reference colour checkers, being able to view either one on top of the other, so you can closely match up the colours.

Correct digital MacBeth charts can be found [here](http://www.nukepedia.com/gizmos/draw/x-rite-colorchecker-classic-2005-gretagmacbeth) in many colourspace's, as EXR download or Nuke Gzimo.

You'll want to move the 4 controls in Reference and Render dropdowns to the corners of your Reference and Render colour checkers, then you have 3 options (Merged, Ref / Render, Render / Ref)

With this workflow you can simply copy the grade nodes over to your CG elements and use them as a starting point for the grade.

I have written up a more detailed workflow guide in another post, which you can find here

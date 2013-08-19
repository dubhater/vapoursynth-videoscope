Description
===========

This is a rewrite of the Avisynth plugin VScope: http://forum.doom9.org/showthread.php?t=76238

It is similar to Avisynth's built-in Histogram() filter.


Usage
=====
::

   vscope.Scope(clip clip[, string mode="both", bint tickmarks=1, string side="Y", string bottom="Y", string corner="blank")

mode
   "side"
      Draw a histogram on the right side.

   "bottom"
      Draw a histogram below the image.

   "both"
      Draw both histograms.

tickmarks
   Draw dotted lines over the histograms.

side
   "Y"
      Draw histogram of luma.

   "U"
      Draw histogram of chroma channel U

   "V"
      Draw histogram of chroma channel V.

   "UV"
      Draw histograms of both chroma channels, side by side.

   "YUV"
      Draw histograms of chroma channels, on top of histogram of luma channel.

bottom
   See *side*.

corner
   "blank"
      Keep the corner blank.

   "colormap"
      Chroma map.

   "Y"
      Full frame histogram of luma.

   "U"
      Full frame histogram of chroma channel U.

   "V"
      Full frame histogram of chroma channel V.

   "UV"
      Vectorscope.


Compilation
===========

::

   clang -O3 -Wall -Wextra -Wno-unused-parameter -fPIC -shared -o libvideoscope.so videoscope.c


License
=======

The license is WTFPL.

The original code processes YUY2 directly, so none of it could be copied.

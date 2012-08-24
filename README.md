This is **NOT** my code. The original README is below followed by some additional instructions for smooth running on OSX 10.8.

Original README
================
The sources are in util.ml, data.ml, cg.ml, bfgs.ml and data.ml.
There is a Makefile to you can build it on any system that has ocaml
(http://caml.inria.fr) installed (I use version 3.07+2; anything since
3.06 should be fine; anything earlier and you'll have to take
-ffast-math out of the Makefile).

To build a safe but slow version, just execute:

  make

which will produce an executable megam, unless something goes wrong.

To build a fast but not so safe version, execuate

  make opt

which will produce an executable megam.opt that will be much much
faster.  If you encounter any bugs, please let me know (if something
crashes, it's probably easiest to switch to the safe by slow version,
run it, and let me know what the error message is).

This code is free to anyone and you can use it in any research thing
you want.  For commercial use, please contact me.  If you use it for
work in a published article, please add a footnote acknowledging the
software, or cite the article available on the web page.

For more information, go to:

  http://hal3.name/megam/

Thanks and enjoy!


Additional OSX 10.8 Instructions
--------------------------------
Here are some additional instructions for building on OSX (tried on 10.8).
You need to install ocaml. The easiest way of doing this is using [Homebrew](http://mxcl.github.com/homebrew/).

The Makefile in this repository version has been amended to locate the necessary libraries
for ocaml.

Additionally the following needs to be run in the terminal:
```bash
sudo ln /usr/local/lib/ocaml/libcamlstr.a /usr/local/lib/ocaml/libstr.a
```
to avoid an ld library error on -lstr.
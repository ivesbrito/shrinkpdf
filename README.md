# shrinkpdf
Shrinkpdf: shrink PDF files with Ghostscript

A simple wrapper around Ghostscript to shrink PDFs (as in reduce filesize) under Linux. Inspired by some code I found in an OpenOffice Python script (I think). The script feeds a PDF through Ghostscript, which performs lossy recompression by such methods as downsampling the images to 72dpi. The result should be (but not always is) a much smaller file.

Usage

Download the script by clicking the filename at the top of the box. Make it executable. If you run it with no arguments, it prints a usage summary. If you run it with a single argument – the name of the pdf to shrink – it writes the result to stdout:

./shrinkpdf.sh in.pdf > out.pdf

You can also provide a second filename for the output:

./shrinkpdf.sh in.pdf out.pdf

And an output resolution in DPI (default is 72 DPI):

./shrinkpdf.sh in.pdf out.pdf 90

If both the input and the output are regular files, the script checks if the output is actually smaller. If not, it writes a message to stderr and copies the input over the output.

Sorry, Windows users; this one is Linux only. A Windows adaptation of this script can be found on this blog. It's a bit more user-friendly than my barebones version and also supports drag-and-drop.
License and acknowledgements

The script is licensed under the BSD 3-clause license.

I didn't invent the wheel, just packaged it nicely. All credits go to the Ghostscript team.

Many thanks to Dr. Alun J. Carr for fixing a portability issue on Mac OS X regarding leading whitespace in the output of wc.

---

All credits of this code for aklomp (https://github.com/aklomp). 

Thanks so much!

http://www.alfredklomp.com

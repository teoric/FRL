# FRL Manual

The manual should compile with modern [groff](https://www.gnu.org/software/groff/), probably already installed if you use some unixy system.  It may also compile with other troffs, bot the `Makefile` will probably not work.

To build the manual as PostScript, call

    make frl.ps

To generate a PDF instead, use:

    make frl.ps

If your groff is new enough to include the `pdf` device and the `pdfmark` macros, you can also build a PDF file with PDF bookmarks, which simplifies navigation.

    make frl.bookmarks.pdf


# Warnings

You may get a warning `./frl.bindex:1: name expected (got `\{'): treated as missing`. This seems to be harmless.

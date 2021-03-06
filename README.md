SoFoBoMo 2011
=============

What is it?
-----------
This a latex implementation of a photo book. It has been used to create a PDF photo book that has low-res images suitable for web display, and also will generate a hi-res version that is compatible with the Blurb.com ["PDF to Book" publish on demand process](http://www.blurb.com/make/pdf\_to\_book).

This particular book was submitted to [SoFoBoMo](http://sofobomo.org) 2011 as a PDF suitable to create a 10x8 softcover book. It should be straightforward to tweak this to other sizes, compared to GUI desktop publishing systems.

To use this, you will need a decent implementation of xelatex.  I used the version of xelatex that is bundled with the TexLive 2009 distribution packaged for Debian Linux (Squeeze).
This distribution is available for other platform (MacOS, Windows, etc.)

Files of interest
-----------------

- _Rakefile_
  Used to build the different versions. Targets: book-web.pdf, book-blurb.pdf, cover-blurb.pdf. The photos are not committed to git.
  This is my first attempt at using rake, so comments are welcome.

- _common-book.tex_
  Content that is common to both web and book (POD) versions

- _fonts.tex_
  Common fonts definition

- _colors.tex_
  Common colors definition. Color are defined as rgb and cmyk.

- _book-web.tex_
  Top level file for the book (web version) PDF. The resulting PDF was uploaded to SoFoBoMo 2011.

- _book-blurb.tex_
  Top level file for the book (Blurb version minus cover) PDF. The resulting PDF is uploaded as the "text block PDF" to blurb.com

- _cover-blurb.tex_
  Top level file for creating the wraparound cover for the book (Blurb version) PDF. The resulting PDF is uploaded as the "cover PDF" to blurb.com

Image preparation
-----------------
I create two directories, <code>photos.web</code> and <code>photos.book</code> which I populate with images downsampled to 144dpi and 300dpi, respectively, at the same "printed" dimensions (e.g. 8x6in).

The images in <code>photos.book</code> are converted to CMYK using the color profile distributed by Blurb.

Licensing
---------
Please see the file called LICENSE.

Credits
-------
This work is heavily based on the templates from Eric Jeschke. See [redskiesatnight.com](http://redskiesatnight.com/books/pod/latex).

Many thanks to Eric.

The main differences among my work and Eric's one:

- don't use his folio templates and his script for image processing
- use parallel and polyglossia packages to manage the bilingual text (English, Italian)
- use overpic package to layout text over images (that's for the cover images of the web book)
- use pstricks and pst-barcode packages to create a QR code
- use pstricks package to create the cover of the blurb book
- use rake to build the books
- book and cover for Blurb are created in CMYK

Contacts
--------
For question and comments:

- [MauroTaraborelli@gmail.com](mailto:MauroTaraborelli@gmail.com)
- [MauroTaraborelliPhoto@gmail.com](mailto:MauroTaraborelliPhoto@gmail.com)
- [www.maurotaraborelliphoto.com](http://www.maurotaraborelliphoto.com)

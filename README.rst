Snake Wrangling for Kids: python 2.7 edition
============================================

Originally cloned from https://code.google.com/p/swfk/ repository maintained 
by the book's author, Jason R Briggs.

This work is licensed under the Creative Commons Attribution-Noncommercial-Share Alike 3.0 New Zealand License.
To view a copy of this license, visit http://creativecommons.org/licenses/by-nc-sa/3.0/nz

My colleagues and I at VCT Labs have volunteered put on an intro-to-programming
event for some local high schools in honor of CS education week. Our lead
instructor, Steve Arnold, chose SWFK as the best free resource on which to base
the slides and as a reference to be sent home with the kids, but we quickly ran
into a complication: 

* the book is compatible with python 3.0
* the live USB sticks for the event provide python 2.7

Clearly there were 2 ways to go about resolving the conflict -- add python 3
to the sticks or get a version of the book compatible with python 2.7.
The former allowed too much potential for confusion if the kids managed to
run the "wrong" version of python after they went home, and contrary to the
suggestion in the book, their parents would be unlikely to be able to help
them.  So, we chose the latter, getting hold of a version of SWFK that was
compatible with the system-wide copy of python on the live USB sticks.

It turned out that early versions of this book were compatible with python 2.7,
but in December 2008 the author switched over to python 3 syntax instead. All
of the enhancements he made after that, including the OS-specific flavors of
the book, were added to the python 3 version. However, thanks to the author's
generous release of the book source files under a Creative Commons license,
we could have the best of both worlds with this fork: roll back to python 2.7
syntax, but keep the other enhancements.

Following modifications were made to create a python 2.7 flavor of version
0.7.7 of Snake Wrangling for Kids::

  Front matter:
   change version string to 0.7.7-python2.7
  
  Preface:
    remove it, it's all about "this book is only compatible with python 3..."
  
  Chapter 1:
    remove reference to preface which was deleted
  
  Chapter 9:
    python2 needs 'import Tkinter' instead of 'import tkinter'
  
  Appendix C: 
    sys.stdout.write() does not return number of characters written in python2;
    take out the new little note mentioning it 

Build instructions
------------------

Note: if you don't want to make any changes, feel free to use the pre-generated
PDFs under ``prebuilt/`` subdirectory rather than building them yourself from source

* make sure texlive-latexextra package is installed (should be available via whatever you use for package management:  apt-get, emerge, yum... )
* run the build: ``python setup.py build``
* find output PDFs under ``target/`` subdirectory


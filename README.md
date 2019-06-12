# CDMI-spec

This repository contains the source files used to build to the official CDMI 2.0 specification document.

The document is written using reStructuredText, and built using the Sphinx (http://www.sphinx-doc.org/en/master/).

Currently, the document is optimized for PDF output via LaTeX.

Build Instructions for Windows 10
=================================

When installing the various applications, it is recommended to choose the _current user only_ installation in contrast to the _all users_ installation. This prevents later issues around the need for Administrative Access.

Sphinx
------

1. Download & Install Python 
   https://www.python.org/downloads/windows/
   Tested with Python 3.6.5

2. From the Windows command line, run: `pip install sphinx sphinxcontrib-bibtex`
   This should also pull in any dependencies

Sphinx with LaTeX
-----------------

3. Download and install MikTeX
   https://miktex.org/download
   Tested with MikTeX 2.9

4. Download and install Perl
   Tested with ActiveState Perl
   https://www.activestate.com/activeperl/downloads

5. Install required MikTeX packages as follows: 

   1. Open MikTeX console from Windows Start menu
   2. Click on 'Stay in user mode'
   3. Choose the tab "Packages" on the left side of the window
   4. Find the package 'latexmk' in the list and install via right-clicking and choosing 'install package'
   5. Close the window
   6. Other MikTeX packages will be automatically installed during the LaTeX build later on.

Build
-----

6. Download the .zip archive of the CDMI-spec repository from Github
7. In the "CDMI-spec-master" directory, run `make latex`
8. In the "CDMI-spec-master\\_build\latex" directory, run `latexmk -pdf`
9. Run `start _build\latex\CDMI_v2.0.0.pdf` to open the newly built PDF


Build Instructions for Macintosh 10.13
======================================

Sphinx
------

1. Install xcode from the Macintosh App Store
2. From the Mac Terminal, run `xcode-select --install` to install the xcode Command Line Tools
3. From the Mac Finder, run the xcode application to accept the license
4. Download macports from https://www.macports.org/install.php
5. From the Mac Finder, run the macports Installer application
6. From the Mac Terminal, run `sudo port install py36-sphinx` to install sphinx
7. From the Mac Terminal, run `sudo port select --set python python36` to set python 3.6 as default
8. From the Mac Terminal, run `sudo port select --set sphinx py36-sphinx` to set python 3.6 as the default for Sphinx
9. From the Mac Terminal, run `sudo port install py36-sphinxcontrib-bibtex` to install the bibtex bibliography extension to sphinx

The following additional pacakges may be required:

* `sudo port install py36-sphinxcontrib-qthelp`
* `sudo port install py36-sphinxcontrib-serializinghtml`
* `sudo port install py36-sphinxcontrib-htmlhelp`
* `sudo port install py36-sphinxcontrib-jsmath`
* `sudo port install py36-sphinxcontrib-devhelp`
* `sudo port install py36-sphinxcontrib-applehelp`

Sphinx with LaTeX
-----------------

9. From the Mac Terminal, run `sudo port install texlive-latex` to install latex
10. From the Mac Terminal, run `sudo port install texlive-xetex` to install xelatex
11. From the Mac Terminal, run `sudo port install latexmk` to install latexmk
12. From the Mac Terminal, run `sudo port install texlive` to install texlive
13. From the Mac Terminal, run `sudo port install texlive-latex-extra` to install texlive extras

Build
-----

14. Download the .zip archive of the CDMI-spec repository from the snia-spec github repository (https://github.com/SNIA/CDMI-spec)
15. From the Mac Terminal, in the CDMI-spec-master directory, run `make latexpdf` to build the document
16. From the Mac Terminal, in the CDMI-spec-master directory, run `open _build/latex/CDMI_v2.0.0.pdf` to open the newly built PDF








===================================================================================================
**** If you like the programs i'm porting and you want to donate to me, see the following URL: ****
**** http://www.bitwiseworks.com/shop/index.php?id_product=38&controller=product& id_lang=1    ****
****             Or send directly to me using PayPal: tellie@elbertpol.nl                      ****
****                All the money you send will go to the QT5 project                          ****
===================================================================================================

Tea v63.0.1   

 CONTENTS OF THIS FILE
 =====================

1. INTRODUCTION

2. REQUIREMENTS

3. INSTALLATION

4. LICENSE, COPYRIGHT, DISCLAIMER

5. CONTACT

6. CREDITS

7. SUPPORT AND DONATIONS

8. HISTORY

9. RESTRICTIONS


1. INTRODUCTION
===============

Welcome to tea v63.0.0 port for OS/2 and eComStation.

TEA is the Qt-based text editor for UNIX-like systems and Windows. 
With an ultimate small size TEA provides you hundreds of functions. 



2. REQUIREMENTS
===============
  The following requirements can be installed either by rpm or by zip files  
  except Extended System Tray widget which is currently available as zip only.
  

  RPM Installation (preferred):
  ============================
  klibc
  -----
   1. yum install libc
  
  
  --------
   1. yum install libgcc1
   2. yum install libssp
   3. yum install libstdc++6 libstdc++
   4. yum install libsupc++6 libsupc++
   5. yum install libgcc-fwd

  Qt5 dll
  -------
   1. yum install Qt5Core Qt5Gui Qt5Wdgt

    
  Zlib  
  ----
   1. yum install zlib
  
  Hunspell
  -------
   1. yum install hunspell

  aspell15
  ------
   1. yum install aspell15 (this also installs the english dictionary)

  aspell languages
  ----------------
   1. yum install aspell-xx were xx is your language (not all are available)

  Hunspell
  --------
   1. yum install hunspell

  djvuli21
  --------
   1. yum install djvuli21

  poppq51
  -------
   1. Yum install poppler


3. INSTALLATION
===============

  Tea
  ---
  1. It's create a directory for Tea.
  2. It's create a WPS object for Tea.exe.
  

4. LICENSE, COPYRIGHT, DISCLAIMER
=================================

(C) 2007-2023 peter.semiletov@gmail.com https://github.com/psemiletov/tea-qt

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.


5. CONTACT
==========

if you find a bug, then add a ticket to the trac at http://svn.netlabs.org/qtapps

Only bug reports with a reproducable bug are accepted. :-)



6. CREDITS
==========

The port was done by: Elbert Pol aka TeLLie

Thanks go to:

  * Peter 'Roxton' Semiletov
  * Dmitry A. Kuminov
  * Silvan Scherrer

They either helped me when I had some nasty questions or did some testing for me.


7. SUPPORT AND DONATIONS
========================

Tea is based on volunteer work. If you would like to support further
development, you can do so in one of the following ways:


  * Donate to the Qt5 project

  * While working on Qt 5 for OS/2, we are glad to know that our work is being partly sponsored by the grateful OS/2 community.
    Given the scale of this project and all other OS/2 projects that we work on, and also the fact that the OS/2 world has limited financial resources nowadays, every penny counts.
    We need to pay our full-time and part-time developers for their hard work. So any contribution is highly appreciated!
    To do so, please visit our online shop where you can buy development units of a preferred value.
    https://www.bitwiseworks.com/shop/index.php

  * Contribute to the project: Besides actual development, this also includes maintaining the documentation and the project web site as well as help for users.

8. HISTORY
==========
Compiled now with Qt v5.15.2

Changelog:
May 11 2024 - TEA 63.0.1 is out! The spellchecker fix.

May 10 2024 - TEA 63.0.0 is out!

Hello! This release removes a lot, and also brings a lot, it's all about changes and moving forward. The QT-version of TEA was born at 2007, with many functions of predecessors (the first TEA was developed at the year 2000 for Windows, with Delphi, and then was reborn many times on different programming languages and toolkits).

So I recreated many old functions, those was useful in the past, and from yest to year TEA just grew with functionality. Different things became obscure and deprecated. I haven't touch some code over a decade. It was good working code at 2007, but now?

TEA version 63 is a try to refresh a program, make it more compact and clean, and also modern. Not just the "maintainance release". Despite this horrible promise, TEA is still C++ 98 code (and C++ 17 when build with Qt6), and can be compiled with Qt4, Qt5 or Qt6.

One of the core TEA features was ability to work with any possible character sets. This was implemented using Qt's wrapper around the iconv, and that wrapper was deprecated at Qt6, but still available there as the part of Qt5Compat.

At TEA 63 I removed this dependency, now TEA can handle only a limited number of charsets - UTF-8, UTF-16 and legacy Cyrillic encodings. If you need some specific 8-bit charset support, let me know.

Also, all charset auto-detection code is removed.

Another big and important thing in TEA is ZIP-support, that is needed to work with DOCX, ODT, EPUB, etc. Previously, TEA used the bundled Quazip and zlib to handle ZIPs. Sure, I was glad to use it at the full power and gave to TEA the packing abilities. Now even I don't use TEA as the zipper or unzipper.

So, now TEA uses another, the smaller library (ZIP/Miniz) for ZIP support, and cannot create archives.

As a result of these changes, I removed also: RTF reader (probably temporary), gzipped text files reader, and all code that related to zip/unzip, including the file names charset setting (it was important for the ancient zips with Cyrillic file names). Noooo! Noooo! It broke my heart!

TEA 63 uses the code from my new program, the e-book reader and "speaker" Beseda (https://psemiletov.github.io/beseda/) designed for visually impaired people. Thus leaded me to rewrite and fix FB2 and Epub support for TEA.

Other removals are: Alt-WASD as cursor keys and Meson build system support.

Meson is good, but it is too much for TEA to support all three build systems: qmake, Meson and cmake. So now we have legacy qmake support for Qt4 and Qt5 (but cmake for Qt5 is preferred), and cmake for Qt5 and Qt6.

Spellchecking now much improved. It is fixed at Windows port (at least with Hunspell, but I think there are some issues with Aspell, need to test more).

Among Aspell and Hunspell, you can use shining modern Nuspell (if TEA is build with it support).

Over all three spellchecking engines TEA provides own simple spellchecker, that works transparently and provides the user-defined dictionary, shared between all engines and languages.

Another new feature, the experimental one - Speech Dispatcher support, please read the TEA documentation how to use it. Briefly, TEA now can speak the text, but it will be enhanced in the future releases to make it really handy.

Another note about formats support. PDF support now uses libpoppler-cpp, not Qt bindings.

A known issue - all Alt-key based user-defined hotkeys works strange under Plasma 6, please avoid such hotkeys.

NOTE FOR PACKAGERS:

- Removed dependency: zlib
- Removed optional dependency: poppler-qt5/6
+ New optional dependencies: popplercpp, nuspell

Stay tuned.
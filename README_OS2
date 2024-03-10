===================================================================================================
**** If you like the programs i'm porting and you want to donate to me, see the following URL: ****
**** http://www.bitwiseworks.com/shop/index.php?id_product=38&controller=product& id_lang=1    ****
****             Or send directly to me using PayPal: tellie@elbertpol.nl                      ****
****                All the money you send will go to the QT5 project                          ****
===================================================================================================

Tea v62.4.0   

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

Welcome to tea v62.4.0 port for OS/2 and eComStation.

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

62.4.0, March 2024
   More Qt6-related fixes!

62.1.2

* Spellchecker fix

62.1.1
* PDF fix

62.1.0
+ new version of pugixml XML parser
* cmake support is rewritten a lot.

* 62.0.1 quick fix
+ Edit - Select all

* Qt6 copy text with new lines - fixed
* Markdown functions - fixes 

+ View - Preview Markdown //Qt 5.14+ 

+ QT6 only: Functions - Math - Subtitles: shift timecode by msecs 
            put msecs to FIF. msecs can be negative, i.e "-2000" shifts timecodes by 2000 msecs earlier
            //works also for Youtube subs

+ Options - Interface - Show tabs and spaces
* find in files FIX
* TEA theme FIX

- Individual ODT/SXW reader class, the functionality moved to common zipped XML reader
+ Tune - Functions - Misc - Show ebooks fine (adds spaces before each paragraph)
* old bookmarks file automatically converts to new format
* bookmarks and recent files has a new format (with a separator *)
* recent files list will be updated to new format on use, so the old records will be lost

* xml parser changed to pugixml

+ FB2.ZIP, FBZ support
* single application mode fixes

+ FB2 support improvements
+ poppler-qt6 support with cmake
* DJVU support with cmake - fixed

+ autosave
* braces hl megafix

* cmake + hunspell detection fix
+ Polish UI and Manual translation by Krzysztof Jakiewicz
+ Rust hl support
+ The time consuming operations such as "Find in files" can be interrupted.

* Dates panel upd
+ SRT hightlighting
+ Basic Haskell hightlighting
* Good old bug with syntax hl engine (related to partial hl module file) is fixed
+ Youtube subtitles highlighting support
+ Fn - Case - Capitalize sentences


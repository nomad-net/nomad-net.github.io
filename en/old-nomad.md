---
lang: en
layout: page
nav: 40
---
# Old Nomad

Nomad is a powerful file manager written in Delphi language. This version is canceled and superseded by [**Nomad.NET**](/en/about).

## Background

I was previously a fan and old user of Dos Navigator manager, but this program was abandoned, and their [developers](http://www.ritlabs.com/) switched to another projects. As an old dos program DN stop satisfy my needs (a most disappointment is lack of long filenames support) so I decided to switch to another manager.

And I cannot find one that both powerful and good-looking. There was a couple of expensive Explorer replacements, FAR (also abandoned by author and now supported by [community](http://www.farmanager.com/?l=en)) and Window Commander (now [Total Commander](http://ghisler.com/)). FAR was not an option because it has old console look (I switch from console to windows, so I want all new beautiful interface), Windows Commander is powerful but sooo ugly.

So I started this project in 1998 as a hobby. Project was grows from version 1.0 to version 1.92 (last release in 2002) until I can find free time to support it (and at the end project satisfy me in all areas almost fully).

This project is also was very good to test my abilities and skills. From its beginning I was learn a LOT about system programming for Windows.

### Minimum requirements

Supported OS: Win95, Win98, WinME, WinNT, Win2k, and WinXP.

## Features

This program is advanced file manager with many different functions such as:

- Two panel view.
- Each panel can show files, folder tree, and quick file preview or drive information.
- Very powerful file filtration.
- Search with ability to find file according to many rules (including duplicate finding), with ability to save search for later use.
- Threaded file operations. All file operations (copy, delete, move, etc) are executed in separate threads and do not prevent you to work with program. This feature was implemented from very first version, and in when released Nomad was first file manager that has such threaded design!
- Archive opening, search and folder branch are also executed in separated threads, so you can always stop them when they took too much time.
- Copy with file filtering and group renaming (highly customized).
- Full Drag and Drop and clipboard support.
- Easy to configure utilities menu.
- Very easy to configure. Full support to change color scheme or keyboard layout. Ability to create your own toolbars.
- Powerful file [viewer](/en/old-viewer). Supports many code pages (including Unicode and UTF-8), hex and dump view modes. You can view files of unlimited size.
- Text files [editor](/en/old-editor) with syntax highlight. Supports many code pages (including Unicode and UTF-8). Edited file size restricted only by available memory size.
- Calculator with native math expressions evaluation.
- Internal support for many archive formats. Internal unpacking for some of them.

## Supported archive types

Archives support implemented through plug-in system. At this moment there is four archive plug-ins available:

- Archives
    - [ZIP](http://www.pkware.com/) with internal unpack
    - [RAR](http://www.rarlab.com/) with internal unpack
    - CAB with internal unpack
    - ACE with internal unpack
    - ARC with internal unpack
    - PAK with internal unpack (not all methods)
    - LZH
    - ARJ
    - [GZip](http://www.gzip.org/) with internal unpack
    - Z (Unix)
    - [TAR](https://www.gnu.org/software/tar/tar.html) with internal unpack
    - BZip2 with internal unpack
    - HA
    - ZOO
    - HYP (Hyper)
    - Q (Quantum)
- Internet files
    - MIME with attachments. Base64, Quoted-printable, UUE decoding.
    - UUE with internal decoding
    - XXE with internal decoding
    - HQX (BinHex) with internal decoding
    - DBX (Outlook Express Database) with internal unpack
- Disk Images
    - IMA (FAT Disk Image) with internal unpack
    - ISO (ISO 9660 CD-ROM Disk Image) with internal unpack
- Computer game files
    - WAD (Doom) with internal unpack
    - WAD2 (Quake) with internal unpack
    - PAK (Quake) with internal unpack

## Screenshot

![Screenshot](/assets/images/old-nomad-shot.png)

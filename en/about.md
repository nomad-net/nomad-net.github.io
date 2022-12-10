# About

**Nomad.NET** is the successor of Nomad, a powerful file manager written by me a couple of years ago. It is completely rewritten (no single line of code was taken from previous Nomad) using best ideas and algorithms and implementing everything in a completely new way.

Several years ago I changed my employer and moved to Microsoft new technology called ".Net". For better understanding of many hidden areas, techniques and classes from new framework I started to write small simple applications that did what I knew the best - how to work with OS in file manager way. When I had dozens of such simple applications an idea to completely rewrite old Nomad on new framework had come. So in 2008 the work began.

New Nomad was developed with multi-threading in mind, so almost all long operations can take advantage of multi-core cpu (comparing, copying, searching, detecting archive format and so on - too many to list all of them here).

I do not want to create all-in-one mega monster that plays mp3, shows movies, etc, as many other file managers do. My goal is to build only file manager functionality, but do it very good, or even best of all. For other purposes there are dedicated programs that always do things better than such jack-of-all-trades programs.

## Features Overview

As for features of original Nomad, you can take a look at them on appropriate page. Here I describe the features that are significantly changed or just are new:

- Full Unicode support.<sup>[[screenshot]](unicode.png)</sup>
- Tabbed interface. But in contrast to almost every other file manager tabs are not panel based.
- Powerful bookmarks system. You can bookmark you favorite folders, ftp sites or even searches (yes, you can create virtual search folders).
- One of the most powerful search engines on market (if I can say market, project is freeware). You can create very complex search rules, with ability to search in different encoding (complete encodings auto detect), use IFilter filters, apply custom text search rules (including regular expressions), search in hex, duplicates search and so on... For novices there is a simplified search that is not so scary at first sight.[screenshot]
- Powerful filtering system, based on the same core as search. You can use dedicated advanced filter dialog, or use simple toolstrip for quick filtering.[screenshot]
- Much simpler, elegant and polished UI (program must look nice, right?)[screenshot]
- Customizable visual themes[screenshot] and icon packs. And you can even create your own themes and icon packs.
- The most powerful toolbar you can even find in file manager.[screenshot]
- Improved main form layout. You can use single panel or dual panel mode (horizontal or vertical). Each panel can have its own tree view that can be hidden or displayed horizontally or vertically. And you can even store your customized layouts for future use.
- Ability to customize selected folders view and options (filter, sort, etc). This is unique feature and you cannot find it in other managers.[screenshot]
- Program is highly customizable via Options dialog[screenshot], including simple UI scaling according to your current system DPI settings (or manually).
- Breadcrumb folder toolstrip on every panel is much more powerful than simple folder name.[screenshot]
- Full internal support for many archive types (using 7-Zip libraries). Program can also handle WCX Total Commander plug-ins, even in more powerful way than original did. You can view, create and edit archives.
- Support for WDX (new columns) and WFX (new file systems) Total Commander plug-ins are also here.
- FTP folders support (with limitations yet, for example, only one http proxy allowed with no UI to configure).
- Many things were done more correctly - drag'n'drop from explorer, clipboard handling, shell file menus and so on.
- Support for shell shortcuts, url shortcuts (ftp only) and even shell folder shortcuts (rarely supported in other file managers).
- And last, Nomad is the first ~~and only~~ (there is more now, but Nomad is still the first) file manager written on .net. This is not advantage, because in addition to strong sides, it has some drawbacks. Just a fact.
- And many, many more...

As you can see, the main idea of new Nomad.NET is to do the same things in more correct and beautiful way.

## Screenshot

One image can say more than thousand words.
![Nomad screenshot]({% link /en/assets/images/nomad_shot_en.png %})

## License

Nomad.NET is freeware, you are free to use and distribute it, as long as you are not selling it for profit. There is no warranty or other guarantee of any kind, use it at your own risk. Read full license [here](license.txt).

Some other libraries used by Nomad written by other people and distributed under another licenses. Read license information for 7z.dll [here](7z-license.txt). And GNU lesser general public license can be found [here](copying.txt) (used for both 7z.dll and TagLib#).

## Special Thanks

I wish to thank the following people for their invaluable help. These people helping me make Nomad.NET better:
- **Sven Knurr** for German localization.
- **Martijn Weisbeek** for Dutch localization.
- **Igor Kovalenko** for Ukrainian localization.
- **Guy Pouliot for** French localization.
- **Claudio Vicari** for Italian localization.
- **Jakub Vít** for Czech localization.

## Thanks

Also I wish to thank following people and organizations, with their explicit or implicit help this program came to life:

- [www.codeproject.com](https://www.codeproject.com/) and all of its authors and contributors. I took a lot of useful information from articles located on this site, and want to pay them same coin (I have plan to publish several articles related to Nomad development).
- **Igor Pavlov** and his excellent [7-Zip](https://www.7-zip.org/) archiver.
- [www.pinvoke.net](http://www.pinvoke.net/) for all correct and incorrect P/Invoke translations.
- **Phil. Wright** for excellent [Office2007Renderer](https://www.codeproject.com/Articles/16666/Office-2007-ToolStrip-Renderer) class.
- **xasthom** for idea of how to create my own vista progress bar and for initial code for it.
- **Eyal Post** for idea and implementation of [IFilter reader](https://www.codeproject.com/Articles/13391/Using-IFilter-in-C) (still I overwrote it completely).
- **Mark James** for [silk icons set](http://www.famfamfam.com/). I still miss some of icons for the program.
- [TagLib#](https://github.com/mono/taglib-sharp/) for excellent audio/video tag library.

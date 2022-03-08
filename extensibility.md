---
layout: page
title: Extensibility (Plug-ins)
---

# Extensibility (Plug-ins)

There is no perfect piece of software in the world and Nomad, of course, is not ideal too. There is a lot of request to add some new functionality to Nomad.NET, and I understand that I cannot satisfy them all. So program extensibility is the only way to give users (i.e. you) more.

## Native Plug-ins

Starting from version 3.0 Nomad contains extensible plug-ins framework that you can use to create your own native plug-ins. But there is one caveat - no API documentation available at the moment (creating documentation requires a lot of work, so I'll not do this while it is not really necessary). So if you want to write a new shiny Nomad plug-in, please contact me, or examine source of plug-ins that is currently shipped with Nomad:

- CmdLinePlugin
- CommandPromptPlugin
- VirusTotalPlugin

But, if you really want to write plug-in for Nomad, it is better to contact me first. While I've tried to use as many interfaces and abilities as possible in plug-ins listed above, there is much more APIs available.

## Total Commander Plug-ins

Other options to extend Nomad is also available. In order to compete with another file managers, Nomad must take others strong parts while avoiding weak sides. For example one of the strongest sides of Total Commander is support for plug-ins (and there is lot of them). It is not wise to skip such codebase and that is why Nomad supports several kind of TC's plug-ins.

However plug-ins framework in TC is outdated and suffer from many weak architectural decisions (for example many plug-ins use some hacks to get access to TC main window, because it is not possible to do this with framework. Of course it will be not possible under Nomad). Environment for plug-ins in Nomad is different than in TC and sometimes Nomad is also handling plug-ins differently, that is why some plug-ins can work partially or even can not work at all. I tried to do my best, but I physically cannot test every plug-in available. That is why I created compatibility tables (you can find them below) for plug-ins that I test by myself.

If you find TC plug-in that is works or not works with Nomad, please contact me and I will update appropriate table. Of course if plug-in is not working I'll try to fix this as soon as possible.

## Plug-ins installation

For TC plug-ins there is two ways to install them. If plug-in comes as archive and it is configured to auto-install (archive contains pluginst.inf file), Nomad will ask to install it when you open it. For plug-ins that do not support such functionality you can simple extract (copy) them into appropriate plug-ins folder (\plugins\wcx\ for wcx plugins, \plugins\wdx\ for wdx plug-ins, etc). Note that for many plug-ins Nomad restart is required after installation.

## WCX Plug-ins

These plug-ins intended to extend application by adding support for more archive formats. **Nomad.NET** have full support for such plug-ins, both for extracting existing archives and for creating a new ones.

#### Compatibility list for WCX plug-ins

| Plug-in Name | Tested Version | Test Result | Test Date | Nomad Version | Tested By | Comment |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| [btdir](http://wincmd.ru/plugring/btdir.html) | 0.1 beta2 | Works | <time datetime="2011-03-31">Mar 31, 2011</time> | 2.8.7.1740 | Me |
| [EFD_View](http://infostart.ru/projects/3555/) | 0.9.5.2 | Fail | <time datetime="2011-01-17">Jan 17, 2011</time> | 2.8.7.1700 | Roman Bakay |
| [HA](http://www.totalcmd.net/plugring/ha.html) | 1.1.0.0 | Works | <time datetime="2008-10-16">Oct 16, 2008</time> | 2.5.0.x | Me |
| [MhtUnPack](http://www.totalcmd.net/plugring/MhtUnPack.html) | 0.4.0 | Works | <time datetime="2008-10-16">Oct 16, 2008</time> | 2.5.0.x | Me |
| [Resource Extractor](http://www.totalcmd.net/plugring/resextract.html) | 1.1.1 | Partially | <time datetime="2010-11-15">Nov 15, 2010</time> | 2.8.7.1700 | Me |

*Note:* Not every plug-in supports detection archive format by content, so you can change or add new archive extensions for this (or any other) archive format in application options.
{% assign wcx_plugins = site.data.tc_plugin_compatibility | where: 'category', 'wcx' %}
| Plug-in Name | Tested Version | Test Result | Test Date | Nomad Version | Tested By | Comment |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
{% for item in wcx_plugins %}| [{{ item.plugin_name }}]({{ item.plugin_url }}) | {{ item.plugin_version }} | {{ item.test_result }} | {{ item.test_date | date: "%b %d, %Y" }} | {{ item.nomad_version }} | {{ item.tested_by }} | {{ item.comment }} |
{% endfor %}

## WDX Plug-ins

These plug-ins extend application by adding new columns (properties) for items. Columns available in Detailed list view, you can show, hide and manage them. Also search files with this properties (columns) is also possible. **Nomad.NET** have full support for such plug-ins.

#### Compatability list for WDX plug-ins

| Plug-in Name | Tested Version | Test Result | Test Date | Nomad Version | Tested By | Comment |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| [DirSizeCalc](http://www.totalcmd.net/plugring/dirsizecalc.html) | 2.15 | Works | <time datetime="2010-03-22">Mar 22, 2010</time> | 2.8.5.x | Me |
| [ExeFormat](http://www.totalcmd.net/plugring/exeformat.html) | 0.6a | Fail | <time datetime="2010-10-10">Dec 10, 2010</time> | 2.8.7.1700 | Me | Error: Attempted to read or write protected memory. |
| [Exif plugin](http://www.totalcmd.net/plugring/exif2.html) | 1.47b | Works | <time datetime="2010-03-22">Mar 22, 2010</time> | 2.8.5.x | Me |
| [ShellDetails](http://www.totalcmd.net/plugring/shelldetails.html) | 1.22 | Works | <time datetime="2010-12-10">Dec 10, 2010</time> | 2.8.7.1725 | Me |

## WFX Plug-ins

These plug-ins provide support for new file systems (ext2 for example). Support for such plug-ins is available starting from version 3.0.

#### Compatibility list for WFX plug-ins

| Plug-in Name | Tested Version | Test Result | Test Date | Nomad Version | Tested By | Comment |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| [Device Manager](http://www.totalcmd.net/plugring/devman.html) | 1.4 | Works | <time datetime="2011-08-01">Aug 1, 2011</time> | 3.0.0.2135 | Me | This plug-in not fully functional under Vista and Win7. |
| [Events NT](http://www.totalcmd.net/plugring/eventsnt.html) | 1.3.2.22 | Works | <time datetime="2011-08-01">Aug 1, 2011</time> | 3.0.0.2135 | Me |
| [ProcFS](http://www.totalcmd.net/plugring/procfs.html) | 2.0 | Works | <time datetime="2011-08-01">Aug 1, 2011</time> | 3.0.0.2135 | Me |
| [Registry](http://www.totalcmd.net/plugring/registry.html) | 4.8 | Works | <time datetime="2011-08-01">Aug 1, 2011</time> | 3.0.0.2135 | Me |
| [Services](http://www.totalcmd.net/plugring/services.html) | 2.4.0.203 | Works | <time datetime="2011-08-01">Aug 1, 2011</time> | 3.0.0.2135 | Me |
| [Startup Guardian](http://gorbush.narod.ru/) | 0.5.1.66 | Fail | <time datetime="2011-08-24">Aug 24, 2011</time> | 3.0.0.2135 | Alexander Slepenkin | System.ArgumentOutOfRangeException: Not a valid Win32 FileTime. Parameter name: fileTime |
| [Temp drive](http://www.totalcmd.net/plugring/tempd.html) | 1.0.1.41 | Partially | <time datetime="2011-08-01">Aug 1, 2011</time> | 3.0.0.2135 | Me |
| [Temporary Panel](http://www.totalcmd.net/plugring/temporarypanel.html) | 1.0.0.12 | Works | <time datetime="2011-08-01">Aug 1, 2011</time> | 3.0.0.2135 | Me |
| [VirtualPanel](http://www.totalcmd.net/plugring/virtualpanel.html) | 1.0.0.820 | Works | <time datetime="2011-08-01">Aug 1, 2011</time> | 3.0.0.2135 | Me |

---
*Note:* If you find working plug-in that is not in lists, or (which is worse) plug-in that does not work with **Nomad.NET**, please contact me.

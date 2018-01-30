# Homecoming Banner

[![Build status](https://ci.appveyor.com/api/projects/status/akpxc4885tnkpqnp?svg=true)](https://ci.appveyor.com/project/lcamichigan/homecoming-banner)

This is a collection of resources for creating a Homecoming banner for
[Sigma Zeta of ΛΧΑ](http://lcamichigan.com).

## Contents

* [Getting Started](#getting-started)
* [Creating an InDesign File](#creating-an-indesign-file)

## Getting Started

To create a banner, you need:

* [Adobe InDesign](https://www.adobe.com/products/indesign.html). Visit
  https://www.adobe.com/creativecloud/plans.html for more information.

* Banner.idml. The easiest way to get this file is to download it from
  https://ci.appveyor.com/project/lcamichigan/homecoming-banner/build/artifacts,
  but you can also [create your own](#creating-indesign-files).

* These fonts:

  | Font                                                                                                    | Download URL                                |
  |---------------------------------------------------------------------------------------------------------|---------------------------------------------|
  | [Skyline Bold Condensed](https://store.typenetwork.com/foundry/fontbureau/fonts/skyline/bold-condensed) | N/A                                         |
  | [Linux Libertine](http://www.linuxlibertine.org) (OpenType version)                                     | http://mirrors.ctan.org/fonts/libertine.zip |

## Creating an InDesign File

Creating an InDesign IDML file from the files in this repository requires the
free [Zip](http://www.info-zip.org/Zip.html) utility. To install Zip on Windows:

1. Click ftp://ftp.info-zip.org/pub/infozip/win32/zip300xn-x64.zip to download
   zip300xn-x64.zip.

2. Right-click zip300xn-x64.zip, choose Extract All, and then click Extract to
   extract a folder named zip300xn-x64.

3. Right-click zip300xn-x64.zip in the zip300xn-x64 folder you just extracted,
   choose Extract All, and then click Extract to extract another folder named
   zip300xn-x64.

4. Move this second zip300xn-x64 folder to C:\Program Files.

Zip is included with macOS.

To create an InDesign file, first download this repository as a ZIP archive. To
do this, click
[here](https://github.com/lcamichigan/homecoming-banner/archive/master.zip).
Unzip the archive wherever you wish. Then, `cd` to the
[Banner IDML](Banner%20IDML) folder and enter in PowerShell

```powershell
& "$env:ProgramFiles\zip300xn-x64\zip" -X0 ..\Banner.idml mimetype
& "$env:ProgramFiles\zip300xn-x64\zip" --recurse-paths --no-dir-entries -X9 ..\Banner.idml * --exclude mimetype
```

or in Command Prompt

```batch
"%ProgramFiles%\zip300xn-x64\zip" -X0 ..\Banner.idml mimetype
"%ProgramFiles%\zip300xn-x64\zip" --recurse-paths --no-dir-entries -X9 ..\Banner.idml * --exclude mimetype
```

or in Terminal

```sh
zip -X0 ../Banner.idml mimetype
zip --recurse-paths --no-dir-entries -X9 ../Banner.idml * --exclude *.DS_Store mimetype
```

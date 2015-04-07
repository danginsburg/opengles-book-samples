# Supported Platforms #

The sample code from the book is available for the following platforms:
  * [iPhone](Instructions#iPhone.md)
  * [Windows](Instructions#Windows.md) (Microsoft Visual Studio) using the AMD OpenGL ES 2.0 Emulator or PowerVR Khronos OpenGL ES 2.0 SDK
  * [WebGL](Instructions#WebGL.md)
  * [Android](Instructions#Android.md) 2.2+
  * [Linux](Instructions#Linux.md)
  * [Blackberry](Instructions#Blackberry.md)

# iPhone #

## Prerequisites ##
In order to be able to build and run the code samples, you will need:

  * Mac OS X 10.6.5 or later
  * iOS 4.2 SDK

Please checkout the source code from the subversion repository by doing:

```
svn checkout http://opengles-book-samples.googlecode.com/svn/trunk/ opengles-book-samples-read-only
```

The iPhone projects are located in the `/iPhone` directory.

## Build Instructions ##
Instructions for building and using the samples are in an e-Chapter on the iPhone 3GS available for download in PDF format from this link: http://www.opengles-book.com/OpenGL_ES_20_Programming_Guide_iPhone_eChapter.pdf.

# Windows #

## Prerequisites ##
In order to be able to build and run the code samples, you will need:
  * Microsoft Windows XP or Windows Vista/7
  * An OpenGL 2.0-capable Graphics Card
  * Microsoft Visual Studio 2005 or Microsoft Visual Studio  2008 (you can also use the free Express Edition available from Microsoft at http://www.microsoft.com/express/download/.

You will need to download and install the following:

In order to build and run the code samples, you will need

  1. AMD's OpenGL ES 2.0 Emulator which can be downloaded from http://www.opengles-book.com/ESEmulator.2009-04-28-v1.4.APRIL_2009_RELEASE.msi.  Please note that the OpenGL ES 2.0 Emulator is no longer being actively developed or supported by AMD.  The most recent version is provided here for download as is, no support, feature enhancements or bug fixes will be provided by AMD for this software.
  1. In order to view the `RenderMonkey` example workspaces, you will need to download and install `RenderMonkey` v1.81.  This tool can be downloaded from AMD Developer Central at http://developer.amd.com/gpu/rendermonkey/Pages/default.aspx.
  1. In order to build and run the OpenKODE sample in Chapter 15, you will need Acrodea's OpenKODE 1.0 Implementation for Windows. This can be downloaded from http://www.acrodea.co.jp/en/openkode/ (NOTE: if you do not care to build/run the OpenKODE sample in Chapter 15, you can skip this step).

## Examples ##
All of the code samples and `RenderMonkey` workspaces can either be checked out from the opengles-book-samples subversion tree or downloaded from the following link: http://www.opengles-book.com/OpenGL_ES_Programming_Guide_v1.0.2.zip.

  * (Updated 4/19/09 - v1.0.2) Paul Bennett reported two bugs in esGenSphere() in esShapes.c..The new update includes his fixes.
  * (Updated 8/24/08 - v1.0.1) We have received reports that some users are having difficulty running the samples on Nvidia GPUs when using the AMD OpenGL ES 2.0 Emulator.  To workaround this issue, we updated the sample framework to be compatible with the Imagination Technologies PowerVR SDK.  For instructions on using the PowerVR SDK, please see [Setup Instructions Using the PowerVR SDK Alternative: Setup Instructions Using the PowerVR SDK](Instructions#Alternative:.md).
  * For those users running on an Nvidia GPU and still wanting to use the `RenderMonkey` samples, Till Rathmann posted a workaround over at the AMD Developer Forums at the following [link](http://forums.amd.com/devforum/messageview.cfm?catid=347&threadid=106798) (7/26/09).

## Setup Instructions ##
  1. Unzip `OpenGL_ES_Programming_Guide_v1.0.1.zip` to its own folder or checkout the opengles-book-samples project from subversion.
  1. If you have not done so already, install AMD's OpenGL ES 2.0 Emulator.
  1. Copy the following files from `C:\program files\AMD\OpenGL ES 2.0 Emulator v1.1\bin` to the `\Bin` folder:
    * libEGL.dll
    * libGLESv2.dll
  1. Copy the following files from `C:\program files\AMD\OpenGL ES 2.0 Emulator v1.1\lib` to the `\Lib` folder:
    * libEGL.lib
    * libGLESv2.lib
  1. For the OpenKODE sample in Chapter 15, place the following file from Acrodea's OpenKODE Implementation to the `\Lib` folder:
    * libKD.lib

## Alternative: Setup Instructions Using the PowerVR SDK ##

  1. Unzip `OpenGL_ES_Programming_Guide_v1.0.1.zip` to its own folder.
  1. Download Imagination Technologies Khronos OpenGL ES 2.0 SDK from [here](http://www.imgtec.com/powervr/insider/sdkdownloads/index.asp).
  1. Copy the following files from `C:\Imagination Technologies\PowerVR SDK\OGLES2_WINDOWS_PCEMULATION_2.02.22.0756\Builds\OGLES2\WindowsPC\Lib` to the  `\Bin` folder:
    * libEGL.dll
    * libGLESv2.dll
  1. Copy the following files from `C:\Imagination Technologies\PowerVR SDK\OGLES2_WINDOWS_PCEMULATION_2.02.22.0756\Builds\OGLES2\WindowsPC\Lib` to the `\Lib` folder:
    * libEGL.lib
    * libGLESv2.lib
  1. Copy all of the files from `C:\Imagination Technologies\PowerVR SDK\OGLES2_WINDOWS_PCEMULATION_2.02.22.0756\Builds\OGLES2\Include` to the `\Common\Include` folder (overwriting the existing headers).
  1. For the OpenKODE sample in Chapter 15, place the following file from Acrodea's OpenKODE Implementation to the \Lib folder:
    * libKD.lib

# WebGL #
The WebGL sample code is available from the opengles-book-samples subversion repository.

```
svn checkout http://opengles-book-samples.googlecode.com/svn/trunk/ opengles-book-samples-read-only
```

You can also view the WebGL sample code in action at http://www.opengles-book.com/webgl.html.

# Android #
I have ported most of the samples to Java on Android 2.2.  As of this writing, the emulator does not support OpenGL ES 2.0, so you will have to run the samples on your Android 2.2 device.  The code is available in the subversion repository in the `/Android` directory.

## Building with the Eclipse ADT ##
To build the code using Android SDK API 8 (or greater), in Eclipse:

  1. Do Import... -> "Existing Projects into Workspace"
  1. Point to the `/Android' subdirectory
  1. Select all of the example projects to import

That's it.  You should then be able to run on an Android 2.2-device (I have tested them only on the Motorola DroidX, let me know if there are problems on your device).

# Linux #
The Linux versions of the examples have been tested to run against Ubuntu Linux 11.04, 11.11 and Fedora Linux 15. Before trying to compile the source make sure the development environment is set up correctly. To do so, run these commands based on your operating system:

Ubuntu 11.04/11.11:
```
sudo apt-get install make gcc libgles2-mesa-dev
```

Fedora 15:
```
su -c "yum install make gcc mesa-libGLES-devel mesa-libEGL-devel"
```

Note that you will need superuser rights for the environment you are operating in.

## Building for Linux/X11 ##
Once the development environment is setup, compiling of the examples is done using the included Makefile. Type:

```
make
```

and the process should be completed automatically. Final executables for each example are stored in the subfolder tree. The compiled executables are runnable from their respective places.

## Other than Ubuntu/Fedora based Linux platforms ##

The examples are compilable with any Linux/X11 based operating system, which can provide needed requirements. The exact requirements would be development headers for EGL and GLESv2. Those can be obtained from khronos.org directly. Another thing are the EGL and GLESv2 runtime libraries. Those files would be platform specific, and in that case it is suggested to contact your platform vendor for obtaining those. However, majority of the linux distributions are shipping Mesa, which includes GLESv2 and EGL implementations. For these examples the Mesa solution is sufficient, even without hardware acceleration enabled.

The examples have been test driven with following configurations:
  * ATI Radeon HD 3200 graphics with Mesa 7.11-0ubuntu3, Ubuntu 11.10
  * NVidia Quadro FX 2800M/PCI/SSE2 with Mesa 7.11-0ubuntu3, Ubuntu 11.10
  * NVidia Tegra 2, native EGL/GLESv2 drivers, Ubuntu 11.04


# Blackberry #

Please see the [README.md](http://code.google.com/p/opengles-book-samples/source/browse/trunk/BlackBerry/README.md) file in the Blackberry folder of the source tree for instructions on installing and building the samples for the Blackberry Native SDK.
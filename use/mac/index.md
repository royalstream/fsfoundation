---
layout: default
title: Use F# on Mac OSX | The F# Software Foundation
headline: Use F# on Mac OSX
---


### Option 1: Install F# with Xamarin Studio

![logo](/images/thumbs/xamarin-studio.png)&nbsp;[Xamarin Studio](http://xamarin.com/studio) is a free IDE for general purpose development, with freemium add-ins for mobile development. 

* [Install Xamarin Studio](http://xamarin.com/studio) 

You can create new projects and cross-compile projects built in 
Visual Studio and other environments.
See the [Mac, Linux and Cross-Platform Dev Guide](/guides/mac-linux-cross-platform) to
go further. For 64-bit support, see below.

<br />

### Option 2: Install F# alone

To use the F# command-line compiler and tools on Mac OSX:

*  [Install Mono](http://www.go-mono.com/mono-downloads/download.html). Use version 4.2.0 or later.

See the [Mac, Linux and Cross-Platform Dev Guide](/guides/mac-linux-cross-platform) to
go further. For 64-bit support, see below.

<br />

### Option 3: Install F# via Homebrew (64-bit)

F# is installed as part of the Mono homebrew formula:

    brew install mono

You can configure Xamarin Studio to use this 64-bit installation: Preferences > .NET Runtimes > Add > ```/usr/local```

### Option 4: Install F# (64-bit) from source

To use the F# command-line compiler and tools on Mac OSX in 64-bit mode:

* [Get and build a 64-bit installation of the runtime used by F# from source](http://www.mono-project.com/Compiling_Mono_on_OSX). 

  Set the "--prefix" flag, e.g. "--prefix=/mono64"

    ```git clone https://github.com/mono/mono```
    
    ```cd mono```
    
    ```./autogen.sh --prefix=/mono64 --enable-nls=no```
    
    ```make```
    
    ```sudo make install```

* [Compile F# from source](https://github.com/fsharp/fsharp/blob/master/README.md)

  Set the "--prefix" flag, e.g. "--prefix=/mono64"

    ```git clone https://github.com/fsharp/fsharp```
    
    ```cd fsharp```
    
    ```./autogen.sh --prefix=/mono64```
    
    ```make```
    
    ```sudo make install```

* When you run mono, use ```/mono64/bin/mono``` and put ```/mono64/bin``` on your path.  Adjust other applications that launch mono to use this location.

* Xamarin Studio and MonoDevelop run applications in 32-bit mode by default. You can configure additional runtimes under Preferences > .NET Runtimes to benefit from 64-bit execution.

<br />



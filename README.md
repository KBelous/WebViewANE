
# WebViewANE 

WebView Adobe Air Native Extension for OSX 10.10+, Windows Desktop, iOS 9.0+ and Android19+.
This ANE provides access to a more modern webview from AIR.

[ASDocs Documentation](https://tuarua.github.io/asdocs/webviewane/)

-------------

##### Much time, skill and effort has gone into this. Help support the project

[![paypal](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=5UR2T52J633RC)

##### IDE Software provided by JetBrains
[![Jetbrains](https://raw.githubusercontent.com/tuarua/WebViewANE/master/screenshots/jetbrains.png)](https://www.jetbrains.com)

-------------

## Windows
The Windows version utilises the [CefSharp WinForms](https://github.com/cefsharp/CefSharp) version of Chromium Embedded Framework.

##### Dependencies
From the command line cd into /example and run:
````shell
bash get_dependencies.ps1
`````

##### Windows Installation - Important!
* Download cef_binaries_x86.zip from the latest [release tag](https://github.com/tuarua/WebViewANE/releases)
* Unzip the contents of cef_binaries_x86.zip into the bin folder of your AIRSDK. 
* Copy the contents of the "cef_sharp_libs_x86" folder into the bin folder of your AIRSDK. 

The location of this will vary depending on your IDE. These dlls and other cef files need to reside in the folder where adl.exe is run from.
* CEF was built with MS Visual Studio 2013. As such your machine (and user's machines) will need to have Microsoft Visual C++ 2013 Redistributable (x86) runtime installed.
http://download.microsoft.com/download/2/E/6/2E61CFA4-993B-4DD4-91DA-3737CD5CD6E3/vcredist_x86.exe

* This ANE was built with MS Visual Studio 2015. As such your machine (and user's machines) will need to have Microsoft Visual C++ 2015 Redistributable (x86) runtime installed.
https://www.microsoft.com/en-us/download/details.aspx?id=48145

* This ANE also uses .NET 4.6 Framework. As such your machine (and user's machines) will need to have to have this installed.
https://www.microsoft.com/en-us/download/details.aspx?id=48130

* For release builds, the cef_binaries_x86 and cef_sharp_libs_x86 files need to be packaged in the same folder as your exe.  
It is highly recommended you package your app for release using an installer.  
Please see the win_installer folder for an example Inno Setup project which handles .NET 4.6 and MSVC2013 and MSV2015 dependencies.

* The Cef view and processes can only be attached once to your app. Therefore only one instance can be created and used.

##### Windows 64bit

The Adobe AIRSDK 64bit BETA is available here:
https://fpdownload.macromedia.com/pub/labs/flashruntimes/air/win64SDK/AIRSDK_Compiler.zip

If you are using the 64bit version follow the above instructions replacing x86 with x64 where applicable

## OSX

The OSX version utilises the native WKWebView.

##### Dependencies
From the command line cd into /example and run:
````shell
bash get_dependencies.sh
`````

````xml
<extensions>
<extensionID>com.tuarua.CommonDependencies</extensionID>
</extensions>
`````
````actionscript
private var commonDependenciesANE:CommonDependencies = new CommonDependencies();
`````

## iOS

The OSX version utilises the native WKWebView.

##### Dependencies
From the command line cd into /example-mobile and run:
````shell
bash get_ios_dependencies.sh
`````

### Running on Simulator

The example project can be run on the Simulator from IntelliJ using AIR 28.

### Running on Device

The example project can be run on the device from IntelliJ using AIR 28.



### Prerequisites

You will need

- Xcode 9.1 / AppCode
- IntelliJ IDEA
- AIR 28

## Android
The Android version utilises the native WebView. 

##### Dependencies
From the command line cd into /example-mobile and run:
````shell
bash get_android_dependencies.sh
`````


![alt tag](https://raw.githubusercontent.com/tuarua/WebViewANE/master/screenshots/screenshot1.jpg)



### References
* [https://developer.apple.com/reference/webkit/wkwebview]
* [https://github.com/cefsharp/CefSharp]




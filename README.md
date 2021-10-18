# NBPackage Test Installers

Test configuration files for packaging Apache NetBeans and JDK using
[NBPackage](https://github.com/apache/netbeans-tools/pull/47).

Clone and build NBPackage. Download the Apache NetBeans 12.5 zip distribution into this directory. Download and
configure the JDK and build tools for the relevant configuration as described below. Execute the build using
`./nbpackage -v --config nb125-TYPE.properties --input netbeans-12.5-bin.zip`.

## Windows InnoSetup installer

The `nb125-windows.properties` configuration requires an installation of [Inno Setup](https://jrsoftware.org/isinfo.php). On Linux, this can be installed using `wine`. The configuration file is setup to build on Linux by
calling the included `issc.sh` script - change the configuration file to directly invoke `ISCC.exe` on Windows.

Download the relevant JDK into this directory. Change the runtime link if using a different JDK, and update the
license file if using a JDK from a different vendor.

## Linux AppImage x86_64

The `nb125-linux-x86_64.properties` configuration requires a copy of
[`appimagetool-x86_64.AppImage`](https://github.com/AppImage/AppImageKit/releases/) to be downloaded to this
directory and made executable.

Download the relevant JDK into this directory, changing the runtime link in the configuration file if needed.

## Linux AppImage Arm

The `nb125-linux-arm.properties` configuration is suitable for building a Linux AppImage for running on an
`armhf` system such as Raspberry Pi OS. It must be built on such a machine.

 The configuration requires a copy of
[`appimagetool-armhf.AppImage`](https://github.com/AppImage/AppImageKit/releases/) to be downloaded to this
directory and made executable.

Download the relevant JDK into this directory, changing the runtime link in the configuration file if needed.


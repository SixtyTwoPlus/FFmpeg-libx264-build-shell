# FFmpeg-libx264-build-shell
## LibURL
 * libx264:https://www.videolan.org/developers/x264.html
 * ffmpeg:https://github.com/FFmpeg/FFmpeg

## build-x264.sh
### x264 iOS build script

See https://github.com/kewlbear/FFmpeg-iOS for integration with FFmpeg and more.

This is a shell script to build x264 for iOS apps.

Tested with:

* x264-snapshot-20160814-2245-stable
* Xcode 9.2

### Usage

* Untar the source code into a folder named x264

* To build everything:

        ./build-x264.sh

* To build for arm64:

        ./build-x264.sh arm64

* To build fat library for armv7 and x86_64 (64-bit simulator):

        ./build-x264.sh armv7 x86_64

* To build fat library from separately built thin libraries:

        ./build-x264.sh lipo

* Library and Header Files are in
	./x264-iOS
  
* Update ios-version to 8.0

## FFmpeg iOS build script

See the following repository for Swift package, .xcframeworks and more:

https://github.com/kewlbear/FFmpeg-iOS

[![Build Status](https://travis-ci.org/kewlbear/FFmpeg-iOS-build-script.svg?branch=master)](https://travis-ci.org/kewlbear/FFmpeg-iOS-build-script)

This is a shell script to build FFmpeg libraries for iOS and tvOS apps.

Tested with:

* FFmpeg 4.3.1
* Xcode 12.2

### Requirements

* https://github.com/libav/gas-preprocessor
* yasm 1.2.0

### Usage

Use build-ffmpeg-tvos.sh for tvOS.

* To build everything:

        ./build-ffmpeg.sh

* To build arm64 libraries:

        ./build-ffmpeg.sh arm64

* To build fat libraries for armv7 and x86_64 (64-bit simulator):

        ./build-ffmpeg.sh armv7 x86_64

* To build fat libraries from separately built thin libraries:

        ./build-ffmpeg.sh lipo
	
* Add build-ffmpeg.sh x264 support

### Download

You can download a binary for FFmpeg 4.3.1 release at https://downloads.sourceforge.net/project/ffmpeg-ios/ffmpeg-ios-master.tar.bz2

### External libraries

You should link your app with

* libz.dylib
* libbz2.dylib
* libiconv.dylib

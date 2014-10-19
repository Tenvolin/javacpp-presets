
 * Include new `createIndexer()` method in `CvMat`, `IplImage`, `Mat`, etc. for easy and efficient multidimensional access of data ([issue #317](http://code.google.com/p/javacv/issues/detail?id=317))
 * Deprecate `get*Buffer()` methods in favor of a better named and generic `createBuffer()` method
 * Fix `java.lang.UnsatisfiedLinkError` when allocating `opencv_core.Mat`, among others ([issue javacv:9](https://github.com/bytedeco/javacv/issues/9) and [issue javacv:28](https://github.com/bytedeco/javacv/issues/28))
 * Force OpenCV to build with GCC 4.6, as newer versions are known to hang on Android 2.2 ([issue android:43819](https://code.google.com/p/android/issues/detail?id=43819))
 * Upgrade presets for FFmpeg 2.4.2, LLVM 3.5.0, videoInput, where the latest code got merged into the master branch
 * Add callbacks for Tesseract according to new functionality in JavaCPP
 * Fix missing dependency of `opencv_contrib` on `opencv_nonfree`
 * Skip functions that are not actually implemented in `avdevice`, causing load failures on Android
 * Update presets for FFmpeg where `avcodec` now inherits from `swresample` ([issue #13](https://github.com/bytedeco/javacpp-presets/issues/13))
 * Add a `README.md` file to each presets with links to original project, Java API documentation, and sample usage
 * Add missing overloaded methods with `PointerPointer` parameters in LLVM module

### July 27, 2014 version 0.9
 * Add libmp3lame to FFmpeg builds ([issue javacv:411](https://code.google.com/p/javacv/issues/detail?id=448))
 * Upgrade presets for FFmpeg 2.3, FlyCapture 2.6.3.4 ([pull #6](https://github.com/bytedeco/javacpp-presets/pull/6), [issue #8](https://github.com/bytedeco/javacpp-presets/issues/8)), libfreenect 0.5
 * Make the `cppbuild.sh` scripts install native libraries inside the `cppbuild` subdirectories, instead of on the system
 * Include new `platform.dependency` and `platform.dependencies` properties to let users depend easily on the artifacts that contain native libraries
 * Add presets for flandmark 1.07 ([pull #9](https://github.com/bytedeco/javacpp-presets/pull/9)), FFTW 3.3.4, GSL 1.16, LLVM 3.4.2, Leptonica 1.71, Tesseract 3.03-rc1
 * Fix missing `static` keyword on methods annotated with an `@Adapter` ([issue #3](https://github.com/bytedeco/javacpp-presets/issues/3))
 * Turn `Mat.createFrom()` into a static factory method, and make `Mat.copyFrom()` call `Mat.create()` as appropriate ([issue #1](https://github.com/bytedeco/javacpp-presets/issues/1))
 * Add missing `native_camera` modules of `opencv_highgui` for Android
 * Fix functions from `opencv_stitching` not accepting a `MatVector` as apparently intended by the API (issue javacv:466)

### April 28, 2014 version 0.8
 * Move from Google Code to GitHub as main source code repository
 * Rename the `com.googlecode.javacpp` package to `org.bytedeco.javacpp`
 * Appended the version of the parent artifact to the ones of the child modules, in an effort to avoid conflicts
 * Updated `cppbuild.sh` scripts with support for the "android-x86" platform (issue javacv:411), thanks to Xavier Hallade
 * Added presets for PGR FlyCapture 1.7
 * Fixed compilation errors on Android, Mac OS X, and Windows
 * Upgraded to OpenCV 2.4.9, FFmpeg 2.2.1, libdc1394 2.2.2, and libfreenect 0.4
 * Introduced build scripts, based on the CPPJARs package of JavaCV, to install native C/C++ libraries
 * Ported various helper classes and methods from JavaCV
 * Inserted missing dependency entries in the `pom.xml` files of the child modules
 * Added presets for the C++ API of OpenCV 2.4.8, which can now be parsed due to the latest changes in JavaCPP

### January 6, 2014 version 0.7
 * Fixed JavaCPP properties not getting set by the parent `pom.xml` file
 * Added presets for the C API of OpenCV 2.4.8, FFmpeg 2.1.x, libfreenect 0.2 (OpenKinect), videoInput 0.200, and ARToolkitPlus 2.3.0

### September 15, 2013 version 0.6
Initial release


Acknowledgments
---------------
This project was conceived at the [Okutomi & Tanaka Laboratory](http://www.ok.ctrl.titech.ac.jp/), Tokyo Institute of Technology, where I was supported for my doctoral research program by a generous scholarship from the Ministry of Education, Culture, Sports, Science and Technology (MEXT) of the Japanese Government. I extend my gratitude further to all who have reported bugs, donated code, or made suggestions for improvements (details above)!
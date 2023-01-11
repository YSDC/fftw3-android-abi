
# FFTW3 for Android
_________

Repository for compiling [FFTW3](http://www.fftw.org/) on Android. This is a fork I did because the original repository was building only for a single architecture. In this repository you have the solution to select for which you want to deploy. 

The current version of the FFTW3 is unknown and need to be identified. 


In order to built this project you need to download and install [Android NDK](https://developer.android.com/studio/projects/add-native-code.html#download-ndk). Then simply run the following command to build FFTW3:

```bash
./build.sh
```
The result is available in the 'obj' folder.

The next step, if you want to add in an Android project is describe [in this repository](https://developer.android.com/studio/projects/add-native-code.html#download-ndk)

### What's next
In order to use the generated files (libfftw3.a files in each of the architecture folders), you need to add them in the jni libs folder of an Android NDK module, and hte fftw3.h file in the cpp folder of that same module. 
We have develop a wrapper that integrates it under the name 'TBD'.

### Single-precision 

If you want to compile a single-precision version of FFTW you need add the following defines to [config.h](jni/fftw3/config.h)

```C
#define BENCHFFT_SINGLE 1
#define FFTW_SINGLE 1
```
Then follow the instructions at: <http://www.fftw.org/fftw3_doc/Precision.html#Precision>.

For more information send me an email at <djohannotapp@gmail.com> or the owner of the original repository <lauszus@gmail.com>.

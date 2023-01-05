
# FFTW3 for Android
_________

Repository for compiling [FFTW3](http://www.fftw.org/) on Android. This is a fork I did because the original repository was building only for a single architecture. In this repository you have the solution to select for which you want to deploy. 

I also updated the FFTW3 source file. The current version used is the 3.3.10.


In order to built this project you need to download and install [Android NDK](https://developer.android.com/studio/projects/add-native-code.html#download-ndk). Then simply run the following command to build FFTW3:

```bash
./build.sh
```
The result is available in the 'obj' folder.

The next step, if you want to add in an Android project is describe [in this repository](https://developer.android.com/studio/projects/add-native-code.html#download-ndk)

### Single-precision 

If you want to compile a single-precision version of FFTW you need add the following defines to [config.h](jni/fftw3/config.h)

```C
#define BENCHFFT_SINGLE 1
#define FFTW_SINGLE 1
```
Then follow the intructions at: <http://www.fftw.org/fftw3_doc/Precision.html#Precision>.

For more information send me an email at <djohannotapp@gmail.com> or the owner of the original repository <lauszus@gmail.com>.

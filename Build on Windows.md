# Building on Windows

## MinGW
* Download MinGW
* Inside MinGW Installation Manager install -> Basic Setup
* "mingw-developer-toolkit" -> Mark For Installation
* "mingw32-base bin" -> Mark For Installation
* "mingw32-gcc-g++ bin" -> Mark For Installation
* "msys-base bin" -> Mark For Installation
* Installation -> Apply All Changes
* Add to system environment variables "c:\MinGW\bin" "c:\MinGW\msys\1.0\bin"
* Create "c:\MinGW\msys\1.0\etc\fstab" and add the line "C:\MinGW /mingw"

## Other Install
* CMake 3.0.1 installed
* Boost 1.55 extracted to <boost>
* Googletest 1.7 extracted to <gtest>
* LevelDB extracted to <leveldb>
* mu_coin source in <mu_coin_source>

## Run MSYS shell
* Run "c:/MinGW/msys/1.0/msys.bat"
* Run "export PATH=$PATH:/c/MinGW/bin/" inside MSYS shell to add compiler tools to path

## Build LevelDB

## Build Boost
* Inside directory <boost> run "bootstrap.bat mingw"
* Run "b2"

## Build Googletest
* Inside directory <gtest> run 'cmake -G "MSYS Makefiles"'
* Run "make"

## Set up CMake
* Run cmake-gui
* Set "Where is the Source Code" to <mu_coin_source>
* Set "Where to build the binaries" to <mu_coin_build> which should not be inside <mu_coin_source>
* Push "Configure"
* When asked "Build directory does not exist, should I create it" push "Yes"
* Under "Specify the generator for this project, select "MinGW Makefiles"
* Select "Use default native compilers"
* Push "Finish"
* Add Entry Name "CMAKE_MODULE_PATH" Type "PATH" Value <mu_coin_source>
* Push "Generate"
* Modify entry "BerkeleyDB_INCLUDE_DIR"
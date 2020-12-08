
# Pyxodr - Read opendrive with python parser
This project is fork from [here](https://github.com/javedulu/ad-xolib) with some modification for utf-8 based user. Also, test building the python API with python 3.8 (built test with VS2017, VS2019 in Windows 10).

C++ library for Parsing OpenScenario (1.0.0) & OpenDrive format files (1.6) with Python bindings for 3.+ 

## Introduction <a name="introduction"></a>

This repository provides a library for reading ASAM's OpenStandards OpenScenario & OpenDrive Data files, the parsing conforms to

[ASAM OpenDRIVE 1.6
Specification](https://www.asam.net/index.php?eID=dumpFile&t=f&f=3495&token=56b15ffd9dfe23ad8f759523c806fc1f1a90a0e8)

[ASAM OpenScenario 1.0.0
Specification](https://www.asam.net/index.php?eID=dumpFile&t=f&f=3496&token=df4fdaf41a8463e585495001cc3db3298b57d426)

![Image of asam-logo](https://www.asam.net/typo3conf/ext/asam_cms/Resources/Public/Images/asam-logo.svg)


## Inspiration <a name="inspiration"></a>


- https://github.com/carla-simulator/map
- https://github.com/esmini/esmini.git


## Getting started <a name="started"></a>
The project is compiled with c++14 enabled compiler, choose your stack accordingly .

#### Build from Source <a name="build"></a>

```bash
git clone https://github.com/moonstarsky37/ad-xolib
cd ad-xolib
git submodule update --init --recursive 
# build by cmake, if you not link a alias, the default is "C:\Program Files\CMake\bin\cmake.exe"
# i.e below command can be using as 
# "C:\Program Files\CMake\bin\cmake.exe" . -B build 
cmake . -B build # it will create a folder named "build", if not, created by "mkdir build"
cmake . --target build

```

To now, you will create a folder named build with following code.

![](https://i.imgur.com/O0cZZGC.png)
Open the "ad-xolib.sln" with VS.
And Click the "Local Window Debugger" will create the pybind result python API.
That is, after building the src, it will create some folder like this the API file is under the folder named "pybind".

![](https://i.imgur.com/Me3xv8w.png)

In my case, the builted result under python 3.8 will like following:

![](https://i.imgur.com/Fd1jaW2.png)

If you missing any of *.dll in this folder, just copy 
```
1. ./build/src/xosc/Debug/xosc.dll
2. ./build/src/xodr/Debug/xodr.dll
3. ./build/deps/pugixml/Debug/pugixml.dll
```
to ```./build/pybind``` folder.

Finally, you can import pyxodr now and read opendrive file

![](https://i.imgur.com/9NhAlKq.png)
![](https://i.imgur.com/A9CwZip.png)



## Alternatives <a name="alternatives"></a>
- [https://github.com/JensKlimke/odrparser](https://github.com/JensKlimke/odrparser)- OpenDrive 1.5 
- [https://github.com/DLR-TS/xodr](https://github.com/DLR-TS/xodr) - OpenDrive 1.4
- [https://github.com/pyoscx/pyoscx](https://github.com/pyoscx/pyoscx) - pyoscx
- [https://github.com/carla-simulator/scenario_runner](https://github.com/carla-simulator/scenario_runner) - Scenario Runner
- [https://github.com/MrMushroom/CarlaScenarioLoader](https://github.com/MrMushroom/CarlaScenarioLoader) - CarlaScenarioLoader

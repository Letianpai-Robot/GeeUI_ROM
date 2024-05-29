## Download GeeUI ROM method:

Download address:

Download the system as shown in the figure:
![rom_zip_list](docs/20240529-032231.jpeg)
## Decompression:

Extract the ROM into the Linux system, then execute the following command to merge the compressed files and decompress them
```
cat geeui_android11_20240528.tar.gz.* | gzip -c > geeui_android11_20240528.tar.gz
tar -zxvf geeui_android11_20240528.tar.gz
```

## Compilation:
After decompression, enter the system directory for compilation and execute the following command to compile:

Compiling Android requires high machine configuration requirements:
64 bit CPU
16GB physical memory+swap memory
250GB of free disk space
Suggest using Ubuntu 18.04 operating system or higher
Ubuntu 16.04 or 18.04 software package installation reference:
```
sudo apt-get update

sudo apt-get install git gnupg flex bison gperf libsdl1.2-dev \
libesd-java libwxgtk3.0-dev squashfs-tools build-essential zip curl \
libncurses5-dev zlib1g-dev pngcrush schedtool libxml2 libxml2-utils \
xsltproc lzop libc6-dev schedtool g++-multilib lib32z1-dev lib32ncurses5-dev \
lib32readline-dev gcc-multilib libswitch-perl libssl-dev unzip zip device-tree-compiler \
liblz4-tool python-pyelftools python3-pyelftools -y
```

```
. build/envsetup.sh
lunch  2
./build.sh -AKUup
```
Compilation completed, the compiled system image update.img can be found in out
## Burn
Please refer to the following article for the burning method. Change the burning package to the image compiled above.
[Burning method](https://global.letianpai.com/all/?p=1680&v=8528837ceeea)

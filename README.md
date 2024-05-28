## 下载GeeUI ROM方式：

下载地址：

下载系统如图：
![rom_zip_list](docs/20240529-032231.jpeg)
## 解压：

解压ROM到linux系统中，然后执行如下指令,合并压缩文件，并解压
```
cat geeui_android11_20240528.tar.gz.* | gzip -c > geeui_android11_20240528.tar.gz
tar -zxvf geeui_android11_20240528.tar.gz
```

### 编译：
解压后可，进入系统目录进行编译，执行如下指令编译：

```
. build/envsetup.sh
lunch  2
./build.sh -AKUup
```
编译完成，可在out中找到编译好的系统镜像 update.img
### 烧录
使用rk_tools 烧录工具
烧录方式参见下面文章，将其中的烧录包改为上面编译出来的镜像即可。
[烧录方式](https://global.letianpai.com/all/?p=1680&v=8528837ceeea)

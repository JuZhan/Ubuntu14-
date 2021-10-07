由于ROS版本限制所以只能使用的ubuntu14.4下的一些记录

### 第一步 右键命令行
```
sudo apt-get install nautilus-open-terminal
```
安装这个，然后就可以文件夹右键打开命令行了

### 远程服务器文件夹
文件夹里面的 `Network` 的 `Connect to Server`

格式比如：`sftp://172.31.233.78/home/juzhan`

### vscode远程写代码 (时代变了，直接官方remote插件)
1. 安装插件 `Remote Workspace`
2. 写个配置文件，后缀名 `.code-workspace`
3. 格式如下：
```
{
    "folders": [{
        "uri": "sftp://my-user:my-password@my_server.example.com:my_folder_path",
        "name": "Whatever"
    }]
}
```
4. `File` -> `Open Workspace` 打开这 `code-workspace` 文件就可以了

### git最新版本
```
sudo add-apt-repository ppa:git-core/ppa
sudo apt-get install git
```

### pip安装最新
```
curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py 
sudo python get-pip.py
```

### pip 的阿里源
在 `~/.pip/pip.conf`
```
[global]
index-url = http://mirrors.aliyun.com/pypi/simple/                          
[install]
trusted-host=mirrors.aliyun.com
```

### conda的清华源
在`~/.condarc`
```
channels:
  - http://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/
  - http://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
  - http://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/pytorch/
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
  - defaults
show_channel_urls: true
```

### python 2.7 对应的ipython最高版
一般是 `ipython 5.x.x`，比如： `sudo pip install ipython==5.3.0`

### ubuntu的字体
`sudo apt-get install ttf-wqy-microhei  #文泉驿-微米黑`

### ubuntu美化
> https://blog.csdn.net/ghty520/article/details/79524623

### 截图与录制视频
`sudo apt-get install kazam`

### 安全更新cmake到3.0以上版本
> https://blog.csdn.net/love1055259415/article/details/79875113
> 
> https://zhuanlan.zhihu.com/p/93480024
>

> https://askubuntu.com/questions/829310/how-to-upgrade-cmake-in-ubuntu

```
In the new version of cmake (ex: 3.9.6), to install, download tar file from https://cmake.org/download/. Extract the downloaded tar file and then:

cd $CMAKE_DOWNLOAD_PATH
./configure
make
sudo make install
```

> 完美的一句：`sudo pip install --upgrade cmake==3.13.2`

### pytorch的cuda8.0，python2.7安装
```
sudo pip install http://download.pytorch.org/whl/cu80/torch-0.4.1-cp27-cp27mu-linux_x86_64.whl
or > pip install http://download.pytorch.org/whl/cu80/torch-0.1.12.post2-cp27-none-linux_x86_64.whl
```
### blender 2.79的python
> 是系统内自带的python 3.6，所以安装第三方库和pip都是python3.6上进行的

### gazebo的坑
> 自定义模型的mesh路径必须是 file:// 开头，model:// 开头的是默认路径
> 
> gazebo似乎会对默认路径下的模型几何体有初始化到缓存什么的，创建后有碰撞体积
> 
> 但是自己导入的模型如果也是model://开头，就没有碰撞体积了

### OpenEXR 安装问题（为了在blender里面安装bpycv遇见的）[2021.05.03更新：好像官方用了新的方法安装bpycv，更简单了]

+ 情况一：没有“Python.h”，参考bpycv的链接。
+ 情况二：没有“pyconfig.h”，找现有的python环境里面，include文件夹下复制一份。
+ 情况三：没有“ImathBox.h”，得自己手动安装openexrpython，前往这里，找到对应的版本下载https://www.lfd.uci.edu/~gohlke/pythonlibs/

### E-pick
> http://wiki.ros.org/robotiq
> 
> https://github.com/ros-industrial/robotiq
>
> https://github.com/ros-industrial/robotiq/pull/175/files

### Failed to connect to github.com port 443
```
git config --global --unset http.proxy
```

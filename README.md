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

### pytorch的cuda8.0，python2.7安装
`sudo pip install http://download.pytorch.org/whl/cu80/torch-0.4.1-cp27-cp27mu-linux_x86_64.whl`
`pip install http://download.pytorch.org/whl/cu80/torch-0.1.12.post2-cp27-none-linux_x86_64.whl`

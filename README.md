由于ROS版本限制所以只能使用的ubuntu14.4下的一些记录

### 第一步 右键命令行
```
sudo apt-get install nautilus-open-terminal
```
安装这个，然后就可以文件夹右键打开命令行了

### 远程服务器文件夹
文件夹里面的 `Network` 的 `Connect to Server`

格式比如：`sftp://172.31.233.78/home/juzhan`

### vscode远程写代码
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

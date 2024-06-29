---
layout: post

title: 用VSCode实现HelloWorld案例

tag: ROS

typora-root-url: ..\images\posts
---

# 1.创建工作空间并初始化

```shell
mkdir -p 自定义空间名称/src
cd 自定义空间名称
catkin_make  #自动生成构建目录
```

# 2.用VSCode打开

```shell
code .  #在工作区文件夹下
```

# 3.配置json文件

按住**Ctrl+Shift+B**，在弹出的窗口中选择**catkin_make:build右边的小齿轮**

修改task.json文件

```json
{
    "version":"2.0.0",
    "tasks":[
        {
            "label": "catkin_make:debug",
            "type": "shell",
            "command": "catkin_make",
            "args": [],
            "group":{"kind": "build","isDefault": true},
            "presentation":{
                "reveal": "always"            
            },
            "problemMatcher": "$msCompile"        
        }    
    ]
}
```

# 4.编译

按住`Ctrl+Shift+B`，默认编译整个工作空间

# 5.新建/编辑/编译运行功能包

右键工作区下的src文件夹，选择`Create Catkin Package`

第一个弹出框：**输入功能包的包名**

第二个弹出框：**功能包的依赖**，一般为

```
roscpp rospy std_msgs
```


---
---

# Centos镜像使用帮助

## 收录架构

  + i386

  + x86_64

## 收录版本

  + 5

  + 6

  + 7

## 使用说明

首先备份CentOS-Base.repo 

    
    
    mv /etc/yum.repos.d/CentOS-Base.repo /etc/yum.repos.d/CentOS-Base.repo.backup

下载对应版本的CentOS-Base.repo, 放入/etc/yum.repos.d/ 

这是CentOS 5的: 

[CentOS-Base.repo](/wiki/_export/code/mirrors/help/CentOS-Basecc37.repo?codeblock=1 "下载片段")

    
    
    
    # CentOS-Base.repo
    #
    # The mirror system uses the connecting IP address of the client and the
    # update status of each mirror to pick mirrors that are updated to and
    # geographically close to the client.  You should use this for CentOS updates
    # unless you are manually picking other mirrors.
    #
    # If the mirrorlist= does not work for you, as a fall back you can try the 
    # remarked out baseurl= line instead.
    #
    #
     
    [base]
    name=CentOS-$releasever - Base - mirrors.ustc.edu.cn
    baseurl=http://mirrors.ustc.edu.cn/centos/$releasever/os/$basearch/
    #mirrorlist=http://mirrorlist.centos.org/?release=$releasever&arch=$basearch&repo=os
    gpgcheck=1
    gpgkey=http://mirrors.ustc.edu.cn/centos/RPM-GPG-KEY-CentOS-5
     
    #released updates 
    [updates]
    name=CentOS-$releasever - Updates - mirrors.ustc.edu.cn
    baseurl=http://mirrors.ustc.edu.cn/centos/$releasever/updates/$basearch/
    #mirrorlist=http://mirrorlist.centos.org/?release=$releasever&arch=$basearch&repo=updates
    gpgcheck=1
    gpgkey=http://mirrors.ustc.edu.cn/centos/RPM-GPG-KEY-CentOS-5
     
    #additional packages that may be useful
    [extras]
    name=CentOS-$releasever - Extras - mirrors.ustc.edu.cn
    baseurl=http://mirrors.ustc.edu.cn/centos/$releasever/extras/$basearch/
    #mirrorlist=http://mirrorlist.centos.org/?release=$releasever&arch=$basearch&repo=extras
    gpgcheck=1
    gpgkey=http://mirrors.ustc.edu.cn/centos/RPM-GPG-KEY-CentOS-5
     
    #packages used/produced in the build but not released
    [addons]
    name=CentOS-$releasever - Addons - mirrors.ustc.edu.cn
    baseurl=http://mirrors.ustc.edu.cn/centos/$releasever/addons/$basearch/
    #mirrorlist=http://mirrorlist.centos.org/?release=$releasever&arch=$basearch&repo=addons
    gpgcheck=1
    gpgkey=http://mirror.centos.org/centos/RPM-GPG-KEY-CentOS-5
     
    #additional packages that extend functionality of existing packages
    [centosplus]
    name=CentOS-$releasever - Plus - mirrors.ustc.edu.cn
    baseurl=http://mirrors.ustc.edu.cn/centos/$releasever/centosplus/$basearch/
    #mirrorlist=http://mirrorlist.centos.org/?release=$releasever&arch=$basearch&repo=centosplus
    gpgcheck=1
    enabled=0
    gpgkey=http://mirrors.ustc.edu.cn/centos/RPM-GPG-KEY-CentOS-5
     
    #contrib - packages by Centos Users
    [contrib]
    name=CentOS-$releasever - Contrib - mirrors.ustc.edu.cn
    baseurl=http://mirrors.ustc.edu.cn/centos/$releasever/contrib/$basearch/
    #mirrorlist=http://mirrorlist.centos.org/?release=$releasever&arch=$basearch&repo=contrib
    gpgcheck=1
    enabled=0
    gpgkey=http://mirrors.ustc.edu.cn/centos/RPM-GPG-KEY-CentOS-5

这是CentOS 6的: 

[CentOS-Base.repo](/wiki/_export/code/mirrors/help/CentOS-Basec273.repo?codeblock=2 "下载片段")

    
    
    
    # CentOS-Base.repo
    #
    # The mirror system uses the connecting IP address of the client and the
    # update status of each mirror to pick mirrors that are updated to and
    # geographically close to the client.  You should use this for CentOS updates
    # unless you are manually picking other mirrors.
    #
    # If the mirrorlist= does not work for you, as a fall back you can try the 
    # remarked out baseurl= line instead.
    #
    #
     
    [base]
    name=CentOS-$releasever - Base - mirrors.ustc.edu.cn
    baseurl=http://mirrors.ustc.edu.cn/centos/$releasever/os/$basearch/
    #mirrorlist=http://mirrorlist.centos.org/?release=$releasever&arch=$basearch&repo=os
    gpgcheck=1
    gpgkey=http://mirrors.ustc.edu.cn/centos/RPM-GPG-KEY-CentOS-6
     
    #released updates 
    [updates]
    name=CentOS-$releasever - Updates - mirrors.ustc.edu.cn
    baseurl=http://mirrors.ustc.edu.cn/centos/$releasever/updates/$basearch/
    #mirrorlist=http://mirrorlist.centos.org/?release=$releasever&arch=$basearch&repo=updates
    gpgcheck=1
    gpgkey=http://mirrors.ustc.edu.cn/centos/RPM-GPG-KEY-CentOS-6
     
    #additional packages that may be useful
    [extras]
    name=CentOS-$releasever - Extras - mirrors.ustc.edu.cn
    baseurl=http://mirrors.ustc.edu.cn/centos/$releasever/extras/$basearch/
    #mirrorlist=http://mirrorlist.centos.org/?release=$releasever&arch=$basearch&repo=extras
    gpgcheck=1
    gpgkey=http://mirrors.ustc.edu.cn/centos/RPM-GPG-KEY-CentOS-6
     
    #additional packages that extend functionality of existing packages
    [centosplus]
    name=CentOS-$releasever - Plus - mirrors.ustc.edu.cn
    baseurl=http://mirrors.ustc.edu.cn/centos/$releasever/centosplus/$basearch/
    #mirrorlist=http://mirrorlist.centos.org/?release=$releasever&arch=$basearch&repo=centosplus
    gpgcheck=1
    enabled=0
    gpgkey=http://mirrors.ustc.edu.cn/centos/RPM-GPG-KEY-CentOS-6
     
    #contrib - packages by Centos Users
    [contrib]
    name=CentOS-$releasever - Contrib - mirrors.ustc.edu.cn
    baseurl=http://mirrors.ustc.edu.cn/centos/$releasever/contrib/$basearch/
    #mirrorlist=http://mirrorlist.centos.org/?release=$releasever&arch=$basearch&repo=contrib
    gpgcheck=1
    enabled=0
    gpgkey=http://mirrors.ustc.edu.cn/centos/RPM-GPG-KEY-CentOS-6

这是CentOS 7的: 

[CentOS-Base.repo](/wiki/_export/code/mirrors/help/CentOS-Base4f98.repo?codeblock=3 "下载片段")

    
    
    
    # CentOS-Base.repo
    #
    # The mirror system uses the connecting IP address of the client and the
    # update status of each mirror to pick mirrors that are updated to and
    # geographically close to the client.  You should use this for CentOS updates
    # unless you are manually picking other mirrors.
    #
    # If the mirrorlist= does not work for you, as a fall back you can try the
    # remarked out baseurl= line instead.
    #
    #
     
    [base]
    name=CentOS-$releasever - Base
    #mirrorlist=http://mirrorlist.centos.org/?release=$releasever&arch=$basearch&repo=os
    baseurl=http://mirrors.ustc.edu.cn/centos/$releasever/os/$basearch/
    gpgcheck=1
    gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7
     
    #released updates
    [updates]
    name=CentOS-$releasever - Updates
    # mirrorlist=http://mirrorlist.centos.org/?release=$releasever&arch=$basearch&repo=updates
    baseurl=http://mirrors.ustc.edu.cn/centos/$releasever/updates/$basearch/
    gpgcheck=1
    gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7
     
    #additional packages that may be useful
    [extras]
    name=CentOS-$releasever - Extras
    # mirrorlist=http://mirrorlist.centos.org/?release=$releasever&arch=$basearch&repo=extras
    baseurl=http://mirrors.ustc.edu.cn/centos/$releasever/extras/$basearch/
    gpgcheck=1
    gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7
     
    #additional packages that extend functionality of existing packages
    [centosplus]
    name=CentOS-$releasever - Plus
    # mirrorlist=http://mirrorlist.centos.org/?release=$releasever&arch=$basearch&repo=centosplus
    baseurl=http://mirrors.ustc.edu.cn/centos/$releasever/centosplus/$basearch/
    gpgcheck=1
    enabled=0
    gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7

运行yum makecache生成缓存 

## 相关链接

官方主页: <http://www.centos.org/>   
邮件列表: <http://www.centos.org/modules/tinycontent/index.php?id=16>  
论坛: <http://www.centos.org/modules/newbb/>   
文档: <http://www.centos.org/docs/>   
Wiki: <http://wiki.centos.org/>   
镜像列表: <http://www.centos.org/modules/tinycontent/index.php?id=32>

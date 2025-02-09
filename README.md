# MR-study

Multi-rotor Study repo.

***

## Man 命令

man 命令是 Linux 操作系统中用于显示手册页（manual page）的重要工具，它提供了对各种命令、函数、库等的详细说明。

#### man 命令有许多参数，以下是一些主要参数的功能：

> -f：显示命令或函数的简短描述。
> -k：使用关键字搜索所有与该关键字相关的手册页。
> -S：指定手册页的搜索路径。
> -a：显示所有与命令或函数相关的手册页。
> -w：显示命令或函数的手册页文件路径。
> -C：指定手册页的格式。
> -l：显示所有手册页的列表。
> -p：显示函数的原型。
> -s：显示指定节的手册页。
> -u：显示未压缩的手册页。
> -h：显示帮助信息 。
> -M：指定手册页的源路径。
>
> 常见的节号包括：
> 1：用户命令
> 2：系统调用
> 3：C 库函数
> 4：设备和特殊文件
> 5：文件格式和约定
> 6：游戏和演示
> 7：杂项
> 8：系统管理命令

#### 使用示例如下：

> 查看命令的使用说明：man ls
> 在所有手册页中搜索关键字：man -k keyword
> 显示所有与命令或函数相关的手册页：man -a command
> 显示命令或函数的手册页文件路径：man -w command
> 显示函数的原型：man -p function
> 显示指定节的手册页：man 2 open
> 显示未压缩的手册页：man -u command
> 指定手册页的源路径：man -M /usr/share/man command

手册页通常包含以下内容：命令或函数的名称、概述和用途，命令或函数的语法格式和参数说明，命令或函数的返回值和错误信息，命令或函数的示例和使用方法，命令或函数的作者、版权和许可证信息。手册页通常被分为多个节（section），每个节包含一类相关的手册页。

例如，我们输入 man ls ，它会在最左上角显示“LS（1）”，在这里，“LS”表示手册名称，而“（1）”表示该手册位于第一节章。同样，我们输入“man ifconfig”它会在最左上角显示“IFCONFIG（8）”。也可以这样输入命令：“man (章节号) 手册名称”。man 是按照手册的章节号的顺序进行搜索的，比如：man sleep ，只会显示 sleep 命令的手册，如果想查看库函数 sleep ，就要输入：man 3 sleep 。在 man 页面中，常用的操作按键及其用途包括：空格键向下翻一页，Page down 向下翻一页，Page up 向上翻一页，home 直接前往首页，end 直接前往尾页，“/”从上至下搜索某个关键词，“?”从下至上搜索某个关键词，“n”定位到下一个搜索到的关键词，“N”定位到上一个搜索到的关键词，“q”退帮助文档。

#### **man命令的主要参数及功能**
man命令拥有众多实用的参数，这些参数赋予了它丰富的功能。
常见的参数包括：

> -a：显示所有匹配的手册页。这意味着会搜索并展示与指定命令或主题相关的所有可用手册页，让您获取全面的信息。
> -f：相当于whatis指令，能够显示给定关键字的简短描述信息。通过这个参数，您可以快速了解某个命令或主题的大致情况。
> -k：用于搜索手册页中与关键字匹配的条目。例如，当您对某个特定的概念或操作有模糊的印象，通过-k参数可以快速找到相关的命令和帮助信息。
> -P：指定在显示内容时使用的分页程序。您可以根据自己的习惯和需求选择合适的分页程序，以更舒适地浏览手册页。
> -M：用于指定man手册搜索的路径。当系统默认的搜索路径无法满足您的需求，或者您有特定的手册存储位置时，这个参数就非常有用。
> 通过这些参数的灵活运用，您可以更高效、更精准地获取man命令提供的帮助信息。

#### **man命令常见的节号及内容**
man手册一般可以分为多个章节，每个章节都包含特定类型的信息。
常见的节号和其内容如下：

> 用户命令：这部分包含了用户在shell环境中可以直接操作的命令或可执行文件，例如ls、cd等常见的基础命令。
> 系统调用：涵盖了操作系统内核提供的接口函数，这些函数通常用于与操作系统内核进行交互。
> 库函数：主要是C语言库中的函数，为开发者在编程中提供了丰富的功能支持。
> 设备文件：对设备文件（通常在/dev下）的相关说明，帮助您了解如何与各种硬件设备进行交互。
> 配置文件：提供了各种配置文件的格式和相关说明，使您能够正确地配置系统和应用程序。
> 游戏：包含了Linux系统中的一些小游戏的相关信息。
> 惯例与协议：例如Linux文件系统、网络协议、ASCII码等的说明，让您深入了解系统的底层规则和标准。
> 系统管理命令：只有管理员可以使用的命令，用于对系统进行管理和维护。
> 根据您的需求选择合适的章节，可以更精准地获取所需的帮助信息。

#### **man命令的使用示例**

以下是一些man命令的使用示例，帮助您更好地理解和运用它：

> 要查看ls命令的手册页面，可以输入：man ls ，系统将展示ls命令的详细用法、参数说明、示例等信息。
> 如果想查看库函数printf，由于库函数通常位于编号为3的手册中，所以要输入：man 3 printf 。
> 若要从所有编号的手册中搜索并全部列出来相关信息，可以输入：man -a sleep ，每次输入:q，可以显示下一个编号的手册搜索结果。
> 通过这些具体的示例，您可以更直观地感受man命令的强大功能和便捷性。

#### **man命令页面的操作按键用途**
在man命令的页面中，有一系列实用的操作按键，方便您浏览和搜索帮助信息。

> 空格键和Page Down键：都可以向下翻一页，让您快速浏览后续内容。
> Page Up键：向上翻一页，便于回顾之前的信息。
> Home键：直接前往首页，快速回到开头。
> End键：直接前往尾页，迅速到达末尾。
> /键：从上至下搜索某个关键词，比如/man ，帮助您快速定位到包含特定关键词的部分。
> ?键：从下至上搜索某个关键词，例如?man 。
> n键：定位到下一个搜索到的关键词。
> N键：定位到上一个搜索到的关键词。
> q键：用于退出帮助文档，当您获取到所需信息或者想要结束浏览时使用。
> 熟练掌握这些操作按键，可以提高您在man命令页面中的操作效率。

***

## tmux命令

列出所有已存在的会话：tmux list-sessions

``	tmux list-sessions     ``

从当前会话中断开连接：tmux detach

``tmux detach``

创建一个新的会话：tmux new -s

``tmux new -s [name]``

连接到一个已存在的会话：tmux attach -t

``tmux attach -t``  

终止一个已存在的会话：tmux kill-session -t

``tmux kill-session -t ``

结束所有进程 tmux kill-server

``tmux kill-server``

> 其他：
> tmux switch -t ： 切换到一个已存在的会话，并将其命名为。
> tmux rename-session ： 重命名一个已存在的会话，从改为。
> tmux split-window -v： 在当前窗口中水平分割一个新窗口。
> tmux split-window -h： 在当前窗口中垂直分割一个新窗口。
> tmux select-pane -t ： 选择一个窗格，并将其编号为。
> tmux resize-pane -t -D ：调整一个窗格的大小，并将其编号为，向下调整行。
> tmux resize-pane -t -U ：调整一个窗格的大小，并将其编号为，向上调整行。
> tmux kill-pane -t ： 终止一个窗格，并将其编号为。
> tmux send-keys -t ： 在一个窗格中发送一个命令，并将其编号为。
> tmux list-panes： 列出当前会话中所有窗格的编号。

***

## Conda命令

#### 前言
​    Conda是Anaconda中一个强大的包和环境管理工具，可以在Windows的Anaconda Prompt命令行使用，也可以在macOS或者Linux系统的终端窗口(terminal window)的命令行使用。

```
本文简单介绍conda的一些常用命令（对于大多数人来说掌握了这些就基本上能够‘生活自理’了吧）命令。当然，本文假定你已经安装了Anaconda，并且在Windows条件下使用Anaconda Prompt或者在Linux下使用terminal window。

本文根据conda-getting-started编译而成，喜欢阅读英文的伙伴们可以直接去读英文说明。

conda命令的一些选项开关有两种指定方式，一种两个连接号“--”后跟选项名全程，一种是一个连接号“-”后跟简称。比如说"-n"和"--name"是等价的。但是要注意有些例外，比如说，“--version”对应的是“-V”（大写的V而不是小写的v）。
```

#### 管理conda自身
查看conda版本
``conda --version``
查看conda的环境配置
``conda config --show``

设置镜像
        conda有时候安装软件会非常慢。设置国内镜像的话可以使	安装更快捷一些。设置方法如下所示：

```#设置清华镜像
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/conda-forge/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/bioconda/
#设置bioconda
conda config --add channels bioconda
conda config --add channels conda-forge
#设置搜索时显示通道地址
conda config --set show_channel_urls yes
```

更新conda
将conda自身更新到最新版本，it is recommended to always 	keep conda updated to the latest version.         

``conda update conda``
 更新Anaconda整体
将整个Anaconda都更新到确保稳定性和兼容性的最新版本

``conda update Anaconda``

查询某个命令的帮助 
``conda create --help``

#### 管理环境
​    Conda允许你创建相互隔离的独立环境，这些环境被称之为虚拟环境（Virtual Environment），这些环境各自包含属于自己的文件、包以及他们的依存关系，并且不会相互干扰。

        Anaconda有一个缺省的名为base的环境。但是不建议把程序放在base环境中，应该创建不同的虚拟环境分别管理不同的开发项目。这个涉及到一个根本的问题：为什么我们需要虚拟环境呢？举一个简单的例子，想象一下你有多个项目要开发，每个项目中都有一些包要依赖于某个共同的包，但是各自的所需要的版本不一致，有一些需要低版本的，有些需要高版本的。然后你就陷入了众口难调的困境。为不同的项目创建虚拟环境就可以把不同项目隔离开来，各自使用自己所需要的软件环境。


创建虚拟环境

使用conda创建虚拟环境的命令格式为:

``conda create -n env_name python=3.8``
这表示创建python版本为3.8、名字为env_name的虚拟环境。

        创建后，env_name文件可以在Anaconda安装目录envs文件下找到。在不指定python版本时，自动创建基于最新python版本的虚拟环境.      

创建虚拟环境的同时安装必要的包。
但是并不建议这样做，简化每一条命令的任务在绝大多数时候都是明智的（一个例外是需要反复执行的脚本）

``conda create -n env_name numpy matplotlib python=3.8``

查看有哪些虚拟环境
以下三条命令都可以。注意最后一个是”--”，而不是“-”.

```bash
conda env list
conda info -e
conda info --envs
```

激活虚拟环境
使用如下命令即可激活创建的虚拟环境。

``conda activate env_name``
        此时使用python --version可以检查当前python版本是否为所想要的（即虚拟环境的python版本）。

        在4.6版本以前需要使用如下命令：
    
        Linux:  source activate your_env_name
    
        Windows: activate your_env_name
    
        但是为什么要停留在过去（4.6以前的版本）呢？毕竟现在至少已经有4.10版本了，所以如果你不是最新版本，运行一下"conda update conda"吧



退出虚拟环境
        使用如下命令即可退出当前工作的虚拟环境。

```bash
conda activate
conda deactivate
```

​        有意思的是，以上两条命令只中任一条都会让你回到base environment，它们从不同的角度出发到达了同一个目的地。可以这样理解，activate的缺省值是base，deactivate的缺省值是当前环境，因此它们最终的结果都是回到base

        这个只适用于4.6及以后版本。如果你还在4.6以前的话，参见上一条说明。

删除虚拟环境
        执行以下命令可以将该指定虚拟环境及其中所安装的包都删除。

```bash
conda remove --name env_name --all
#如果只删除虚拟环境中的某个或者某些包则是：
conda remove --name env_name  package_name
```

导出环境 
很多的软件依赖特定的环境，我们可以导出环境，这样方便自己在需要时恢复环境，也可以提供给别人用于创建完全相同的环境。

```bash
#获得环境中的所有配置
conda env export --name myenv > myenv.yml
#重新还原环境
conda env create -f  myenv.yml
```

#### 包（Package）的管理
查询包的安装情况
查询看当前环境中安装了哪些包

```bash
conda list
        查询当前Anaconda repository中是否有你想要安装的包conda search package_name
        当然与互联网的连接是执行这个查询操作乃至后续安装的前提条件.
```



查询是否有安装某个包

用conda list后跟package名来查找某个指定的包是否已安装，而且支持*通配模糊查找*。

```bash
conda list pkgname        
conda list pkgname*       
```

> 当然如果你确认是否有某个包的目的是要对其进行更新的话，那就直接执行conda update pkgname即可，如果该包没有安装的话，conda会报告PackageNotInstalledError错误（然后改用conda install即可）



包的安装和更新
在当前（虚拟）环境中安装一个包：

```
conda install package_name
```

当然也可以如上所述在创建虚拟环境的同时安装包，但是并不建议。安装完一个包后可以执行conda list确认现在列表中是否已经包含了新安装的包。

```bash
#也可以以以下命令安装某个特定版本的包(以下例为安装0.20.3版本的numpy)：
conda install numpy=0.20.3
#可以用以下命令将某个包更新到它的最新版本 ：
conda update numpy
#安装包的时候可以指定从哪个channel进行安装，比如说，以下命令表示不是从缺省通道，而是从conda_forge安装某个包。
conda install pkg_name -c conda_forge
```

conda卸载包

```bash
conda uninstall package_name
#这样会将依赖于这个包的所有其它包也同时卸载。
```



```bash
#如果不想删除依赖其当前要删除的包的其他包：
conda uninstall package_name --force
```


但是并不建议用这种方式卸载，因为这样会使得你的环境支离破碎，如以下（conda manual  description原文）所述：

> ​    一个直观的理解就是，如果一个包A被删除了，而依赖于它的包B、C等却没有删除，但是那些包其实也已经不可用了。另一方面，之后你又安装了A的新版本，而不幸的是，B、C却与新版本的A不兼容因此依然是不可用的。



清理anaconda缓存

```bash
conda clean -p      # 删除没有用的包 --packages
conda clean -t      # 删除tar打包 --tarballs
conda clean -y -all # 删除所有的安装包及cache(索引缓存、锁定文件、未使用过的包和tar包)
#关于清除命令的更详细的说明，可以执行以下命令进行查询：
conda clean -h
```

> [2023-05-07] 
>
> conda就像个守财奴一样，把每个历史安装包都会好好保存。。。好处是可以很方便地恢复到旧的历史版本，坏处是占内存空间。。。前两天由于安装一个新的包，系统报告“CondaMemoryError: The conda process ran out of memory. Increase system memory and/or try again.”，执行"conda -y -all"清除了约30G的空间！



#### Python版本的管理
​    除了上面在创建虚环境时可以指定python版本外，Anaconda基环境的python版本也可以根据需要进行更改。



将版本变更到指定版本

```bash
conda install python=3.5
```

更新完后可以用以下命令查看变更是否符合预期。

```bash
python --version
```



将python版本更新到最新版本

```bash
#如果你想将python版本更新到最新版本，可以使用以下命令：
conda update python
```



#### conda install vs pip install 

**有什么区别？**
conda可以管理非python包，pip只能管理python包。
conda自己可以用来创建环境，pip不能，需要依赖virtualenv之类的。

conda安装的包是编译好的二进制文件，安装包文件过程中会自动安装依赖包；pip安装的包是wheel或源码，装过程中不会去支持python语言之外的依赖项。
conda安装的包会统一下载到一个目录文件中，当环境B需要下载的包，之前其他环境安装过，就只需要把之间下载的文件复制到环境B中，下载一次多次安装。pip是直接下载到对应环境中。

conda只能在conda管理的环境中使用，例如比如conda所创建的虚环境中使用。pip可以在任何环境中使用，在conda创建的环境 中使用pip命令，需要先安装pip（conda install pip ），然后可以 环境A 中使用pip 。conda 安装的包，pip可以卸载，但不能卸载依赖包，pip安装的包，只能用pip卸载。

pip和conda在安装软件包时，在依赖关系方面的处理机制不同。pip在递归的串行循环中安装依赖项，不会确保同时满足所有软件包的依赖关系，如果按顺序较早安装的软件包相对于按顺序较晚安装的软件包具有不兼容的依赖项版本，则可能导致环境以微妙的方式被破坏掉；conda使用SAT（satisfiability）solver来验证是否满足环境中安装的所有软件包的所有要求，只要有关依赖项的软件包元数据正确，conda就会按预期产生可用的环境。



**能否混用？**

首先，不建议混用。混用容易导致库的依赖关系出现混乱，然后突然哪天环境可能就崩了，安装不了新的包，无法进行conda update之类的。[2023-05-07]刚刚这两天遭遇了一次这样的事件，由于要安装一个新的包，各种各样的稀奇古怪的事情层出不穷，比如说：

>> conda install packagename....
>>
>> CondaMemoryError: The conda process ran out of memory. Increase system memory and/or try again.
>>
>> conda update conda

>- defaults/win-64::_anaconda_depends==2020.07=py38_0
>
>- defaults/win-64::_ipyw_jlab_nb_ext_conf==0.1.0=py38_0
>  failed with repodata from current_repodata.json, will retry with next repodata source.
>   Solving environment: failed with repodata from current_repodata.json, will retry with next repodata
>   source.
>   Collecting package metadata (repodata.json): failed
>
>  RemoveError: 'requests' is a dependency of conda and cannot be removed from
>  conda's operating environment. 



上天入地各种官方民间偏方的试，搞不定，最后只好卸载重新安装Anaconda完事。。。

其次，由于conda的库确实不如pip的库丰富{很多包只在 pip 有：PYPI有15万可用包，而Anaconda repository中（使用conda命令安装）提供了1,500多个软件包，Anaconda cloud上（使用conda-forge或bioconda命令安装）的几千种其他软件包。}，所以有时候可能迫不得已要使用pip安装。切记，只有在conda install搞不定时才使用pip intall。 而且，最后使用虚拟环境进行环境隔离。



**安装在哪里？**

conda install xxx：这种方式安装的库都会放在anaconda3/pkgs目录下，这样的好处就是，当在某个环境下已经下载好了某个库，再在另一个环境中还需要这个库时，就可以直接从pkgs目录下将该库复制至新环境而不用重复下载。

pip install xxx：分两种情况，一种情况就是当前conda环境的python是conda安装的，和系统的不一样，那么xxx会被安装到anaconda3/envs/current_env/lib/python3.x/site-packages文件夹中，如果当前conda环境用的是系统的python，那么xxx会通常会被安装到~/.local/lib/python3.x/site-packages文件夹中。

**如何判断conda中某个包是通过conda还是pip安装的？**
执行 conda list ，用pip安装的包显示的build项目为pypi。

#### conda configuration

> conda的配置文件为".condarc"，该文件在安装时不是缺省存在的。但是当你第一次运行conda config命令时它就被自动创建了。".condarc"配置文件遵循简单的YAML语法。



#### condarc文件在哪儿？ 

> 执行conda info，会有信息显示。



#### Channel管理

```bash
#追加conda-forge channel:
conda config --add channels conda-forge

#移除conda-forge channel:
conda config --remove channels conda-forge

#查询当前配置中包含哪些channels
conda config --get channels

```

#### conda指令执行技巧
在指令后输入-y或者--yes可以制动确认指令，避免后期再次输入y确认，例如：

```bash
pip create --name demo python=3.8 --yes  # 自动创建python环境demo，并指定python版本为3.8
pip install numpy pandas matplotlib -y  # 自动安装numpy、pandas和matplotlib软件包
```





***

## ROS2

### 核心概念

#### Workspace：开发过程的大本营

ROS系统中一个典型的工作空间结构如图所示，这个dev_ws就是工作空间的根目录，里边会有四个子目录，或者叫做四个子空间。

![image-20220524111415729](https://book.guyuehome.com/ROS2/2.%E6%A0%B8%E5%BF%83%E6%A6%82%E5%BF%B5/image/2.1_%E5%B7%A5%E4%BD%9C%E7%A9%BA%E9%97%B4/image-20220524111415729.png)

- **src，代码空间**，未来编写的代码、脚本，都需要人为的放置到这里；
- **build，编译空间**，保存编译过程中产生的中间文件；
- **install，安装空间**，放置编译得到的可执行文件和脚本；
- **log，日志空间**，编译和运行过程中，保存各种警告、错误、信息等日志。

总体来讲，这四个空间的文件夹，我们绝大部分操作都是在src中进行的，编译成功后，就会执行install里边的结果，build和log两个文件夹用的很少。

##### **自动安装依赖**

我们从社区中下载的各种代码，多少都会有一些依赖，我们可以手动一个一个安装，也可以使用rosdep工具自动安装：

```bash
sudo apt install -y python3-pip
sudo pip3 install rosdepc
sudo rosdepc init
rosdepc update
cd ..                                                      #回到的是包含src的文件夹
rosdepc install -i --from-path src --rosdistro humble -y
```

##### **编译工作空间**

依赖安装完成后，就可以使用如下命令编译工作空间啦，如果有缺少的依赖，或者代码有错误，编译过程中会有报错，否则编译过程应该不会出现任何错误：

```bash
sudo apt install python3-colcon-ros
cd ~/dev_ws/   												#回到的是包含src的文件夹
colcon build
```

##### **设置环境变量**

编译成功后，为了让系统能够找到我们的功能包和可执行文件，还需要设置环境变量：

```bash
source install/local_setup.sh # 仅在当前终端生效
echo " source ~/dev_ws/install/local_setup.sh" >> ~/.bashrc # 所有终端均生效
```



#### Package：功能包，功能源码的聚集地

###### 创建功能包

如何在ROS2中创建一个功能包呢？我们可以使用这个指令：

```bash
ros2 pkg create --build-type <build-type> <package_name>
```

ros2命令中：

- **pkg**：表示功能包相关的功能；
- **create**：表示创建功能包；
- **build-type**：表示新创建的功能包是C++还是Python的，如果使用C++或者C，那这里就跟ament_cmake，如果使用Python，就跟ament_python；
- **package_name**：新建功能包的名字。

比如在终端中分别创建C++和Python版本的功能包：

```bash
cd ~/dev_ws/src
ros2 pkg create --build-type ament_cmake learning_pkg_c               # C++
ros2 pkg create --build-type ament_python learning_pkg_python 		   # Python
```

###### 编译功能包

在创建好的功能包中，我们可以继续完成代码的编写，之后需要编译和配置环境变量，才能正常运行：

```bash
cd ~/dev_ws    #返回Workspace
colcon build   # 编译工作空间所有功能包
$ source install/local_setup.sh
```

###### 功能包结构

C++类型的功能包：其中必然存在两个文件：**package.xml**和**CMakerLists.txt**

Python功能包：C++功能包需要将源码编译成可执行文件，但是Python语言是解析型的，不需要编译，所以会有一些不同，但也会有这两个文件：**package.xml**和**setup.py**。

#### Node：机器人的工作细胞

###### 创建节点流程

总体而言，节点的实现方式是这四个步骤：

- 编程接口初始化
- 创建节点并初始化
- 实现节点功能
- 销毁节点并关闭接口

###### 节点命令行操作

节点命令的常用操作如下：

```bash
ros2 node list               # 查看节点列表
ros2 node info <node_name>   # 查看节点信息
```



#### Topic：节点之间传递数据的桥梁

从话题本身的实现角度来看，使用了基于DDS的**发布/订阅模型**。

话题数据传输的特性是从一个节点到另外一个节点，发送数据的对象称之为**发布者**，接收数据的对象称之为**订阅者**，每一个话题都需要有一个名字，传输的数据也需要有固定的数据类型。

因为话题是**多对多的模型**，发布控制指令的摇杆可以有一个，也可以有2个、3个，订阅控制指令的机器人可以有1个，也可以有2个、3个，大家可以想象一下这个画面，似乎还是挺魔性的，如果存在多个发送指令的节点，建议大家要**注意区分优先级**，不然机器人可能不知道该听谁的了。

话题通信还有一个特性，那就是**异步**。异步的特性也让话题更适合用于一些周期发布的数据，比如传感器的数据，运动控制的指令等等，如果某些逻辑性较强的指令，比如修改某一个参数，用话题传输就不太合适了。

**消息是ROS中的一种接口定义方式**，与编程语言无关，我们也可以通过**.msg**后缀的文件自行定义，有了这样的接口，各种节点就像积木块一样，通过各种各样的接口进行拼接，组成复杂的机器人系统。

##### Publisher发布者流程总结

对以上程序进行分析，如果我们想要实现一个发布者，流程如下：

- 编程接口初始化
- 创建节点并初始化
- 创建发布者对象
- 创建并填充话题消息
- 发布话题消息
- 销毁节点并关闭接口

##### Subscriber订阅者流程总结

对以上程序进行分析，如果我们想要实现一个订阅者，流程如下：

- 编程接口初始化
- 创建节点并初始化
- 创建订阅者对象
- 回调函数处理话题数据
- 销毁节点并关闭接口

#### Service：节点之间的你问我答

##### **客户端/服务器模型**

从服务的实现机制上来看，这种你问我答的形式叫做**客户端/服务器模型**，简称为CS模型，客户端在需要某些数据的时候，针对某个具体的服务，发送请求信息，服务器端收到请求之后，就会进行处理并反馈应答信息。

##### **服务接口**

和话题通信类似，服务通信的核心还是要传递数据，数据变成了两个部分，一个**请求的数据**，比如请求苹果位置的命令，还有一个**反馈的数据**，比如反馈苹果坐标位置的数据，这些数据和话题消息一样，在ROS中也是要标准定义的，话题使用.msg文件定义，服务使用的是.srv文件定义。

##### **流程总结**

如果我们想要实现一个服务端，流程如下：

- 编程接口初始化
- 创建节点并初始化
- 创建服务器端对象
- 通过回调函数处进行服务
- 向客户端反馈应答结果
- 销毁节点并关闭接口

话题和服务是ROS中最为常用的两种数据通信方法，前者适合传感器、控制指令等周期性、单向传输的数据，后者适合一问一答，同步性要求更高的数据，比如获取机器视觉识别到的目标位置。

#### Interface：数据传递的标准结构

##### **ROS通信接口**

接口可以让程序之间的依赖降低，便于我们使用别人的代码，也方便别人使用我们的代码。ROS有三种常用的通信机制，分别是**话题、服务、动作**，通过每一种通信种定义的接口，各种节点才能有机的联系到一起。

##### **语言无关**

为了保证每一个节点可以使用不同语言编程，ROS将这些接口的设计做成了和**语言无关**的

#### Parameter：机器人系统的全局字典

##### **全局字典**

在ROS系统中，参数是以**全局字典**的形态存在的，什么叫字典？就像真实的字典一样，由名称和数值组成，也叫做键和值，合成**键值**。或者我们也可以理解为，就像编程中的参数一样，有一个参数名 ，然后跟一个等号，后边就是参数值了，在使用的时候，访问这个参数名即可。

##### **可动态监控**

在ROS2中，参数的特性非常丰富，比如某一个节点共享了一个参数，其他节点都可以访问，如果某一个节点对参数进行了修改，其他节点也有办法立刻知道，从而获取最新的数值。这在**参数的高级编程**中，大家都可能会用到。

#### Action：完整行为的流程管理

目的就是便于**对机器人某一完整行为的流程进行管理**。动作是一种应用层的通信机制，其底层就是基于话题和服务来实现的。

##### **客户端/服务器模型**

动作和服务类似，使用的也是客户端和服务器模型，客户端发送动作的目标，想让机器人干什么，服务器端执行动作过程， 控制机器人达到运动的目标，同时周期反馈动作执行过

##### **一对多通信**

和服务一样，动作通信中的客户端可以有多个，大家都可以发送运动命令，但是服务器端只能有一个，毕竟只有一个机器人，先执行完成一个动作，才能执行下一个动作。

##### **同步通信**

既然有反馈，那动作也是一种同步通信机制，之前我们也介绍过，动作过程中的数据通信接口，使用.action文件进行定义。程中的状态。

#### DDS(Data Distribution Service)：机器人的神经网络

##### **通信模型**

DDS的核心是通信，能够实现通信的模型和软件框架非常多，这里我们列出常用的四种模型。

![image-20220528020740057](https://book.guyuehome.com/ROS2/2.%E6%A0%B8%E5%BF%83%E6%A6%82%E5%BF%B5/image/2.10_DDS/image-20220528020740057.jpg)

- 第一种，**点对点模型**，许多客户端连接到一个服务端，每次通信时，通信双方必须建立一条连接。当通信节点增多时，连接数也会增多。而且每个客户端都需要知道服务器的具体地址和所提供的服务，一旦服务器地址发生变化，所有客户端都会受到影响。
- 第二种，**Broker模型**，针对点对点模型进行了优化，由Broker集中处理所有人的请求，并进一步找到真正能响应该服务的角色。这样客户端就不用关心服务器的具体地址了。不过问题也很明显，Broker作为核心，它的处理速度会影响所有节点的效率，当系统规模增长到一定程度，Broker就会成为整个系统的性能瓶颈。更麻烦是，如果Broker发生异常，可能导致整个系统都无法正常运转。之前的ROS1系统，使用的就是类似这样的架构。
- 第三种，**广播模型**，所有节点都可以在通道上广播消息，并且节点都可以收到消息。这个模型解决了服务器地址的问题，而且通信双方也不用单独建立连接，但是广播通道上的消息太多了，所有节点都必须关心每条消息，其实很多是和自己没有关系的。
- 第四种，就是**以数据为中心的DDS模型**了，这种模型与广播模型有些类似，所有节点都可以在DataBus上发布和订阅消息。但它的先进之处在于，通信中包含了很多并行的通路，每个节点可以只关心自己感兴趣的消息，忽略不感兴趣的消息，有点像是一个旋转火锅，各种好吃的都在这个DataBus传送，我们只需要拿自己想吃的就行，其他的和我们没有关系。

可见，在这几种通信模型中，DDS的优势更加明显。

##### **什么是DDS**

好啦，说了半天DDS，到底啥意思呢？我们来做一个完整的介绍

DDS的全称是**Data Distribution Service**，也就是**数据分发服务**，2004年由**对象管理组织OMG**发布和维护，是一套专门为**实时系统**设计的**数据分发/订阅标准**，最早应用于美国海军， 解决舰船复杂网络环境中大量软件升级的兼容性问题，现在已经成为强制标准。

DDS强调**以数据为中心**，可以提供丰富的**服务质量策略**，以保障数据进行实时、高效、灵活地分发，可满足各种分布式实时通信应用需求。

这里也提一下对象管理组织OMG，成立于1989年，它的使命是开发技术标准，为数以千计的垂直行业提供真实的价值，比如大家课可能听说过的统一建模语言SYSML和UML，还有中间件标准CORBA等，当然还有DDS。

##### **DDS在ROS2中的应用**

DDS在ROS2系统中的位置至关重要，所有上层建设都建立在DDS之上。在这个ROS2的架构图中，蓝色和红色部分就是DDS。

![image-20220528020937717](https://book.guyuehome.com/ROS2/2.%E6%A0%B8%E5%BF%83%E6%A6%82%E5%BF%B5/image/2.10_DDS/image-20220528020937717.jpg)

刚才我们也提到，DDS是一种通信的标准，就像4G、5G一样，既然是标准，那大家都可以按照这个标准来实现对应的功能，所以华为、高通都有很多5G的技术专利，DDS也是一样，**能够按照DDS标准实现的通信系统很多**，这里每一个红色模块，就是某一企业或组织实现的一种DDS系统。

既然可选用的DDS这么多，那我们该用哪一个呢？具体而言，他们肯定都符合基本标准，但还是会有性能上的差别，ROS2的原则就是尽量兼容，让用户根据使用场景选择，比如个人开发，我们选择一个开源版本的DDS就行，如果是工业应用，那可能得选择一个商业授权的版本了。

为了实现对多个DDS的兼容，ROS设计了一个**Middleware中间件**，也就是一个统一的标准，不管我们用那个DDS，保证上层编程使用的函数接口都是一样的。此时兼容性的问题就转移给了DDS厂商，如果他们想让自己的DDS系统进入ROS生态，就得按照ROS的接口标准，开发一个驱动，也就是这个部分。

无论如何，ROS的宗旨不变，要提高软件代码的复用性，下边DDS任你边，上边的软件没影响。

![image-20220528020948738](https://book.guyuehome.com/ROS2/2.%E6%A0%B8%E5%BF%83%E6%A6%82%E5%BF%B5/image/2.10_DDS/image-20220528020948738.jpg)

在ROS的四大组成部分中，由于DDS的加入，大大提高了分布式通信系统的综合能力，这样我们在开发机器人的过程中，就不需要纠结通信的问题，可以把更多时间放在其他部分的应用开发上。

##### **质量服务策略QoS**

DDS为ROS的通信系统提供提供了哪些特性呢？我们通过这个通信模型图来看下。

![image-20220528021108329](https://book.guyuehome.com/ROS2/2.%E6%A0%B8%E5%BF%83%E6%A6%82%E5%BF%B5/image/2.10_DDS/image-20220528021108329.jpg)

DDS中的基本结构是**Domain**，Domain将各个应用程序绑定在一起进行通信，回忆下之前我们配置树莓派和电脑通信的时候，配置的那个DOMAIN ID，就是对全局数据空间的分组定义，只有处于同一个DOMAIN小组中的节点才能互相通信。这样可以避免无用数据占用的资源。

DDS中另外一个重要特性就是**质量服务策略，QoS**。

QoS是一种网络传输策略，应用程序指定所需要的网络传输质量行为，QoS服务实现这种行为要求，尽可能地满足客户对通信质量的需求，可以理解为**数据提供者和接收者之间的合约**。

![image-20220528021119863](https://book.guyuehome.com/ROS2/2.%E6%A0%B8%E5%BF%83%E6%A6%82%E5%BF%B5/image/2.10_DDS/image-20220528021119863.jpg)

具体会有哪些策略？比如：

- **DEADLINE**策略，表示通信数据必须要在每次截止时间内完成一次通信；
- **HISTORY**策略，表示针对历史数据的一个缓存大小；
- **RELIABILITY**策略，表示数据通信的模式，配置成BEST_EFFORT，就是尽力传输模式，网络情况不好的时候，也要保证数据流畅，此时可能会导致数据丢失，配置成RELIABLE，就是可信赖模式，可以在通信中尽量保证图像的完整性，我们可以根据应用功能场景选择合适的通信模式；
- **DURABILITY**策略，可以配置针对晚加入的节点，也保证有一定的历史数据发送过去，可以让新节点快速适应系统。

![image-20220528021133020](https://book.guyuehome.com/ROS2/2.%E6%A0%B8%E5%BF%83%E6%A6%82%E5%BF%B5/image/2.10_DDS/image-20220528021133020.jpg)

所有这些策略在ROS系统中都可以通过类似这样的结构体配置，如果不配置的话，系统也会使用默认的参数。

#### Distributed Communication**分布式通信**

##### 什么叫分布式？

之前我们也讲过，在ROS系统中，机器人功能是由各种节点组成的，这些节点可能位于不同的计算机中，这种结构可以将原本资源消耗较多的任务，分配到不同的平台上，减轻计算压力，这就是分布式通信框架的典型应用之一。

### 常用工具

#### Launch：多节点启动与配置脚本

一种可以一次性启动所有节点的方式，**Launch启动文件**，它是ROS系统中多节点启动与配置的一种脚本。**ROS2中的Launch文件就是基于Python描述的**。

Launch的核心目的是**启动节点**，我们在命令行中输入的各种参数，在Launch文件中，通过类似这样的很多代码模版，也可以进行配置，甚至还可以使用Python原有的编程功能，大大丰富了启动过程中的多样化配置。

##### **Launch文件包含**

在复杂的机器人系统中，launch文件也会有很多，此时我们可以使用类似编程中的include机制，让launch文件互相包含。

#### **TF：机器人坐标系管理神器**

##### 机器人中的坐标系

比如在机械臂形态的机器人中，机器人安装的位置叫做**基坐标系**Base Frame，机器人安装位置在外部环境下的参考系叫做**世界坐标系**World Frame，机器人末端夹爪的位置叫做**工具坐标系**，外部被操作物体的位置叫做**工件坐标系**，在机械臂抓取外部物体的过程中，这些坐标系之间的关系也在跟随变化。

在移动机器人系统中，坐标系一样至关重要，比如一个移动机器人的中心点是**基坐标系**Base Link，雷达所在的位置叫做**雷达坐标系**laser link，机器人要移动，里程计会累积位置，这个位置的参考系叫做**里程计坐标系**odom，里程计又会有累积误差和漂移，绝对位置的参考系叫做**地图坐标系**map。

关于坐标系变换关系的基本理论，在每一本机器人学的教材中都会有讲解，可以分解为**平移和旋转**两个部分，通过一个四乘四的矩阵进行描述，在空间中画出坐标系，那两者之间的变换关系，其实就是向量的数学描述。

##### **查看TF树**

在当前运行的两只海龟中，有哪些坐标系呢，我们可以通过这个小工具来做查看。

```bash
ros2 run tf2_tools view_frames 
```

默认在当前终端路径下生成了一个frames.pdf文件，打开之后，就可以看到系统中各个坐标系的关系了。

##### **查询坐标变换信息**

只看到坐标系的结构还不行，如果我们想要知道某两个坐标系之间的具体关系，可以通过tf2_echo这个工具查看：

```bash
ros2 run tf2_ros tf2_echo turtle2 turtle1
```

运行成功后，终端中就会循环打印坐标系的变换数值了，由平移和旋转两个部分组成，还有旋转矩阵。

##### **静态TF广播**

坐标变换中最为简单的应该是相对位置不发生变化的情况，比如你家的房子在哪个位置，只要房子不拆，这个坐标应该就不会变化。在机器人系统中也很常见，比如激光雷达和机器人底盘之间的位置关系，安装好之后基本不会变化。

在TF中，这种情况也称之为**静态TF变换**.

#### **URDF：机器人建模方法**

ROS专门提供了一种机器人建模方法——**URDF**，用来描述机器人外观、性能等各方面属性。

##### **机器人的组成**

建模描述机器人的过程中，我们自己需要先熟悉机器人的组成和参数，比如机器人一般是由**硬件结构、驱动系统、传感器系统、控制系统**四大部分组成，市面上一些常见的机器人，无论是移动机器人还是机械臂，我们都可以按照这四大组成部分进行分解。

- 硬件结构就是底盘、外壳、电机等实打实可以看到的设备；
- 驱动系统就是可以驱使这些设备正常使用的装置，比如电机的驱动器，电源管理系统等；
- 传感系统包括电机上的编码器、板载的IMU、安装的摄像头、雷达等等，便于机器人感知自己的状态和外部的环境；
- 控制系统就是我们开发过程的主要载体了，一般是树莓派、电脑等计算平台，以及里边的操作系统和应用软件。

机器人建模的过程，其实就是按照类似的思路，通过建模语言，把机器人每一个部分都描述清楚，再组合起来的过程。

#### **URDF**

ROS中的建模方法叫做**URDF**，全称是**统一机器人描述格式**，不仅可以清晰描述机器人自身的模型，还可以描述机器人的外部环境。

![image-20220528144424329](https://book.guyuehome.com/ROS2/3.%E5%B8%B8%E7%94%A8%E5%B7%A5%E5%85%B7/image/3.3_URDF/image-20220528144424329.png)

URDF模型文件使用的是**XML格式**，右侧就是一个机器人的URDF描述，乍看上去，有点像网页开发的源代码，都是由一系列尖括号包围的标签和其中的属性组合而成。

如何使用这样一个文件描述机器人呢？比如机械臂，大家可以看下自己的手臂，我们的手臂是由大臂和小臂组成，他们独自是无法运动的，必须通过一个手肘关节连接之后，才能通过肌肉驱动，产生相对运动。

在建模中，大臂和小臂就类似机器人的这些独立的刚体部分，称为**连杆Link**，手肘就类似于机器人电机驱动部分，称为**关节joint**。

所以在URDF建模过程中，关键任务就是通过这里的<link>和<joint>，理清楚每一个连杆和关节的描述信息。

##### **连杆Link的描述**

<link>标签用来描述机器人某个刚体部分的**外观和物理属性**，外观包括尺寸、颜色、形状，物理属性包括质量、惯性矩阵、碰撞参数等。

![image-20220528144534685](https://book.guyuehome.com/ROS2/3.%E5%B8%B8%E7%94%A8%E5%B7%A5%E5%85%B7/image/3.3_URDF/image-20220528144534685.png)

以这个机械臂连杆为例，它的link描述如下：

![image-20220528144549092](https://book.guyuehome.com/ROS2/3.%E5%B8%B8%E7%94%A8%E5%B7%A5%E5%85%B7/image/3.3_URDF/image-20220528144549092.png)

link标签中的name表示该连杆的名称，我们可以自定义，未来joint连接link的时候，会使用到这个名称。

link里边的<visual>部分用来描述机器人的外观，比如：

- <geometry>表示**几何形状**，里边使用<mesh>调用了一个在三维软件中提前设计好的蓝色外观，就是这个stl文件，看上去和真实机器人是一致的
- <origin>表示**坐标系相对初始位置的偏移**，分别是x、y、z方向上的平移，和roll、pitch、raw旋转，不需要偏移的话，就全为0。

第二个部分<collision>，描述**碰撞参数**，里边的内容似乎和<visual>一样，也有<geometry>和<origin>，看似相同，其实区别还是比较大的。

- <visual>部分重在描述机器人看上去的状态，也就是视觉效果；
- <collision>部分则是描述机器人运动过程中的状态，比如机器人与外界如何接触算作碰撞。

在这个机器人模型中，蓝色部分是通过<visual>来描述的，在实际控制过程中，这样复杂的外观在计算碰撞检测时，要求的算力较高，为了简化计算，我们将碰撞检测用的模型简化为了绿色框的圆柱体，也就是<collision>里边<geometry>描述的形状。<origin>坐标系偏移也是类似，可以描述刚体质心的偏移。

![image-20220528144603646](https://book.guyuehome.com/ROS2/3.%E5%B8%B8%E7%94%A8%E5%B7%A5%E5%85%B7/image/3.3_URDF/image-20220528144603646.png)

如果是移动机器人的话，link也可以用来描述小车的车体、轮子等部分。

##### **关节Joint描述**

机器人模型中的刚体最终要通过关节joint连接之后，才能产生相对运动。

URDF中的关节有六种运动类型。

![image-20220528144655899](https://book.guyuehome.com/ROS2/3.%E5%B8%B8%E7%94%A8%E5%B7%A5%E5%85%B7/image/3.3_URDF/image-20220528144655899.png)

1. continuous，描述旋转运动，可以围绕某一个轴无限旋转，比如小车的轮子，就属于这种类型。
2. revolute，也是旋转关节，和continuous类型的区别在于不能无限旋转，而是带有角度限制，比如机械臂的两个连杆，就属于这种运动。
3. prismatic，是滑动关节，可以沿某一个轴平移，也带有位置的极限，一般直线电机就是这种运动方式。
4. fixed，固定关节，是唯一一种不允许运动的关节，不过使用还是比较频繁的，比如相机这个连杆，安装在机器人上，相对位置是不会变化的，此时使用的连接方式就是Fixed。
5. Floating是浮动关节，第六种planar是平面关节，这两种使用相对较少。

![image-20220528144722751](https://book.guyuehome.com/ROS2/3.%E5%B8%B8%E7%94%A8%E5%B7%A5%E5%85%B7/image/3.3_URDF/image-20220528144722751.png)

在URDF模型中，每一个link都使用这样一段xml内容描述，比如关节的名字叫什么，运动类型是哪一种。

![image-20220528144729633](https://book.guyuehome.com/ROS2/3.%E5%B8%B8%E7%94%A8%E5%B7%A5%E5%85%B7/image/3.3_URDF/image-20220528144729633-16537204524521.png)

- parent标签：描述父连杆；
- child标签：描述子连杆，子连杆会相对父连杆发生运动；
- origin：表示两个连杆坐标系之间的关系，也就是图中红色的向量，可以理解为这两个连杆该如何安装到一起；
- axis表示关节运动轴的单位向量，比如z等于1，就表示这个旋转运动是围绕z轴的正方向进行的；
- limit就表示运动的一些限制了，比如最小位置，最大位置，和最大速度等。

<details class="info" open="open" style="box-sizing: inherit; background-color: var(--md-admonition-bg-color); border: 0.075rem solid rgb(0, 184, 212); border-radius: 0.2rem; box-shadow: var(--md-shadow-z1); color: rgba(0, 0, 0, 0.87); display: flow-root; font-size: 0.64rem; margin: 1.5625em 0px; padding: 0px 0.6rem; break-inside: avoid; transition: box-shadow 125ms; overflow: visible; font-family: Roboto, -apple-system, BlinkMacSystemFont, Helvetica, Arial, sans-serif; font-style: normal; font-variant-ligatures: normal; font-variant-caps: normal; font-weight: 400; letter-spacing: normal; orphans: 2; text-align: start; text-indent: 0px; text-transform: none; widows: 2; word-spacing: 0px; -webkit-text-stroke-width: 0px; white-space: normal; text-decoration-thickness: initial; text-decoration-style: initial; text-decoration-color: initial;"><summary class="" style="box-sizing: border-box; background-color: rgba(0, 184, 212, 0.1); border-top: none; border-right: none; border-bottom: none; border-left: 0.2rem none; border-image: initial; font-weight: 700; margin: 0px -0.6rem; padding: 0.4rem 1.8rem 0.4rem 2rem; position: relative; cursor: pointer; display: block; min-height: 1rem; overflow: hidden; border-top-left-radius: 0.1rem; border-top-right-radius: 0.1rem; -webkit-tap-highlight-color: transparent; outline: none;">Info</summary><p style="box-sizing: border-box; margin-bottom: 0.6rem;">ROS中关于平移的默认单位是m，旋转是弧度（不是度），所以这里的3.14就表示可以在-180度到180度之间运动，线速度是m/s，角速度是rad/s。</p></details>

##### **完整机器人模型**

![image-20220528144900705](https://book.guyuehome.com/ROS2/3.%E5%B8%B8%E7%94%A8%E5%B7%A5%E5%85%B7/image/3.3_URDF/image-20220528144900705.png)

最终所有的link和joint标签完成了对机器人每个部分的描述和组合，全都放在一个robot标签中，就形成了完整的机器人模型。

![image-20220528144824234](https://book.guyuehome.com/ROS2/3.%E5%B8%B8%E7%94%A8%E5%B7%A5%E5%85%B7/image/3.3_URDF/image-20220528144824234.png)

所以大家在看某一个URDF模型时，先不着急看每一块代码的细节，先来找link和joint，看下这个机器人是由哪些部分组成的，了解完全局之后，再看细节。

#### **Gazebo：三维物理仿真平台**

##### **介绍**

Gazebo是ROS系统中最为常用的**三维物理仿真平台**，支持动力学引擎，可以实现高质量的图形渲染，不仅可以模拟机器人及周边环境，还可以加入摩擦力、弹性系数等物理属性。

![image-20220528145639277](https://book.guyuehome.com/ROS2/3.%E5%B8%B8%E7%94%A8%E5%B7%A5%E5%85%B7/image/3.4_Gazebo/image-20220528145639277.png)

比如我们要开发一个火星车，那就可以在Gazebo中模拟火星表面的环境，再比如我们做无人机，续航和限飞都导致我们没有办法频繁用实物做实验，此时不妨使用Gazebo先做仿真，等算法开发的差不多了，再部署到实物上来运行。

所以类似Gazebo这样的仿真平台，可以帮助我们验证机器人算法、优化机器人设计、测试机器人场景应用，为机器人开发提供更多可能。

##### **安装**

Gazebo如何使用呢？我们不妨先把它给跑起来，互相认识一下。

为了确保系统中已经完整安装了Gazebo相关的功能包，大家可以通过这样一个命令，简单直接的把和gazebo相关的包都给装上：

```bash
sudo apt install ros-humble-gazebo-*
```

##### **运行**

通过这句命令就可以启动啦：

```bash
ros2 launch gazebo_ros gazebo.launch.py
```

![image-20220528145818827](https://book.guyuehome.com/ROS2/3.%E5%B8%B8%E7%94%A8%E5%B7%A5%E5%85%B7/image/3.4_Gazebo/image-20220528145818827.png)

<details class="attention" open="open" style="box-sizing: inherit; background-color: var(--md-admonition-bg-color); border: 0.075rem solid rgb(68, 138, 255); border-radius: 0.2rem; box-shadow: var(--md-shadow-z1); color: rgba(0, 0, 0, 0.87); display: flow-root; font-size: 0.64rem; margin: 1.5625em 0px; padding: 0px 0.6rem; break-inside: avoid; transition: box-shadow 125ms; overflow: visible; font-family: Roboto, -apple-system, BlinkMacSystemFont, Helvetica, Arial, sans-serif; font-style: normal; font-variant-ligatures: normal; font-variant-caps: normal; font-weight: 400; letter-spacing: normal; orphans: 2; text-align: start; text-indent: 0px; text-transform: none; widows: 2; word-spacing: 0px; -webkit-text-stroke-width: 0px; white-space: normal; text-decoration-thickness: initial; text-decoration-style: initial; text-decoration-color: initial;"><summary style="box-sizing: border-box; background-color: rgba(68, 138, 255, 0.1); border-top: none; border-right: none; border-bottom: none; border-left: 0.2rem none; border-image: initial; font-weight: 700; margin: 0px -0.6rem; padding: 0.4rem 1.8rem 0.4rem 2rem; position: relative; cursor: pointer; display: block; min-height: 1rem; overflow: hidden; border-top-left-radius: 0.1rem; border-top-right-radius: 0.1rem; -webkit-tap-highlight-color: transparent; outline: none;">Attention</summary><p style="box-sizing: border-box; margin-bottom: 0.6rem;">为保证模型顺利加载，请将离线模型下载并放置到~/.gazebo/models路径下</p></details>

，下载链接如下：https://github.com/osrf/gazebo_models

认识了Gazebo，接下来是不是该试试机器人仿真啦？

大家还记得之前课程中，我们设计的移动机器人模型么？我们一起尝试把它放到Gazebo中，还要控制它在仿真环境中运动。

##### **XACRO机器人模型优化**

我们之前设计好的URDF模型此时还不能直接放到Gazebo中，需要我们做一些优化。这里给大家介绍一个URDF文件格式的升级版本——**XACRO文件**。

同样也是对机器人URDF模型的创建，XACRO文件加入了更多编程化的实现方法，可以让模型创建更友好。

![image-20220528145940535](https://book.guyuehome.com/ROS2/3.%E5%B8%B8%E7%94%A8%E5%B7%A5%E5%85%B7/image/3.4_Gazebo/image-20220528145940535.png)

比如：

- **宏定义**，一个小车有4个轮子，每个轮子都一样，我们就没必要创建4个一样的link，像函数定义一样，做一个可重复使用的模块就可以了。
- **文件包含**，复杂机器人的模型文件可能会很长，为了切分不同的模块，比如底盘、传感器，我们还可以把不同模块的模型放置在不同的文件中，然后再用一个总体文件做包含调用。
- **可编程接口**，比如在XACRO模型文件中，定义一些常量，描述机器人的尺寸，定义一些变量，在调用宏定义的时候传递数据，还可以在模型中做数据计算，甚至加入条件语句，比如你的机器人叫A，就有摄像头，如果叫B，就没有摄像头。

XACRO建模过程就像写代码一样，功能更为丰富了。

接下来，我们就通过XACRO文件对移动机器人的模型做一下优化，大家先要使用这句命令安装必要的功能包。

```
$ sudo apt install ros-humble-xacro
```

以下是一些常用的XACRO文件语法，大家了解下。

###### **常量定义**

![image-20220528150321426](https://book.guyuehome.com/ROS2/3.%E5%B8%B8%E7%94%A8%E5%B7%A5%E5%85%B7/image/3.4_Gazebo/image-20220528150321426.png)

<xacro:property>标签用来定义一些常量，比如这样定义一个PI的常量名为“M_PI”，值为“3.14159”，在调用的时候，通过$加大括号，里边就可以使用定义好的常量了。

![image-20220528150331042](https://book.guyuehome.com/ROS2/3.%E5%B8%B8%E7%94%A8%E5%B7%A5%E5%85%B7/image/3.4_Gazebo/image-20220528150331042.png)

针对原本移动机器人的URDF文件，我们就可以把底盘的质量、尺寸，轮子的质量、尺寸、安装位置，这些不会变化的数据，都通过常量定义，未来需要修改的时候也很方便，就不需要在模型文件中一行一行找了。

![image-20220528150338969](https://book.guyuehome.com/ROS2/3.%E5%B8%B8%E7%94%A8%E5%B7%A5%E5%85%B7/image/3.4_Gazebo/image-20220528150338969.png)

###### **数学计算**

![image-20220528150430205](https://book.guyuehome.com/ROS2/3.%E5%B8%B8%E7%94%A8%E5%B7%A5%E5%85%B7/image/3.4_Gazebo/image-20220528150430205.png)

如果需要做数学计算，同样是在“${}”中进行，比如某一个位置，我们可以通过这两个常量做运算得到，就加入了加法和除法运算。

![image-20220528150435206](https://book.guyuehome.com/ROS2/3.%E5%B8%B8%E7%94%A8%E5%B7%A5%E5%85%B7/image/3.4_Gazebo/image-20220528150435206.png)

在移动机器人的模型中，很多有相对关系的数据，我们尽量都改成公式计算，如果直接写结果的数值，未来修改的时候，可能根本想不起来这个数据是怎么来的。

<details class="info" open="open" style="box-sizing: inherit; background-color: var(--md-admonition-bg-color); border: 0.075rem solid rgb(0, 184, 212); border-radius: 0.2rem; box-shadow: var(--md-shadow-z1); color: rgba(0, 0, 0, 0.87); display: flow-root; font-size: 0.64rem; margin: 1.5625em 0px; padding: 0px 0.6rem; break-inside: avoid; transition: box-shadow 125ms; overflow: visible; font-family: Roboto, -apple-system, BlinkMacSystemFont, Helvetica, Arial, sans-serif; font-style: normal; font-variant-ligatures: normal; font-variant-caps: normal; font-weight: 400; letter-spacing: normal; orphans: 2; text-align: start; text-indent: 0px; text-transform: none; widows: 2; word-spacing: 0px; -webkit-text-stroke-width: 0px; white-space: normal; text-decoration-thickness: initial; text-decoration-style: initial; text-decoration-color: initial;"><summary style="box-sizing: border-box; background-color: rgba(0, 184, 212, 0.1); border-top: none; border-right: none; border-bottom: none; border-left: 0.2rem none; border-image: initial; font-weight: 700; margin: 0px -0.6rem; padding: 0.4rem 1.8rem 0.4rem 2rem; position: relative; cursor: pointer; display: block; min-height: 1rem; overflow: hidden; border-top-left-radius: 0.1rem; border-top-right-radius: 0.1rem; -webkit-tap-highlight-color: transparent; outline: none;">Info</summary><p style="box-sizing: border-box; margin-bottom: 0.6rem;">所有数学运算都会转换成浮点数进行，以保证运算精度</p></details>

###### **宏定义**

![image-20220528150542643](https://book.guyuehome.com/ROS2/3.%E5%B8%B8%E7%94%A8%E5%B7%A5%E5%85%B7/image/3.4_Gazebo/image-20220528150542643.png)

机器人的轮子我们也做成宏定义，定义方式是通过这个<xacro:macro>标签描述的，还可以像函数一样，设置里边会用到的一些参数，比如这里的A、B、C。

当需要使用这个宏的时候，就可以像这样，通过宏名字的标签，来调用，同时要记得把几个参数设置好。

![image-20220528150603346](https://book.guyuehome.com/ROS2/3.%E5%B8%B8%E7%94%A8%E5%B7%A5%E5%85%B7/image/3.4_Gazebo/image-20220528150603346.png)

比如在模型中，轮子的宏定义是这样的，包含了link描述和joint关节设置，link的名称和关节的位置，是通过输入的参数来区分的，在使用的时候，通过这两句调用，两个轮子就出现了。

![image-20220528150619175](https://book.guyuehome.com/ROS2/3.%E5%B8%B8%E7%94%A8%E5%B7%A5%E5%85%B7/image/3.4_Gazebo/image-20220528150619175.png)

这里的1和-1，是设置关节位置的，刚好是一个镜像关系。

###### **文件包含**

![image-20220528150712684](https://book.guyuehome.com/ROS2/3.%E5%B8%B8%E7%94%A8%E5%B7%A5%E5%85%B7/image/3.4_Gazebo/image-20220528150712684.png)

宏定义是可以嵌套的，于是我们把机器人的底盘也做成了一个宏，然后使用另外一个模型文件，对底盘宏定义的文件做了一个包含，然后再调用。

![image-20220528150741631](https://book.guyuehome.com/ROS2/3.%E5%B8%B8%E7%94%A8%E5%B7%A5%E5%85%B7/image/3.4_Gazebo/image-20220528150741631.png)

这种流程是不是似曾相识，很像C语言中的include文件包含，然后再去调用里边的某些函数。

到这里为止，仿真使用的模型优化还没有结束，接下来我们还得加入一些仿真必备的模块和参数。

##### **机器人仿真模型配置**

###### **完善物理参数**

第一步是确保每一个link都有惯性参数和碰撞属性，因为Gazebo是物理仿真平台，必要的物理参数是一定需要的。

![image-20220528150842585](https://book.guyuehome.com/ROS2/3.%E5%B8%B8%E7%94%A8%E5%B7%A5%E5%85%B7/image/3.4_Gazebo/image-20220528150842585.png)

![image-20220528150832258](https://book.guyuehome.com/ROS2/3.%E5%B8%B8%E7%94%A8%E5%B7%A5%E5%85%B7/image/3.4_Gazebo/image-20220528150832258.png)

###### **添加Gazebo标签**

第二步是为link添加gazebo标签，主要是为了可以在gazebo中渲染每一个link的颜色，因为URDF中的颜色系统和gazebo中的不同，所以得做一步这样的冗余配置。

![image-20220528150931153](https://book.guyuehome.com/ROS2/3.%E5%B8%B8%E7%94%A8%E5%B7%A5%E5%85%B7/image/3.4_Gazebo/image-20220528150931153.png)

###### **配置传动装置**

第三步是要给运动的joint配置传动装置，可以理解为仿真了一个电机。

![image-20220528150958309](https://book.guyuehome.com/ROS2/3.%E5%B8%B8%E7%94%A8%E5%B7%A5%E5%85%B7/image/3.4_Gazebo/image-20220528150958309.png)

###### **添加控制器插件**

第四步，要添加一个gazebo的控制器插件，小车是差速控制的，那就添加差速控制器插件，这样在不同角度下两个电机的速度分配，就可以交给控制器插件来完成了。

![image-20220528151019063](https://book.guyuehome.com/ROS2/3.%E5%B8%B8%E7%94%A8%E5%B7%A5%E5%85%B7/image/3.4_Gazebo/image-20220528151019063.png)

###### **构建仿真环境**

接下来就考虑如何把模型加载到Gazebo中了，需要用到一个gazebo提供的功能节点spwan_entity。

#### **Rviz三维可视化平台**

机器人开发过程中，各种各样的功能，如果我们只是从数据层面去做分析，很难快速理解数据的效果，比如给你一堆0到255的数字，问这幅图像描述的内容是什么？你肯定一脸懵。但如果我们把这些数字通过颜色渲染出来，岂不就一目了然么？

![image-20220528152054838](https://book.guyuehome.com/ROS2/3.%E5%B8%B8%E7%94%A8%E5%B7%A5%E5%85%B7/image/3.5_Rviz/image-20220528152054838.jpg)

![image-20220528152050544](https://book.guyuehome.com/ROS2/3.%E5%B8%B8%E7%94%A8%E5%B7%A5%E5%85%B7/image/3.5_Rviz/image-20220528152050544.jpg)

类似的场景还有很多，比如机器人模型，我们需要知道自己设计的模型长啥样，还有模型内部众多坐标系在运动过程中都在哪些位置。

再比如机械臂运动规划和移动机器人自主导航，我们希望可以看到机器人周边的环境、规划的路径，当然还有传感器的信息，摄像头、三维相机、激光雷达等等，数据是用来做计算的，可视化的效果才是给人看的。

所以，数据可视化可以大大提高开发效率，Rviz就是这样一款机器人开发过程中的数据可视化软件，机器人模型、传感器信息、环境信息等等，全都可以在这里搞定。

##### **Rviz介绍**

一句话说明Rviz的功能，只要有数据，它就可以可视化，只有我们想不到的，没有Rviz做不到的。

![image-20220528151929609](https://book.guyuehome.com/ROS2/3.%E5%B8%B8%E7%94%A8%E5%B7%A5%E5%85%B7/image/3.5_Rviz/image-20220528151929609.jpg)

Rviz的核心框架是基于**Qt可视化工具**打造的一个开放式平台，官方出厂就自带了很多机器人常用的可视化显示插件，只要我们按照ROS中的消息发布对应的话题，就可以看到图形化的效果了。如果我们对显示的效果不满意，或者想添加某些新的显示项，也可以在Rviz这个平台中，开发更多可视化效果，方便打造我们自己的上位机。

##### **运行方法**

启动一个终端，使用如下命令即可启动：

```
$ ros2 run rviz2 rviz2
```

![image-20220528152204601](https://book.guyuehome.com/ROS2/3.%E5%B8%B8%E7%94%A8%E5%B7%A5%E5%85%B7/image/3.5_Rviz/image-20220528152204601.jpg)

##### **彩色相机仿真与可视化**

摄像头肯定是最为常用的一种传感器了，我们先来给机器人装上摄像头。

###### **仿真插件配置**

关于传感器的仿真，都需要使用Gazebo提供的插件，摄像头对应的插件叫做libgazebo_ros_camera.so，我们对照模型的代码给大家介绍这个插件的使用方法。

learning_gazebo/urdf/sensers/camera_gazebo.xacro

```
<gazebo reference="${prefix}_link">
    <sensor type="camera" name="camera_node">
        <update_rate>30.0</update_rate>
        <camera name="head">
            <horizontal_fov>1.3962634</horizontal_fov>
            <image>
                <width>1280</width>
                <height>720</height>
                <format>R8G8B8</format>
            </image>
            <clip>
                <near>0.02</near>
                <far>300</far>
            </clip>
            <noise>
                <type>gaussian</type>
                <mean>0.0</mean>
                <stddev>0.007</stddev>
            </noise>
        </camera>
        <plugin name="gazebo_camera" filename="libgazebo_ros_camera.so">
            <ros>
                <!-- <namespace>stereo</namespace> -->
                <remapping>~/image_raw:=image_raw</remapping>
                <remapping>~/camera_info:=camera_info</remapping>
            </ros>
            <camera_name>${prefix}</camera_name>
            <frame_name>${prefix}_link</frame_name>
            <hack_baseline>0.2</hack_baseline>
        </plugin>
    </sensor>
</gazebo>
```

主要配置项如下：

- <sensor>标签：描述传感器

> type：传感器类型，camera
>
> name：摄像头命名，自由设置

- <camera>标签：描述摄像头参数

> 分辨率，编码格式，图像范围，噪音参数等

- <plugin>标签：加载摄像头仿真插件

###### **运行仿真环境**

模型已经配置好啦，能不能把摄像头成功仿真出来，并且在Rviz中看到图像信息，我们拭目以待。

```
$ ros2 launch learning_gazebo load_mbot_camera_into_gazebo.launch.py
```

![image-20220528152414923](https://book.guyuehome.com/ROS2/3.%E5%B8%B8%E7%94%A8%E5%B7%A5%E5%85%B7/image/3.5_Rviz/image-20220528152414923.jpg)

可以使用命令行看下仿真出来的图像话题：

![image-20220528152456256](https://book.guyuehome.com/ROS2/3.%E5%B8%B8%E7%94%A8%E5%B7%A5%E5%85%B7/image/3.5_Rviz/image-20220528152456256.jpg)

###### **图像数据可视化**

我们使用Rviz可视化显示图像信息，先来启动Rviz：

```
$ ros2 run rviz2 rviz2
```

启动成功后，在左侧Displays窗口中点击“Add”，找到Image显示项，OK确认后就可以加入显示列表啦，然后配置好该显示项订阅的图像话题，就可以顺利看到机器人的摄像头图像啦。

![image-20220528152442483](https://book.guyuehome.com/ROS2/3.%E5%B8%B8%E7%94%A8%E5%B7%A5%E5%85%B7/image/3.5_Rviz/image-20220528152442483.jpg)

##### **三维相机仿真与可视化**

二维摄像头不过瘾，想不想试试三维相机，比如我们常用的Kinect体感传感器，或者Intel的Realsense，可以获取外部环境的点云数据。这种相机的价格比usb摄像头可贵不少，不过我们也可以通过仿真，一分钱不用，就可以玩起来。

###### **仿真插件配置**

三维相机使用的Gazebo插件也是libgazebo_ros_camera.so，配置方法如下：

learning_gazebo/urdf/sensers/kinect_gazebo.xacro

```
<gazebo reference="${prefix}_link">
    <sensor type="depth" name="${prefix}">
        <always_on>true</always_on>
        <update_rate>15.0</update_rate>
        <pose>0 0 0 0 0 0</pose>
        <camera name="kinect">
            <horizontal_fov>${60.0*M_PI/180.0}</horizontal_fov>
            <image>
                <format>R8G8B8</format>
                <width>640</width>
                <height>480</height>
            </image>
            <clip>
                <near>0.05</near>
                <far>8.0</far>
            </clip>
        </camera>
        <plugin name="${prefix}_controller" filename="libgazebo_ros_camera.so">
            <ros>
                <!-- <namespace>${prefix}</namespace> -->
                <remapping>${prefix}/image_raw:=rgb/image_raw</remapping>
                <remapping>${prefix}/image_depth:=depth/image_raw</remapping>
                <remapping>${prefix}/camera_info:=rgb/camera_info</remapping>
                <remapping>${prefix}/camera_info_depth:=depth/camera_info</remapping>
                <remapping>${prefix}/points:=depth/points</remapping>
            </ros>
            <camera_name>${prefix}</camera_name>
            <frame_name>${prefix}_frame_optical</frame_name>
            <hack_baseline>0.07</hack_baseline>
            <min_depth>0.001</min_depth>
            <max_depth>300.0</max_depth>
        </plugin>
    </sensor>
</gazebo>
```

###### **运行仿真环境**

使用如下命令启动仿真环境：

```
$ ros2 launch learning_gazebo load_mbot_rgbd_into_gazebo.launch.py
```

![image-20220528152559248](https://book.guyuehome.com/ROS2/3.%E5%B8%B8%E7%94%A8%E5%B7%A5%E5%85%B7/image/3.5_Rviz/image-20220528152559248.jpg)

启动成功后，可以看下当前的话题列表，已经产生了三维相机的相关话题。

![image-20220528152611362](https://book.guyuehome.com/ROS2/3.%E5%B8%B8%E7%94%A8%E5%B7%A5%E5%85%B7/image/3.5_Rviz/image-20220528152611362.jpg)

##### **点云数据可视化**

运行Rviz：

```
$ ros2 run rviz2 rviz2
```

同样的流程，点击Add，添加PointCloud2，设置订阅的点云话题，还要配置Rviz的参考系是odom，就可以看到点云数据啦，每一个点都是由xyz位置和rgb颜色组成。

![image-20220528152552742](https://book.guyuehome.com/ROS2/3.%E5%B8%B8%E7%94%A8%E5%B7%A5%E5%85%B7/image/3.5_Rviz/image-20220528152552742.jpg)

##### **激光雷达仿真与可视化**

除了摄像头和三维相机，激光雷达也是很多移动机器人常备的传感器，包括自动驾驶汽车，我们也来试一试。

###### **仿真插件配置**

雷达使用的Gazebo插件是libgazebo_ros_ray_sensor.so，配置方法如下：

learning_gazebo/urdf/sensers/lidar_gazebo.xacro

```
<gazebo reference="${prefix}_link">
    <sensor type="ray" name="rplidar">
        <update_rate>20</update_rate>
        <ray>
            <scan>
              <horizontal>
                <samples>360</samples>
                <resolution>1</resolution>
                <min_angle>-3</min_angle>
                <max_angle>3</max_angle>
              </horizontal>
            </scan>
            <range>
              <min>0.10</min>
              <max>30.0</max>
              <resolution>0.01</resolution>
            </range>
            <noise>
              <type>gaussian</type>
              <mean>0.0</mean>
              <stddev>0.01</stddev>
            </noise>
        </ray>
        <plugin name="gazebo_rplidar" filename="libgazebo_ros_ray_sensor.so">
      <ros>
    <namespace>/</namespace>
    <remapping>~/out:=scan</remapping>
      </ros>
      <output_type>sensor_msgs/LaserScan</output_type>
        </plugin>
    </sensor>
</gazebo>
```

###### **运行仿真环境**

使用如下命令启动仿真环境：

```
$ ros2 launch learning_gazebo load_mbot_laser_into_gazebo.launch.py
```

![image-20220528152754541](https://book.guyuehome.com/ROS2/3.%E5%B8%B8%E7%94%A8%E5%B7%A5%E5%85%B7/image/3.5_Rviz/image-20220528152754541.jpg)

在话题列表中也可以看到激光雷达啦。

![image-20220528152810332](https://book.guyuehome.com/ROS2/3.%E5%B8%B8%E7%94%A8%E5%B7%A5%E5%85%B7/image/3.5_Rviz/image-20220528152810332.jpg)

##### **点云数据可视化**

启动Rviz：

```
$ ros2 run rviz2 rviz2
```

点击Add，选择Laserscan，然后配置订阅的话题名，rviz的固定坐标系依然是odom，此时就可以看到激光点啦。

![image-20220528152821691](https://book.guyuehome.com/ROS2/3.%E5%B8%B8%E7%94%A8%E5%B7%A5%E5%85%B7/image/3.5_Rviz/image-20220528152821691.jpg)

##### **Rviz vs Gazebo**

好啦，通过这几个案例，相信大家对Rviz可视化平台的使用流程已经非常熟悉了，也了解了常用传感器的仿真方法。

讲到这里，Gazebo和Rviz这两个软件的具体功能，大家是不是会有一些混淆。

![image-20220528152913715](https://book.guyuehome.com/ROS2/3.%E5%B8%B8%E7%94%A8%E5%B7%A5%E5%85%B7/image/3.5_Rviz/image-20220528152913715.jpg)

我们再来强调下：

- Gazebo是**仿真平台**，核心功能是**创造数据**，我们没有机器人或者传感器，它可以帮我们做一个虚拟的；
- Rviz是**可视化平台**，核心功能是**显示数据**，如果没有数据，它也巧妇难为无米之炊。

所以在很多时候，我们使用Gazebo做机器人仿真的时候，也会启动Rviz来显示仿真环境的信息，如果自己手上有真实机器人的话，Gazebo就用不到了，不过还是会用Rviz显示真实机器人传感器的信息。

### **rqt介绍**

正如RQT的命名，它和Rviz一样，也是基于QT可视化工具开发而来，在使用前，我们需要通过这样一句指令进行安装，然后就可以通过rqt这个命令启动使用了。

```
$ sudo apt install ros-humble-rqt
$ rqt
```

![image-20220528153119321](https://book.guyuehome.com/ROS2/3.%E5%B8%B8%E7%94%A8%E5%B7%A5%E5%85%B7/image/3.6_Rqt/image-20220528153119321.png)

类似这个界面一样，里边可以加载很多小模块，每个模块都可以实现一个具体的小功能，一些常用的功能如下：

#### **日志显示**

![image-20220528153332794](https://book.guyuehome.com/ROS2/3.%E5%B8%B8%E7%94%A8%E5%B7%A5%E5%85%B7/image/3.6_Rqt/image-20220528153332794.png)

#### **图像显示**

![image-20220528153354370](https://book.guyuehome.com/ROS2/3.%E5%B8%B8%E7%94%A8%E5%B7%A5%E5%85%B7/image/3.6_Rqt/image-20220528153354370.png)

#### **发布话题数据/调用服务请求**

![image-20220528153406339](https://book.guyuehome.com/ROS2/3.%E5%B8%B8%E7%94%A8%E5%B7%A5%E5%85%B7/image/3.6_Rqt/image-20220528153406339.png)

#### **绘制数据曲线**

![image-20220528153414784](https://book.guyuehome.com/ROS2/3.%E5%B8%B8%E7%94%A8%E5%B7%A5%E5%85%B7/image/3.6_Rqt/image-20220528153414784.png)

#### **数据包管理**

![image-20220528153423185](https://book.guyuehome.com/ROS2/3.%E5%B8%B8%E7%94%A8%E5%B7%A5%E5%85%B7/image/3.6_Rqt/image-20220528153423185.png)

#### **节点可视化**

![image-20220528153433016](https://book.guyuehome.com/ROS2/3.%E5%B8%B8%E7%94%A8%E5%B7%A5%E5%85%B7/image/3.6_Rqt/image-20220528153433016.png)

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



#### Package：功能包，功能源码的聚集地

#### Node：机器人的工作细胞

#### Topic：节点之间传递数据的桥梁

#### Service：节点之间的你问我答

#### Interface：数据传递的标准结构

#### Parameter：机器人系统的全局字典

#### Action：完整行为的流程管理

#### me

#### DDS(Data Distribution Service)：机器人的神经网络

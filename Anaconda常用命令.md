Anaconda常用命令
首先说一点：Windows下 Anaconda Prompt 这个东西就是用来管理Anaconda的，使用的是conda这样的一种命令
在Linux中，可以直接在终端中输入conda 命令

可以使用conda命令创建新的python环境（python版本，包），新的环境与原来的环境不相关。这样，方便不同的应用中使用不同的python版本。
创建新环境的步骤如下：
1、首先在所在系统中安装Anaconda。可以打开命令行输入conda -V检验是否安装以及当前conda的版本。

2、conda常用的命令。

    1） conda list  查看安装了哪些包。
    
    2） conda env list  或  conda info -e  查看当前存在哪些虚拟环境
    
    3） conda update conda  检查更新当前conda
    
    4） conda --version  查询conda版本
    
    5） conda -h  查询conda的命令使用

3、创建python虚拟环境。

     使用  conda create -n your_env_name python=X.X （2.7、3.6等)命令创建python版本为X.X、名字为your_env_name的虚拟环境。your_env_name文件可以在Anaconda安装目录envs文件下找到。
    
     注意：默认的情况下只安装了一些必须的包，并不会像我们安装anaconda时自动安装很多常用的包。要实现上面的功能，则须在末尾加上‘anaconda’，完整命令是：

conda create -n your_env_name python=X.X anaconda
4、使用激活(或切换不同python版本)的虚拟环境。

    打开命令行输入python --version可以检查当前python的版本。
    
    使用如下命令即可 激活你的虚拟环境(即将python的版本改变)。
    
    Linux:   source activate your_env_name (虚拟环境名称)
    
    Windows:  activate your_env_name (虚拟环境名称)

   这是再使用  python --version 可以检查当前python版本是否为想要的。

5、对虚拟环境中安装额外的包。

    使用命令 conda install -n your_env_name [package] 即可安装package到your_env_name中

6、关闭虚拟环境(即从当前环境退出返回使用PATH环境中的默认python版本)。

   使用如下命令即可。

   Linux: source deactivate

   Windows: deactivate
7、删除虚拟环境。

   使用命令 conda remove -n your_env_name(虚拟环境名称) --all ， 即可删除。

8、删除环境中的某个包。

   使用命令 conda remove --name your_env_name package_name  即可。

分类: Python Basic
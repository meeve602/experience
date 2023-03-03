**pip安装方法常用的pip命令**

D:\>pip install <第三方库名>-

 安装指定的第三方库

D:\>pip install –U <第三方库名>- 

使用-U标签更新已安装的指定第三方库

D:\>pip uninstall <第三方库名>-

 卸载指定的第三方库

D:\>pip download <第三方库名>

下载但不安装指定的第三方库

D:\>pip show <第三方库名>-

 列出某个指定第三方库的详细信息

D:\>pip search <关键词>-

根据关键词在名称和介绍中搜索第三方库

pip search blockchain

D:\>pip list

列出当前系统已经安装的第三

新建test.py文件，打断点调试。正在运行的行WingIDE标记为红色,在Debug probe中输入想看的变量的名字即可打印出变量对应的值

打断点直接在代码行左侧双击即可

debug probe输入对应值查看 

pandas 读取文件

给read_csv等方法使用时，直接加上r即可食用，pd.read_csv(r"F:\test_data.csv")

df = pd.read_csv(r"D:\advance_technology\pytorch.study\Learn-Pytorch-And-Become-A-Data-Scientist-master\chapter2\Titanic-dataset/train.csv",encoding= "utf8").tar.bz2格式
将已经下好的包移动到 ...\Anaconda3\pkgs目录下，

在该目录下打开CMD，运行如：

conda install --use-local  **.tar.bz2
1
应用场景2
一个文件夹只要包含.py文件和__init__()文件（没有内容也行，但必须要有）就可构成一个包，可以通过setup.py来安装。

一般是GitHub上的提供，一般会有setup.py文件，没有就需要自己写了

一般用如下命令安装pip install git+https://github.com/用户名/仓库名

这个命令会首先clone下这个仓库，然后利用setup.py文件来安装，如果服务器上连GitHub很费劲，就需要手动先clone下来，再上传，然后利用setup.py来安装

setup.py来安装
移动到setup.py所在目录下，打开终端
启动特定python环境
运行如下命令
python setup.py build
python setup.py install
1
2
Note: 确保要安装的包的对应的文件夹里有__init__()文件，没有自己新建一个
————————————————
版权声明：本文为CSDN博主「星辰·」的原创文章，遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接及本声明。
原文链接：https://blog.csdn.net/weixin_43580966/article/details/104673611

1.用管理员方式打开cmd

2.首先通过pip命令安装wheel
如果提示’pip’不是内部或外部命令，也不是可运行的程序或批处理文件

①将python安装目录下的scripts目录（例如D:\Python27\Scripts）添加到系统环境变量path里，注意前加分号。再执行该命令

pip install wheel

②在cmd下进入到`**D:\Python27\Scripts**`目录下执行该命令

pip install wheel

 

3.安装whl文件

```
 
```

1. `①如果将D:\Python27\Scripts目录添加到path中，可以直接在whl文件所在目录用管理员打开一个cmd窗口，直接执行下面的语句。`
2.  
3. `pip install python_dateutil-2.5.3-py2.py3-none-any.whl`
4.  
5. `②否则的话，需要在D:\Python27\Scripts目录下用管理员打开cmd，运行pip命令，文件名应该写全路径）`
6.  
7. `pip install C:\Users\xxx\Downloads\python_dateutil-2.5.3-py2.py3-none-any.whl`

### 1、Anaconda**



Anaconda 就是管理第三库的工具，同时支持“多开”。



你可以用 Anaconda 创建**多个虚拟环境**。



啥意思？

module load anaconda/2020.11



一个**虚拟环境**好比一个人：



- 培养小王为数学家，专门负责数学相关的事。
- 培养小李为语言学家，专门负责语言相关的事。



体现到虚拟环境上，就是这样：



![图片](https://mmbiz.qpic.cn/mmbiz_png/v1JN0W4OpXgvnzpqMFs1CVd7ZtG4F27cvTpxXqxzsicl8wibPruY1MLZEGZzMLMtggAgDB5wjdpuADLRNHrAiaslw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



我创建了很多虚拟环境。



base 是安装 Anaconda 自带的一个基础环境。其它都是根据自己需求，创建的一个个独立环境。



比如，名为 jack 的环境，是一个通用的开发环境。而名为 faceswap 的环境是我专门为换脸算法搭建的环境，因为它的依赖和有些通用第三方库包是冲突的。



Anaconda 还是跨平台的，在 Windows、MacOS、Linux 都可以安装。



### **2、Jupyter Notebook**



小白推荐 Jupyter Notebook，为啥不推荐 Pycharm 这类 IDE 呢？



因为 Jupyter 安装简单，并且好用，可以在多种平台运行。



工作后，跑算法，往往都是在服务器上运行的。



连个图像界面都没有的服务器，你还能用 Pycharm ？



Jupyter Notebook 是一个**基于网页**的交互式计算笔记本环境。



![图片](https://mmbiz.qpic.cn/mmbiz_png/v1JN0W4OpXgvnzpqMFs1CVd7ZtG4F27cOTgrm1icuCEf0h4djB237OnKTCric87ZURzibgJasaZIAU6mwV9qhJtPg/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



实现了**文字和代码**的完美结合，你甚至可以**边学习边做笔记**，文本编辑还支持 Markdown 格式，插入各种**数学公式**也不在话下。



并且由于 Jupyter Notebook 是基于网页的，你完全可以在服务器端开启服务，本地电脑打开网页，运行各种服务器端的代码。



如果你是做算法、做爬虫，刚学 Python 的小白，不涉及浩大的 Python 工程的开发，那么**别犹豫**，用 Jupyter Notebook 就对了。



### **3、安装**



Anaconda + Jupyter Notebook 的好处安利个遍。



那么，怎么安装呢？



Anaconda 下载地址：

https://www.anaconda.com/products/individual#download-section



根据自己的环境选择安装包：



![图片](https://mmbiz.qpic.cn/mmbiz_png/v1JN0W4OpXgvnzpqMFs1CVd7ZtG4F27cTE9akbg6r4yAibIwFukREhIDYicjjiaPb9f28qpunvp50fNvkPcsibyAibg/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



安装很简单，傻瓜式下一步安装即可。



Windows 安装完，需要**手动添加**环境变量。



Linux 和 MacOS 在安装过程中，会有提示**是否设置**环境变量。



Windows 添加环境变量需要在电脑->鼠标右键->属性->高级系统设置->环境变量->Path中设置。



![图片](https://mmbiz.qpic.cn/mmbiz_png/v1JN0W4OpXgvnzpqMFs1CVd7ZtG4F27cpKH48pZb9M5AaZUMDrAWgGwbWyZOnLibMINPfia54KHicOeNWwJrNHkYQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



 D:\Anaconda 为 Anaconda 的安装目录，将下面这两个地址添加到 Path 中即可。



- 
- 

```
D:\AnacondaD:\Anaconda\Scripts
```



都配置好后，可以在 cmd 或 Anaconda Prompt 中使用 Anaconda 搭建环境了。



输入指令：



- 

```
conda create -n your_name jupyter notebook
```



这句话的意思是创建一个名字为 your_name 的虚拟环境，并且这个虚拟环境额外安装 jupyter notebook 第三方库。



可以将 your_name 改为你自己喜欢的名字，这个名字是你的虚拟环境的名字，自己随便取，比如jack。



随后，输入y进行安装：



![图片](https://mmbiz.qpic.cn/mmbiz_png/v1JN0W4OpXgvnzpqMFs1CVd7ZtG4F27cYtmrKpU4hTwEBKicZW2MH6xP9zAlIafOd7WTYVpvKZAUdwbicUW8BGBA/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



安装好后，可以通过指令 conda info -e 查看已有环境情况。



![图片](https://mmbiz.qpic.cn/mmbiz_png/v1JN0W4OpXgvnzpqMFs1CVd7ZtG4F27ccuskX4LKCXE0UXBiaSWIKMdPJz8vCQV38KxNC1iaRhUD7XkbnRtibEfIg/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



从上图可以看到，有两个环境，一个是 base ，自带的基础环境，另一个是我们新创建的名为 jack 的环境。



安装好环境后，我们可以使用指令激活 jack 环境：



- 

```
activate jack
conda deactivate
```



![图片](https://mmbiz.qpic.cn/mmbiz_png/v1JN0W4OpXgvnzpqMFs1CVd7ZtG4F27c2EPibMm3594YWfyrJZBaicMNXic9MY90SJZK04rgaFt1VYQG6fJttot6Q/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



可以看到，我们的环境由 base 变成了 jack 。



接下来，我们就可以在这个环境里，安装自己想要的第三方库，比如 requests。



- 

```
conda install requests
```



对于 conda 搜不到的包，也可以使用 pip 安装：



- 

```
python -m pip install xxx
```



需要安装的第三方库安装完毕，可使用命令直接打开 Jupyter Notebook：



- 

```
jupyter notebook
```



效果如下：



![图片](https://mmbiz.qpic.cn/mmbiz_gif/v1JN0W4OpXgvnzpqMFs1CVd7ZtG4F27cS3iccIQMThHagEnic4jiaOoLMQsrZAribFoN0gOx09YzGC7feRF5ibAjaSw/640?wx_fmt=gif&tp=webp&wxfrom=5&wx_lazy=1)



创建一个新的 notebook：



![图片](https://mmbiz.qpic.cn/mmbiz_png/v1JN0W4OpXgvnzpqMFs1CVd7ZtG4F27csvwpslTWUlI0iaW3QJr4SxLa3puA9fJlBkyAfQyT5gCNMVoUGsrghQQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



输入代码后，按 Ctrl + Enter 快捷键，即可运行程序：



![图片](https://mmbiz.qpic.cn/mmbiz_png/v1JN0W4OpXgvnzpqMFs1CVd7ZtG4F27clH9yCkh7f3aThQaFuhcwtLN5I91FSp44aJu1laLFVWY3cSRhIBMbWg/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



这个 Jupyter Notebook 使用的环境就是名为 jack 的虚拟环境。



想安装 Pytorch 啥的，直接在这个虚拟环境里安装即可，真香！







  - http://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/win-64/
  - http://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/win-64/
  - http://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/pytorch/


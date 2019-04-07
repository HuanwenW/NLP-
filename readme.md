## Welcome to NLP-2019-huanhuan-homework-1
### 内容涵盖：
- Anaconda  安装  
- Conda 学习  
- Python编辑器安装与学习： jupyter notebook  或者 pycharm   
- Tensorflow 库安装与学习

1. **Anaconda 安装**   
**第一步：** 下载并安装 anaconda，先到 [官网](https://www.continuum.io/downloads)  下载anaconda, 现在的版本有python2.7版本和python3.5版本，下载好对应版本、对应系统的anaconda，本记录以windows8.1+python3.5为例说明：
![image](http://images2015.cnblogs.com/blog/140867/201601/140867-20160111155041616-433515227.png)  
下载的是一个可执行的exe文件，下载完成好，直接双击就可以安装了。  

**第二步：** 在安装的时候，假设我们安装在D盘根目录，如：
![image](http://images2015.cnblogs.com/blog/140867/201601/140867-20160111155053960-1150576793.png)  
并且将两个选项都选上，将安装路径写入环境变量。  
![image](http://images2015.cnblogs.com/blog/140867/201601/140867-20160111155106522-1988128417.png)  
然后等待安装完成就可以了。

**第三步：** 安装完成后，按windows+R，输入cmd命令回车 

输入conda list 就可以查询现在安装了哪些库，常用的numpy, scipy名列其中。如果你还有什么包没有安装上，可以运行conda install ***  来进行安装。

2.**Conda 学习**  
 (1) Anaconda就是可以便捷获取包且对包能够进行管理，同时对环境可以统一管理的发行版本。Anaconda包含了conda、Python在内的超过180个科学包及其依赖项。  
 (2) **常用命令**
  - 验证conda已安装 ：conda --version   或  conda -V  
  - 更新conda到当前版本： conda update conda
  - 获取帮助：conda --help  或  conda -h
  - 更多命令使用详见最后  参考链接3-5
 
 3. **Python编辑器安装与学习：jupyter notebook  或者 pycharm**
  - pycharm之前已经安装，此处不再重复，详见参考教程链接6-7  
  - **jupyter notebook**安装及使用
   **第一步：** 在命令行窗口输入以下命令即可:  
   
     > pip install  jupyter  
     
   **第二步：** 输入jupyter   notebook  即可自动弹出一个网页版编辑器  
    ![image](https://github.com/HuanwenW/MyPostImag/blob/master/007-picture/jupyter-1.png)  
   **第三步：** 在打开的浏览器界面，在new下拉框中选择python3  
    ![image](https://github.com/HuanwenW/MyPostImag/blob/master/007-picture/jupyter-2.png)   
   **第四步：** 进入以下页面即可进行编写  
    ![image](https://github.com/HuanwenW/MyPostImag/blob/master/007-picture/jupyter-3.png)    
    
4. **Tensorflow 库安装与学习**
- **Tensorflow 库安装**
TensorFlow的安装有GPU和CPU两个不同版本，我的GPU不行，所以我安装的是 **CPU** 的版本。采用的输入Shell指令进行安装。  
**第一步：** CPU版--：  

> pip3 install --upgrade https://storage.googleapis.com/tensorflow/windows/cpu/tensorflow-0.12.0-cp35-cp35m-win_amd64.whl

**第二步：** 更新，安装成功之后的TensorFlow的版本是0.12的，所以进行更新：

> pip3 install tensorflow   

**第三步：** 测试TensorFlow

打开“python3.5”，输入测试程序,查看结果

    >>> import tensorflow as tf  
    >>> hello = tf.constant('Hello, TensorFlow!')  
    >>> sess = tf.Session()  
    >>> print(sess.run(hello))  
    Hello, TensorFlow!  
    >>> a = tf.constant(10)  
    >>> b = tf.constant(32)  
    >>> print(sess.run(a + b))  
    
 运行结果：  
 
 ![image](https://github.com/HuanwenW/MyPostImag/blob/master/007-picture/tensorflow-1.jpg?raw=true)

- **Tensorflow学习入门笔记很不错，详见参考教程10**

## 参考教程 
1. [Windows下Anaconda的安装和简单使用](https://blog.csdn.net/dq_dm/article/details/47065323)
2. [推荐教程-Anaconda介绍、安装及使用教程](https://zhuanlan.zhihu.com/p/32925500)
3. [Conda命令手册](https://blog.csdn.net/childcyr/article/details/80367867)
4. [conda常用命令](https://www.cnblogs.com/sddai/p/10322603.html)
5. [Conda常用命令整理](https://blog.csdn.net/menc15/article/details/71477949)
6. [推荐教程-PyCharm 安装教程（Windows）](http://www.runoob.com/w3cnote/pycharm-windows-install.html)
7. [Pycharm学生免费专业版-安装教程](https://blog.csdn.net/SpringRolls/article/details/80363119)
8. [Windows7 64bits下安装TensorFlow CPU版本（图文详解）](https://www.cnblogs.com/zlslch/p/6964944.html)
9. [推荐教程-手把手教你如何安装Tensorflow](https://blog.csdn.net/Cs_hnu_scw/article/details/79695347)
10. [推荐教程-TensorFlow学习笔记1：入门](http://www.jeyzhang.com/tensorflow-learning-notes.html)

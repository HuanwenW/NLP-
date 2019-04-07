##  Markdown 插入图片不友好，如何解决？

### 前奏：

  想要Markdown中图文并茂记录学习历程，偏偏却卡在了插图上，经过牛牛二虎之力，灰心丧气，终于得救~~~下面我来综合多篇博客，给入门的小白(git使用都包教)一条生路！
  
- **环境**：基于github网页版Markdown图片插入记录
- **问题来源：** [MarkDown添加图片的三种方式](https://blog.csdn.net/slaughterdevil/article/details/79255933)无法满足我的需求，问题如下：  
![image](https://github.com/HuanwenW/MyPostImag/blob/master/007-picture/markD-%E6%8F%92%E5%9B%BE-1.jpg?raw=true)  
-  **解决问题思路：**  （截图中提到的方法1和2结合）即本地图片生成链接（保证图片何时何地都可以显示）+ 插入图片连接方法
- **前方高能，提高注意力咯！！**
1. **GitHub 建立仓库篇**
**第一步：** 在GitHub上建立一个图片存储仓库  
(1) 比如我建立的MyPostImage，用来存储需要的图片。  
![image](https://github.com/HuanwenW/MyPostImag/blob/master/190406-markDown/MD-Pic-1.png?raw=true)
(2) 复制项目地址：
![image](https://github.com/HuanwenW/MyPostImag/blob/master/190406-markDown/MD-Pic-2.jpg?raw=true)
**第二步：** 把Github项目-MyPostImage克隆到本地 ：    
(1) 新建一个文件夹-githubPicture，在**文件夹githubPicture内**点击右键--选择Git Bash Here 打开终端，输入命令：  
![image](https://github.com/HuanwenW/MyPostImag/blob/master/190406-markDown/MD-Pic-3.png?raw=true)  
(2) 克隆完成后结果如下：  
![image](https://github.com/HuanwenW/MyPostImag/blob/master/190406-markDown/MD-Pic-4.png?raw=true)  
(3) 发现原来的文件中出现 **MyPostImag**文件夹  
![image](https://github.com/HuanwenW/MyPostImag/blob/master/190406-markDown/MD-Pic-5.jpg?raw=true)  
**第三步：** 在克隆到本地的文件夹中建立一个文件夹--190406-markDown(名字自己取) ：   
![image](https://github.com/HuanwenW/MyPostImag/blob/master/190406-markDown/MD-Pic-6.jpg?raw=true)  
**第四步：** 把你要用的图片存到文件夹里.   

 **第五步：** 把更改push到Github仓库：  
 （1） 输入 " git init "，作用是项目里面会创建一个隐藏的.git文件，执行结果如下：
 ![image](https://github.com/HuanwenW/MyPostImag/blob/master/190406-markDown/MD-Pic-7.jpg?raw=true)    
 （2） 输入 " git add . ", 这个是将项目上所有的文件添加到仓库中的意思，如果想添加某个特定的文件，只需把' . '换成这个特定的文件名即可。  
 ![image](https://github.com/HuanwenW/MyPostImag/blob/master/190406-markDown/MD-Pic-8.png?raw=true)    
 （3） 输入 " git commit -m "first commit "，表示你对这次提交的注释，双引号里面的内容可以根据个人的需要改。例如 " git commit -m "第一次提交 "  
 ![image](https://github.com/HuanwenW/MyPostImag/blob/master/190406-markDown/MD-Pic-9.png?raw=true)  
 （4） 输入 "git remote add origin https://刚才建立的仓库地址（第一步中提到的）"  将本地的仓库关联到github上。
 ![image](https://github.com/HuanwenW/MyPostImag/blob/master/190406-markDown/MD-Pic-10.png?raw=true)   
 （5） 输入 "git push -u origin master "，这是把代码上传到github仓库的意思。  
 ![image](https://github.com/HuanwenW/MyPostImag/blob/master/190406-markDown/MD-Pic-11.png?raw=true) 
 （6） 刷新github页面，发现本地新建文件已经出现：
 ![image](https://github.com/HuanwenW/MyPostImag/blob/master/190406-markDown/MD-Pic-12.png?raw=true) 

2. **图片生成URL篇**  
（1）打开 **190406-markDown** 文件夹，双击你需要的图片进入到下面界面：
![image](https://github.com/HuanwenW/MyPostImag/blob/master/190406-markDown/MD-Pic-13.png?raw=true)   
（2）右键选择**复制图片地址**，然后按照 ![图片名称](复制好的图片地址） 格式，添加到Markdown博文中即可，比如：
我下面插入的图3的图片是这样实现的:  

> ![MD-Pic-13.png]（https://github.com/HuanwenW/MyPostImag/blob/master/190406-markDown/MD-Pic-13.png?raw=true）  

## 参考链接
1. [简单三步在Markdown 中插入图片](https://www.jianshu.com/p/e9f18be1295d)
2. [Github项目（克隆，上传）简单git命令流程使用记录](https://blog.csdn.net/hustwayne/article/details/83014499)
3. [GitHub上克隆项目到本地](https://blog.csdn.net/linton1/article/details/80320121)

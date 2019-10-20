[idea的优点](#iyd)   
[idea下载](#ixz)  
[目录文件的解释](#mlw)  
[idea使用](#isy)

- 创建
	-  [java工程](#jgc) 
	+  [module](#mod)
	+  [web工程](#web)
	-  [tomcat](#tom)
	-  [数据库](#sjk)
	-  [github项目管理](#git)
	+  [maven ](#mav)
- 设置常见的东西 
	+ [常见的视图](#cjd)
	- [项目的配置](#xmd)
		+ [项目名称](#xnm)
		+ [jdk](#jdk)
		- [编译级别](#byj)
		- [class输出路径](#cla)
		- [添加jar包](#tjj)
	- [常用的配置](#cyd1)
		+ [主题](#zt1)
		+ [字体](#zt2)
			- [注释的字体颜色](#zsd)
		+ [自动导包的功能](#zdd)
		- [行号和方法间的分割符](#hhd)
		+ [忽略大小写的提示功能 ](#hld)
		+ [设置取消单行显示tabs的操作](#ssq)
		- [修改头文档的注释信息](#xgt)
		- [项目的文件编码](#xmd)
		+ [设置自动编译](#szd)
		+ [如何使用idea中的vim](#rhs)
		
+ 功能 
	- [debug](#deb)
	- [javadoc](#jav)
	- [插件 ](#cj1)



### idea的优点

<A NAME="iyd">idea优点</A>

1. 强大的整合能力,比如说Git,MAVEN,Spring等
2. 提式功能快速 
3. 提示功能范围广
4. 好用到快捷键和代码模板 private static final psf
5. 搜索强大

<A NAME="ign">idea功能</A> 

| 安装插件后支持 | SQL类      | 基本JVM | 支持的框架             | 额外的代码提示        | 支持容器  |
|----------------|------------|---------|------------------------|-----------------------|-----------|
| PHP            | mysql      | java    | spring MVC             | html5                 | tomcat    |
| python         | postreSQL  | Groovy  | GWT                    | CSs3                  | tomee     |
| Ruby           | Oracle     | 没了    | Vaadin                 | Sass                  | weblogin  |
| scala          | SQl Server |         | Play                   | Less                  | Jboss     |
| kottlin        |            |         | Grails                 | javaScript            | Jetty     |
| ClOjrue        |            |         | Web SErvice,jsf,Struts | CoffeeScript          | WebSphere |
|                |            |         | Hibermate     ,flex    | node.js, ActionScript |           |
<A NAME="ixz">idea下载</A> 

首先上jetbrains.com==>>download>>下载ulitimate  
	window 版本就是下载好exe 一直下一步 就可以了  
	linux 版本也简单就是下载好然后解压到你想要的目录中去就可以了 然后就是[创建一个桌面的快捷方式](https://blog.csdn.net/zSY_snake/article/details/82433030)   
版本命名 年份.版本号   没有必要安装最新版 

<A NAME="mlw">目录文件的解释</A>  

| 文件名                                   | 作用                                                                                                            |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| bin                                      | 容器,执行文件和启动参数                                                                                         |
| help                                     | 帮助文档包括快捷键文档                                                                                          |
| jre64                                    | 64位java运行环境                                                                                                |
| lib                                      | idea依赖的类型                                                                                                  |
| license                                  | 插件的许可                                                                                                      |
| plugin                                   | 插件                                                                                                            |
| /bin/idea64.exe                          | idea64位的启动文件                                                                                              |
| /bin/idea.properties                     | idea的属性配置文件                                                                                              |
| .INterllijIdea++(在用户目录下的隐藏文件) | 该文件用于每个用户的配置如果idea配置出错的话就可以完全删除 这样下次重新打开idea就会生成一个新的默认配置文件了   |
| /.intellijIdea/config                    | 这个是idea配置最重要的目录了 记录了主要的功能配置 自定义代码魔板 之定义文件模板,project的task和一些个性化的配置 |
| /.intellijIdea/system                    | system目录是系统文件目录 里面记录了缓存 索引 容器文件的输出                                                     |

## idea的使用


### 创建

#### idea工程 
 <A name="jgc">java工程</A>  

 1. Create new project 正常的创建方法
 2. import project 导入一个现有的工程
 3. open 打开一个以后的工程  
 4. 可以通过服务起的项目地址打开git托管的项目

 ![开始创建项目](https://github.com/shenxixi250/photo/blob/master/idea_photo/8.png)  

这里面我要详细的说一下idea的工程的概念 idea中Project就是最大的了 各个功能是变成了module处理的
顺带提一下
+ 创建包和类   创建完工程后 会有一个src的目录 右键 New --> Package  就可以了 注意的点是 包名要全部小写 按照域名的倒序来命名  如 com.shenxixi.www

+ 类 的创建是新创建好的包下面 右键 New --> java class 命名要符合驼峰式  HelloWorld 不需要写.java

<A name="mod"> module </A> 

 一个项目可以有多个模块(module) 模块的idea中的次结构  而project是顶层的结构 也就是说一个idea窗口只能对应一个project

 小项目有时候用不多个module 所以也就不会创建  
```
创建的project右键 new-->module点击确认-->选择java点击next-->然后创建包名点击Finish就可以  
```
之后我们就可以在Module的src里写代码了,这个时候我们就可以把Project工程下的src删掉了

**如何删除模块** 

	​```
	新创建的module右键 -->Open Module Setting-->点击modules 点击那个红色的减号即可但是这个时候module还会在你的硬盘上  它只是在项目里被剔除了   如果想要彻底的删除的话 此时再在module右键 delect
	​```

​	



<A name="web"> web工程 </A> 

web的项目想要创建也很简单的就是 new project 中然后 java--->web Application的  
![web工程](https://github.com/shenxixi250/photo/blob/master/idea_photo/9.png) 
<A name="tom"> tomcat </A> 

### 安装tomcat
1. 第一步 去官网下载压缩包  https://tomcat.apache.org/download-80.cgi   注意下载一个tar.gz文件     
2. 第二步  移动到想要安装的位置  我的位置是/usr/local/tomcat
	+ 先创建文件夹  mkdir /usr/local/tomcat  
	+ 移动 mv ap。。。tar.gz /usr/local/tomcat 
	+ 解压 tar -zxvf ap。。。tar.gz  
	+ 给文件加权限sudo chmod 755 -R ap。。。(R的含义是递归权限）
3. 第三步修改 tomcat的bin目录下的startup.sh 文件  将JAVA_HOME的配置加入到文件中  因为 tomcat是依赖与java的
4. 第四步启动测试  sudo ./startup.sh   显示 Tomcat start表示成功  可以打开浏览器进行验证  localhost:8080

**参考链接 https://blog.csdn.net/weixx3/article/details/80808484**

### 在idea中使用tomcat来加载项目
1. 第一步  run--->edit configurations------->左侧的+号 ---->tomcat server --->local   （若是没有找到Tomcat Server 可以点击最后一行 34 items more）
2. 第二步  在Tomcat Server -> Unnamed -> Server -> Application server项目下，点击 Configuration ，找到本地 Tomcat 服务器，再点击 OK按钮。
![kengkeng](tomcat) 




<A name="sjk"> 数据库 </A> 

idea如何导入数据库  

1. 首先新建号项目后    
2. 右边的侧栏会有database 点击后出现Database的选择框 
3. 选择框中的+号 >>>点击后会有data source 中选择mysql即可  
4.   然后就会有如图是界面   可以
          kengkeng
    可以看到有Name Host Port端口号    Database来选择数据库   也可以暂时不选择 等创建好了在添加   注意第一次运行下方会有小的感叹号 点击安装驱动即可    然后  点击Test Connection  查看是否成功  


如何查看数据库驱动  
  在左边创建好数据库上面   右键之后找到 properties进入   界面然后在Driver中点击Mysql  进入界面   在如下图所示的地方停留就会看到 驱动的位置了     了解驱动的位置就可以在外部添加jar包了
<A name="git"> github项目管理 </A> 

同上

  <A name="mav"> maven </A>

  1. 去官网下载 [文件apach-maven](http://maven.apache.org/download.cgi) 

  2. 使用tar命令解压 在profile文件中配置MAVEN_HOME , 我的MAVEN__HOME路径是/usr/local/maven/apache-maven-3.6.2
  3. 配置Maven的本地仓库在   /MAVEN-HOME/conf/setting.xml文件中  找配置Maven的本地仓库 在   /MAVEN-HOME/conf/setting.xml文件中  找到
  <localRepository>/home/shen/Documents/maven_repository</localRepository>
 其中maven-repository为本地仓库  
  4. 配置镜像  找到<mirror>   </mirror>在其中添加内地镜像即可

 ```
 
     | this mirror serves has an ID that matches the mirrorOf element of this mirror. IDs are used
     | for inheritance and direct lookup purposes, and must be unique across the set of mirrors.
     |
  -->
    <mirror>
      <id>alimaven</id>
      <mirrorOf>central</mirrorOf>
      <name>aliyun maven</name>
      <url>http://maven.aliyun.com/nexus/content/repositories/central/</url>
    </mirror>
  
  </mirrors>

  <!-- profiles
   | This is a list of profiles which can be activated in a variety of ways, and which can modify
 ```

 大概就是上面的这个位置  把源添加进去就可以了  

 ---

### 在idea中配置maven 

	首先进入设置(setting)中 选择架构工具 (stru...) 中的Maven

	![设置maven](https://github.com/shenxixi250/photo/blob/master/idea_photo/idea_maven/%E9%80%89%E5%8C%BA_015.png) 
    在进入 maven中的 importing 中进行选择

	![maven设置](https://github.com/shenxixi250/photo/blob/master/idea_photo/idea_maven/%E9%80%89%E5%8C%BA_016.png) 
	更新远程或者本地库 

	![更新库](https://github.com/shenxixi250/photo/blob/master/idea_photo/idea_maven/%E9%80%89%E5%8C%BA_017.png) 



### 如何搭建一个maven项目
   创建一个maven项目  首先就是New project>>>> Maven 
   ![创建maven](https://github.com/shenxixi250/photo/blob/master/idea_photo/idea_maven/%E9%80%89%E5%8C%BA_018.png) 
   ![创建库名称](https://github.com/shenxixi250/photo/blob/master/idea_photo/idea_maven/%E9%80%89%E5%8C%BA_019.png)
   ![选择maven配置](https://github.com/shenxixi250/photo/blob/master/idea_photo/idea_maven/%E9%80%89%E5%8C%BA_020.png) 
   ![项目名和位置](https://github.com/shenxixi250/photo/blob/master/idea_photo/idea_maven/%E9%80%89%E5%8C%BA_021.png) 
这一步之后一个maven项目的框架就已经出来了 我们接下来还要做一下 文件的添加


#####创建必要的文件夹

在main下创建java 和resources文件夹  
早main同级目录下创建测试目录test 同样创建文件夹 java和resources
	
   ![创建目录](https://github.com/shenxixi250/photo/blob/master/idea_photo/idea_maven/%E9%80%89%E5%8C%BA_023.png) 
 
   标记文件目录
   ![标记文件](https://github.com/shenxixi250/photo/blob/master/idea_photo/idea_maven/%E9%80%89%E5%8C%BA_022.png) 

   添加jar包依赖
   ![jar包](https://github.com/shenxixi250/photo/blob/master/idea_photo/idea_maven/%E9%80%89%E5%8C%BA_024.png) 

   刷新jar包依赖
   ![刷新依赖](https://github.com/shenxixi250/photo/blob/master/idea_photo/idea_maven/%E5%B7%A5%E5%85%B7%E6%8F%90%E7%A4%BA_014.png) 


   ok一个maven项目完成  可以在test文件夹下创建一个简单的helloworld来运行

   ```
class HelloWorld 
{
public static void main(string[] args)
	{
	System.out.println("hello maven");
	}

}
   ```

   <++>

	

  

 <A name="cjd"> 常见的视图 </A> 

 view下的toolbar和tool(工具栏) buttons(工具按钮) 这两个选项
 也就是调出常见的工具栏  就是上面文字下面那几行
 ![工具栏](https://github.com/shenxixi250/photo/blob/master/idea_photo/1.png) 
工具按钮是侧面的 
![侧边工具栏](https://github.com/shenxixi250/photo/blob/master/idea_photo/2.png) 
下面就是一个idea中各个选项的中的展开图
![全面图](https://github.com/shenxixi250/photo/blob/master/idea_photo/idea_qjt.png) 




​	
<A name="xmd"> 项目的配置 </A> 


file(文件) ---> Project Structure  然后会进入项目的选项框了

<A name="xnm"> 项目名称 </A> 

进入项目配置框后 在Project中 找Project name 即可

<A name="jdk"> jdk </A> 

进入项目配置框后 在Project中 找Project SDK就可以选择项目运行的jdk了

<A name="byj"> 编译级别 </A> 


进入项目配置框后 在Project中 找Project language level 就可以了

<A name="cla"> class输出路径 </A> 

进入项目配置框后 在Project中 找Project compiler output 然后就可以先选择class的输出路径了

<A NAME="tjj">添加jar包</A>

 


<A NAME="cyd1">idea常用的配置</A> 

在file(文件)--> Settings 进入idea的配置框中

<A name="zt1"> 主题 </A> 

idea的配置框中 点击 Appearance-->theme 默认就只有两个主题  也可以选择自己喜欢的主题 方法[传送门](https://blog.csdn.net/simple_the_best/article/details/46941787) 

<A name="zt2"> 字体 </A> 

idea的配置框中 点击Appearance-->font 可以设置字体的大小和类型
字体的大小还可以通过在idea的配置框中 Editor-->General  在mouse选项中勾选 Change font size with Ctrl+ Mouse Wheel 也就是按住ctrl 来用鼠标的滑轮进行控制


+ <A name="zsd"> 注释的字体颜色 </A> 

在idea的配置框中 Editor-->color Scheme-->language Defaults选择即可

+ Doc Comment – Text:修改文档注释的字体颜色
+ Block comment:修改多行注释的字体颜色
+ Line comment:修改当行注释的字体颜色

<A name="zdd"> 自动导包的功能 </A> 

在idea的配置框中 Editor-->General-->Auto Import 中    
 + 在Inset Import on paste: 选择all
 + ass unambiguous imports on the fly 这个选项前面打上对勾  :作用是自动导入不明确的结构
 - Oprimize imports on the Fly (for current project) 的选项前打上勾 :自动帮我们导入优化的包

<A name="hhd"> 行号和方法间的分割符 </A> 

+ 行号是 在idea的配置框中 Editor --> General-->appearance中   勾选show line number
+ 方法间隔符 在idea的配置框中 Editor --> General-->appearance中   勾选show menthod separators


<A name="hld"> 忽略大小写的提示功能 </A> 

在 在idea的配置框中 Editor --> General-->appearance中   选择None即可

+ IntelliJ IDEA 的代码提示和补充功能有一个特性:区分大小写。如上图标注所
示,默认就是 First letter 区分大小写的。

+  区分大小写的情况是这样的:比如我们在 Java 代码文件中输入 stringBuffer,
IntelliJ IDEA 默认是不会帮我们提示或是代码补充的,但是如果我们输入
StringBuffer 就可以进行代码提示和补充。

+  如果想不区分大小写的话,改为 None 选项即可

<A name="ssq"> 设置取消单行显示tabs的操作 </A> 

 在idea的配置框中 Editor --> General--> Editor tabs中 勾选 Show tab in single now 

在打开很多文件的时候,IntelliJ IDEA 默认是把所有打开的文
件名 Tab 单行显示的。但是我个人现在的习惯是使用多行,多行效率比单行高,
因为单行会隐藏超过界面部分 Tab,这样找文件不方便


<A name="xgt"> 修改头文档的注释信息 </A> 

![头文件注释](https://github.com/shenxixi250/photo/blob/master/idea_photo/10.png) 

	​```

/**

@author shkstart  
@create ${YEAR}-${MONTH}-${DAY} ${TIME}


*/
​	


​	
	​```
-这个是官网给出的一些 头文件中的预设变量 
- ${PACKAGE_NAME} - the name of the target package where the new class or interface will be created.
- ${PROJECT_NAME} - the name of the current project.
- ${FILE_NAME} - the name of the PHP file that will be created.
- ${NAME} - the name of the new file which you specify in the New File dialog box during the file creation.
- ${USER} - the login name of the current user.
- ${DATE} - the current system date.
- ${TIME} - the current system time.
- ${YEAR} - the current year.
- ${MONTH} - the current month.
- ${DAY} - the current day of the month.
- ${HOUR} - the current hour.
- ${MINUTE} - the current minute.
- ${PRODUCT_NAME} - the name of the IDE in which the file will be created.
- ${MONTH_NAME_SHORT} - the first 3 letters of the month name. Example: Jan, Feb, etc.
- ${MONTH_NAME_FULL} - full name of a month. Example: January, February, etc.

<A name="xmd"> 项目的文件编码 </A> 

 在idea的配置框中 Editor --> Code Style-->File ENcodeing中进行操作
​	
 说明:Transparent native-to-ascii conversion 主要用于转换 ascii,一般都要勾选,
不然 Properties 文件中的注释显示的都不会是中文。

<A name="szd"> 设置自动编译 </A> 

 在idea的配置框中 Editor --> Compiler 中勾选 Build project automeatically 和 Compile independent modules in parallel

+ 构建就是以我们编写的 java 代码、框架配置文件、国际化等其他资源文件、
JSP 页面和图片等资源作为“原材料”,去“生产”出一个可以运行的项目的
过程。
+ Intellij Idea 默认状态为不自动编译状态,Eclipse 默认为自动编译:
很多朋友都是从 Eclipse 转到 Intellij 的,这常常
导致我们在需要操作 class 文件时忘记对修改后
的 java 类文件进行重新编译,从而对旧文件进
行了操作。

<A name="rhs"> vim_idea </A> 
这个先挖一个坑




<A name="deb"> debug </A> 


<A name="jav"> javadoc </A> 
<A name="cj1"> 插件 </A> 


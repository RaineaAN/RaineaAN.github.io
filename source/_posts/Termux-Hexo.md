---
title: Termux/Linux搭建Hexo博客
date: 2021-08-17 09:57:45
tags: [Hexo,Termux,Linux]
cover: https://hennessey02.coding.net/p/Pic/d/Pic01/git/raw/master/Blog-img/20220101//Termux.png
top_img: https://121.40.96.38:8005/i/2024/07/669f5807e2ff8.jpg
hide: false
---

## **Hexo简介**


Hexo是一款基于Node.js的静态博客框架，依赖少易于安装使用，可以方便的生成静态网页托管在GitHub和Gitee上，是搭建博客的首选框架。<!-- more -->大家可以进入hexo官网进行详细查看，因为Hexo的创建者是台湾人，对中文的支持很友好，可以选择中文进行查看


## **安装Git**


Git是目前世界上最先进的分布式版本控制系统，可以有效、高速的处理从很小到非常大的项目版本管理



```
apt-get install git -y
```


## **安装nodejs**


Hexo是基于nodeJS编写的，所以需要安装一下nodeJs和里面的npm工具



```
apt-get install nodejs npm -y
```

安装完后，输入命令



```
node -v

npm -v
```

检查是否安装成功

更换npm源为淘宝源

```
npm config set registry https://registry.npm.taobao.org
```


## **安装hexo**


前面git和nodejs安装好后，就可以安装hexo了，先创建一个文件夹filename，然后cd到这个文件夹下

输入命令

```
npm install -g hexo-cli

hexo -v   #查看版本信息
```

![](https://linuecs.files.wordpress.com/2020/08/screenshot_2020_0801_1425592747878800930944621.png)


## **初始化hexo**




```
hexo init filename(文件名随意定义)

cd filename //进入这个文件夹

npm install
```

- cd <folder> #说明：将操作位置转移到将要存放项目的文件夹目录（便于区分，我的项目文件夹名为hexo,~/root/hexo以下将使用这个文件夹）
- hexo init #说明：自动在文件夹（hexo1）中创建项目所需的文件
- npm install #说明：安装依赖包
- hexo generate #说明：构建，会在hexo1中创建public文件夹
  执行完以上命令后，会多出以下文件和文件夹

例如



![](https://linuecs.files.wordpress.com/2020/08/img_20200803_1018077824263297184815366.jpg)



新建完成后，指定文件夹目录下有：

- _config.yml：站点的配置文件，需要备份
- themes：主题文件夹，需要备份
- source：博客文章的 .md 文件，需要备份
- scaffolds：文章的模板，需要备份
- package.json：安装包的名称，需要备份
- .gitignore：限定在 push 时哪些文件可以忽略，需要备份
- .git：主题和站点都有，标志这是一个 git 项目，不需要备份
- node_modules：是安装包的目录，在执行 npm install 的时候会重新生成，不需要备份
- public：是 hexo g 生成的静态网页，不需要备份
- .deploy_git：同上，hexo g 也会生成，不需要备份
- db.json：文件，不需要备份



![](https://linuecs.files.wordpress.com/2020/08/screenshot_2020_0801_1430267700908023566336224.png)



输入命令



```
hexo g
```



![](https://linuecs.files.wordpress.com/2020/08/screenshot_2020_0801_1426494387056801777394283.png)



输入命令

```
hexo s
```

![](https://linuecs.files.wordpress.com/2020/08/screenshot_2020_0801_1427121834223231530076486.png)



打开hexo的服务

在浏览器输入



```
**http://localhost:4000**
```



就可以看到你生成的博客



![](https://linuecs.files.wordpress.com/2020/08/screenshot_2020_0801_1435241192715661277456756.png)



**使用ctrl+c停止服务**



## **Hexo+Github**





## **GitHub创建个人仓库**



注册登录[github官网](http://github.com/)，点击右上角加号，点击New repository，新建仓库



![img](https://linuecs.files.wordpress.com/2020/08/screenshot_2020_0801_1453048826363041159371369.png)



创建一个和用户名相同的仓库,即http://xxxx.github.io，其中xxx是github的用户名



![](https://linuecs.files.wordpress.com/2020/08/screenshot_2020_0801_145655625734147419220357.png)



点击create repository



### **Git初始化设置**

输入命令

```
git config --global user.name "yourname" 

git config --global user.email "youremail"
```

(yourname是github用户名，youremail是注册github的邮箱)



```
git config user.name

git config user.email
```

检查是否正确，输入命令



### **生成SSH添加到GitHub**


输入命令，创建SSH,一路回车



```
ssh-keygen -t rsa -C "youremail"
```



![](https://linuecs.files.wordpress.com/2020/08/img_20200802_1139583858709568397913356.jpg)



查看SSH KEY，输入命令



```
cat ~/.ssh/id_rsa.pub
```

复制id_rsa.pub里面的全部内容



![](https://linuecs.files.wordpress.com/2020/08/img_20200803_0950183625923031218189922.jpg)



在github的setting中，找到SSH keys的设置选项，点击New SSH key，粘贴id_rsa.pub里面的全部内容



![](https://linuecs.files.wordpress.com/2020/08/screenshot_2020_0801_151404755358037895170688.png)



输入命令

```
ssh -T git@github.com
```

查看是否连接成功



![](https://linuecs.files.wordpress.com/2020/08/img_20200803_0950366233783924410194530.jpg)



打开站点配置文件 _config.yml，修改添加以下内容



```
deploy:
  type: git
  repo:
git@github.com:yourgithubname/yourgithubname.github.io.git
  branch: master
```

安装deploy-git ，也就是部署的命令,这样才能用命令部署到github



```
npm install hexo-deployer-git --save
```

输入命令



```
hexo clean 第一次安装不用清缓存

hexo clean &&　hexo g -d 　缩写

hexo g = hexo generate 生成静态文件

hexo generate -deploy 生成静态文件后立即部署网站
```

打开下面的网址



```
**http://yourname.github.io**
```



就可看到和



```
**http://localhost:4000**
```



一样的了！



## **关联Git仓库**


```
git clone https://github.com/你的用户名/你的用户名.github.io.git
```

执行之后会在当前目录生成'你的用户名.github.io'的文件夹，这是关联github仓库的文件夹，需要上传的文件都会移动到这里

更多精彩内容请点击[**hexo官网**](https://hexo.io/zh-cn/docs/)docs/)
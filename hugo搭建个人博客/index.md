# Hugo搭建个人博客




# hugo搭建个人博客

## 1. 安装Hugo

### 1.1 下载

在[hugo release](https://github.com/gohugoio/hugo/releases)界面下载对应的操作系统版本的Hugo二进制文件（Hugo或者Hugo.exe）。

或者

Mac下可直接使用Homebrew安装

```sh
brew install hugo
```

### 1.2 设置环境变量

```sh
vi ~/.bash_profile
```

## 2. 生成站点

Hugo提供了`new`命令来创建一个新的网站：

```sh
hugo new site mysite
```

## 3. 安装主题

Lovelt主题的仓库是：https://github.com/dillonzq/LoveIt.git

可以下载主题zip文件并解压到themes目录下

也可以

直接把主题Lovelt克隆到themes目录下；

```sh
cd mysite/themes
git clone https://github.com/dillonzq/LoveIt.git
```

## 4. 创建文章

```sh
hugo new posts/first_post.md
```

>默认情况下, 所有文章和页面均作为草稿创建. 如果想要渲染这些页面, 请从元数据中删除属性 `draft: true`, 设置属性 `draft: false` 或者为 `hugo` 命令添加 `-D`/`--buildDrafts` 参数.



## 5. 本地启动网站

```sh
hugo serve
```

查看`http://localhost:1313`.

## 6. 部署到GitHub

### 6.1 创建github仓库

> Head over to [GitHub](https://github.com/) and [create a new public repository](https://github.com/new) named *username*.github.io, where *username* is your username (or organization name) on GitHub.

参考[github pages](https://pages.github.com/)

### 6.2 运行hugo

```sh
hugo --baseURL="https://nyutopia.github.io/"
```

会生成一个 `public` 目录, 其中包含你网站的所有静态内容和资源. 现在可以将其部署在任何 Web 服务器上.

```sh
cd public
git init
git add .
git commit -m "first push"
git remote add origin git@github.com:nyutopia/nyutopia.github.io.git
git push -u origin master
```



## 7. 部署到gitee

[gitee静态页面托管](https://gitee.com/help/articles/4136#article-header0)

> 1. 如何创建一个首页访问地址不带二级目录的 pages，如ipvb.gitee.io？
>
>    答：如果你想你的 pages 首页访问地址不带二级目录，如ipvb.gitee.io，**你需要建立一个与自己个性地址同名的仓库**，如 https://gitee.com/ipvb 这个用户，想要创建一个自己的站点，但不想以子目录的方式访问，想以`ipvb.gitee.io`直接访问，那么他就可以创建一个名字为`ipvb`的仓库 https://gitee.com/ipvb/ipvb 部署完成后，就可以以 [https://ipvb.gitee.io](https://ipvb.gitee.io/) 进行访问了。

![图片1](/typoraIMG/hugo搭建个人博客.assets/image-20210628200037954.png)



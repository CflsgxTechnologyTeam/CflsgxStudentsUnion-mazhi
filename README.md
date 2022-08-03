
# 这是一个为成都外国语学校高新校区校团委学生会创建的项目  
校团学会官网项目由第五届校团委宣传部部长![Gloridust](https://github.com/Gloridust)创办，![原项目仓库](https://github.com/Gloridust/cflsgx.top)已停用.原项目文章发布属于是纯手写HTML，非常繁杂不适用于长期运营。考虑到WordPress等服务器运营成本高，为了方便长远运营最终选择了MarkDown+Jekyll+GithubPage+Vercel+CloudFlare的方式实现。  


# 相关配置

1. 正确设置项目名称与分支。

   按照 GitHub Pages 的规定，名称为 `username.github.io` 的项目的 master 分支，或者其它名称的项目的 gh-pages 分支可以自动生成 GitHub Pages 页面。

2. 修改域名。

   如果你需要绑定自己的域名，那么修改 CNAME 文件的内容，并参考 [配置 GitHub Pages 站点的自定义域](https://docs.github.com/cn/pages/configuring-a-custom-domain-for-your-github-pages-site) 做好配置；如果不需要绑定自己的域名，那么删掉 CNAME 文件。

3. 修改配置。

   网站的配置基本都集中在 \_config.yml 文件中，将其中与个人信息相关的部分替换成你自己的，比如网站的 url、title、subtitle 和第三方评论模块的配置等。

   **评论模块：** 目前支持 disqus、gitment、gitalk、utterances 和 beaudar，选用其中一种就可以了，推荐使用 beaudar。它们各自的官方配置指南链接在 \_config.yml 文件的 Comments 一节里都贴出来了，请参考官方指南配置。

   **注意：** 如果使用 disqus，因为 disqus 处理用户名与域名白名单的策略存在缺陷，请一定将 disqus.username 修改成你自己的，否则请将该字段留空。我对该缺陷的记录见 [Issues#2][3]。

4. 放置文章与图片。

   如下文件夹中除了 template.md 文件外，都可以全部删除，然后添加你自己的内容。

   * \_posts 文件夹中是已发布的博客文章。
   * \_drafts 文件夹中是尚未发布的博客文章。
   * images 文件夹中是文章和页面里使用的图片。
   
5. 修改二维码图片
   
   _config.yml 里的 components.qrcode 这一段用于控制二维码。

   不显示二维码：将 components.qrcode.enabled 改为 false。

   替换二维码图片：替换 assets/images/qrcode.jpg 文件。

6. 目录下的 yml 文件内容含义

pages/about.md 文件内容对应网站的「关于」页面，里面的内容多为个人相关，将它们替换成你自己的信息，包括 \_data 目录下的 skills.yml 和 social.yml 文件里的数据。

*skills.yml* 文件里的内容对应[「关于」][1]页面里的 Skill Keywords。

![](/images/posts/template/skills.yml.png)

*social.yml* 文件里的内容对应[「关于」][1]页面里的「联系」里的内容。

![](/images/posts/template/social.yml.png)

*links.yml* 文件里的内容对应[「链接」][2]页面里的内容。

![](/images/posts/template/links.yml.png)


## 使用文档

- [本博客模板常见问题 Q & A](https://mazhuang.org/2020/05/03/blog-template-qna/)。

- 在本地预览博客效果可以参考 [Setting up your Pages site locally with Jekyll]。

- 稿件采用MarkDown语法，具体格式参照![菜鸟教程](https://www.runoob.com/markdown/md-title.html)  

- ## 文档编辑

头部信息实例如下：  
```txt
---
layout: post
title: 本文标题
categories: 分类归档
description: 这里填写文章概要描述
keywords: 关键词, 关键词
topmost: true

---
```

## 经验与思考

* 排版建议遵照一定的规范，推荐 [中文文案排版指北（简体中文版）]。

* 简约，尽量每个页面都不展示多余的内容。

* 有时一图抵千言，有时可能只会拖慢网页加载速度。

* 言之有物，不做无痛之呻吟。

* 如果写技术文章，那先将技术原理完全理清了再开始写，一边摸索技术一边组织文章效率较低。

* 杜绝难断句、难理解的长句子，如果不能将其拆分成几个简洁的短句，说明脑中的理解并不清晰。

* 可以学习一下那些高质量的博主，他们的行文，内容组织方式，有什么值得借鉴的地方。


## 致谢

本系统修改自项目[码志](https://github.com/mzlogin/mzlogin.github.io)，谢谢原作者提供的开源项目！
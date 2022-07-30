# cos的博客

Hexo + Shoka主题 + vercel搭建的属于自己的博客站点

**所有博客如果遇到问题、文章错漏可以直接issue反馈**

通过 vercel 部署，强烈安利 vercel！个人版一个月 100G 流量，小站点完全够用~

用Markdown写文章的感觉并且集中真的超级棒！

## 我也想整一个自己的博客？

前提：注册一个github账户和vercel账号

直接 fork 这个仓库然后 vercel 中导入，直接部署，然后就可以清空source文件夹下我的博客，变成自己的啦

当然，默认的是 [shoka 主题](https://github.com/amehime/hexo-theme-shoka)，如果想要改成别的去看看 hexo 的教程以及下面这些就懂了~

### 一些教程
- 用vercel部署 -> [如何使用 vercel + hexo 搭建博客](https://zhuanlan.zhihu.com/p/342790013)
- 不想用vercel？ -> [Hexo + GitPage 搭建个人博客](https://www.jianshu.com/p/d9dff0bf5da5)
- shoka主题官方教程 -> [Hexo 主题 Shoka 使用说明](https://shoka.lostyu.me/computer-science/note/theme-shoka-doc/)
    - [**🚀快速开始**](https://shoka.lostyu.me/computer-science/note/theme-shoka-doc/) -> [💌依赖插件](https://shoka.lostyu.me/computer-science/note/theme-shoka-doc/dependents/) -> [📌基本配置](https://shoka.lostyu.me/computer-science/note/theme-shoka-doc/config/) -> [🌈界面显示](https://shoka.lostyu.me/computer-science/note/theme-shoka-doc/display/) -> [🦄特殊功能](https://shoka.lostyu.me/computer-science/note/theme-shoka-doc/special/)
- 关于shoka主题我自己总结的一篇配置记录: [Hexo 博客 Shoka 主题配置记录](https://ysx.cosine.ren/hexo-shoka-config/)
## 目录说明
```
cos_blogs
├─ package.json
├─ README.md
├─ scaffolds    存放生成草稿/文章/页面基础模板
│  ├─ draft.md
│  ├─ page.md
│  └─ post.md
├─ source
│  ├─ about     关于我的页面
│  ├─ friends   友链页面
│  ├─ img       静态图片资源：文章首图等
│  ├─ musics    歌单页面
│  ├─ _data     翻译文件，用于翻译文章
│  │  └─ languages.yml     自定义菜单等处显示的文字
│  ├─ _drafts   草稿文章 不会发布
│  └─ _posts    已发布的文章
├─ themes  主题目录
│  └─ shoka     shoka主题
│     ├─ languages     语言
│     ├─ layout        一些HTML模板等
│     ├─ source        主题源码
│     └─ _images.yml   随机图库列表
├─ yarn.lock
├─ _config.shoka.yml     shoka主题相关配置
└─ _config.yml           hexo相关配置文件
```
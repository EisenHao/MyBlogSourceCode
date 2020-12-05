# MyBlogSourceCode
我的博客源码

* 本博客采用[Hexo](https://hexo.io/zh-cn/docs/)博客框架
* 本博客主题为[NexT v8.1.0](https://github.com/next-theme/hexo-theme-next)

## 依赖
* [Node.js](http://nodejs.org/)
* [Git](http://git-scm.com/)
* [Hexo](https://hexo.io/zh-cn/)

## 安装依赖 npm 组件
```shell
cd $YOUR_BLOG_SITE_DIR

# Symbols count and time to read for articles in Hexo blog (后期移除)
npm install hexo-word-counter

# A hexo plugin that generates a list of links to related posts or popular posts.
npm install hexo-related-popular-posts --save

# Highly performant, light and configurable lazy loader in pure JS with no dependencies for images, iframes and more, using IntersectionObserver API
npm install --save lozad

# Server side pangu.js filter for Hexo. (安装失败)
npm install hexo-pangu

# Automatically insert blank space between all Chinese characters and semi form English, numbers and symbols in the web page
npm install pangu --save

# automatically prefetch URLs for links that are in-viewport during idle time.
npm install --save quicklink

# A plugin to fix a serious security bug in leancloud visitor counter for NexT theme site and other site that integrated this function using a similar way.
npm install hexo-leancloud-counter-security

# generating a search index file, which contains all the necessary data of your articles that you can use to write a local search engine for your blog
npm install hexo-generator-searchdb

npm install hexo-deployer-git --save
npm install hexo-tag-dplayer --save
npm install --save hexo-tag-aplayer

```

## 建站流程
```shell 
# 建站
hexo init eisenhao.github.io
cd eisenhao.github.io
npm install

# 获取 NexT 主题
mkdir themes/next
# 下载最新 Release tar包
cd themes/next
curl -o next.tar.gz --insecure https://codeload.github.com/next-theme/hexo-theme-next/tar.gz/v8.1.0
# 解压
tar -zxf next.tar.gz
# 重命名文件夹为 next
mv hexo-theme-next-8.1.0 next
cd ../../

# 修改 Hexo 配置文件
vi ./_config.yml

# 修改 NexT 配置文件
vi ./themes/next/_config.yml

# 为博客添加文章
# ...

# 构建静态博客网站
hexo Clean && hexo g

# 本地调试（http://localhost:4000）
hexo s

# 发布
hexo d
```
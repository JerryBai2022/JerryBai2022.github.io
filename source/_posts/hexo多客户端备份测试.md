---
title: hexo多客户端备份测试
date: 2023-05-01 23:22:06
tags: 配置
categories:
- 环境配置
---

# hexo多客户端备份
hexo环境打包到github，新客户端执行以下步骤即可开始hexo文章编辑：
1. git clone -b hexo git@xxx.github.com hexo
2. 安装环境包：
```
npm install hexo
npm install hexo-cli -g
npm install
npm install hexo-deployer-git
```
注意这一步不需要执行`hexo init`，否则会重置远端部署信息
3. 通过命令`hexo g`和`hexo s`在本地开启同步下来的静态博客页面
4. 提交步骤
```
git add .
git commit -m "修改说明"
git push origin hexo
hexo g -d
```

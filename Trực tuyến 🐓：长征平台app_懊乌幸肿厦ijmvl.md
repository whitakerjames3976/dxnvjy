长征平台app【Q-——333307——】长征平台app【 辋芷《888yx●vip》 】
长征平台app【Q-——333307——】长征平台app【 辋芷《888yx●vip》 】

 如何用 GitHub Actions 自动部署静态博客？新手也能轻松上手

你是不是也在 GitHub 上托管了自己的博客或个人网站？每次写完文章，还要手动执行构建命令、上传文件，甚至担心服务器配置出错。其实，GitHub Actions 能帮你把这套流程自动化，真正做到“push 代码，自动上线”。

今天这篇教程，我会直接带你从零配置一个最常用的部署流程，适合新手，也可以直接复制使用。整个过程分三步，不需要额外服务器，免费额度也足够个人使用。

 第一步：创建 GitHub Actions 工作流文件

在你的仓库里新建一个目录 `.github/workflows/`，然后添加一个文件，比如叫 `deploy.yml`。

这个文件就是告诉 GitHub：什么时候触发任务，跑哪些步骤。最常见的触发方式就是 `push` 到主分支。

 第二步：填写基础的部署配置

下面是一个核心示例，我加了详细注释，方便你按需修改：

```yaml
name: Deploy   工作流名称，可自定义

on:
  push:
    branches: [ main ]   当 main 分支收到 push 时触发

jobs:
  build-and-deploy:
    runs-on: ubuntu-latest
    steps:
      - name: 拉取最新代码
        uses: actions/checkout@v4

      - name: 部署到目标服务器或分支
        run: |
           这里写你自己的构建和部署命令
           例如：npm install && npm run build
```

如果你使用的是常见框架，可以额外加上对应的构建步骤（比如 Node.js 环境配置）。注意：如果你需要将部署文件推送到另一个仓库或分支，记得在 GitHub 仓库设置里配置 `secrets`（密钥），避免明文暴露密码。

 第三步：推送代码并查看运行状态

将写好的文件提交并推送到 GitHub，然后进入仓库首页的 Actions 标签页。你会看到一个名为 “Deploy” 的工作流正在运行。点击进去就能看到每一步的实时日志，如果某个步骤报错，日志里会直接显示错误原因，方便排查。

一般 1-2 分钟就能跑完。看到绿色对号，说明部署成功。

 一些实用的进阶技巧

如果你不满足于最基础的部署，我强烈建议试一下这两个个用法：

1. 使用现成的第三方 Action：比如 `peaceiris/actions-gh-pages`，它专用于 GitHub Pages 部署，只需要写几行配置，不用自己记命令。
2. 定时触发：把 `on` 部分改成 `schedule`，可以设定每天定时更新某个数据源或自动迁移缓存。

> 小互动：你目前是在用静态站点生成器（如 Hugo、VuePress）吗？你部署时遇到的最大痛点是什么？欢迎在评论区写下你卡住的环节，我会挑高频问题单独写一篇解决贴。

 总结与搜索提示

总结一下，利用 GitHub Actions 自动部署有三个核心关键词供你搜索：工作流触发（workflow triggers）、Actions 版本选择（actions checkout）、仓库密钥配置（repository secrets）。如果你打算长期使用，建议再搜索一下 自托管 runner，能大幅提升构建速度。

如果这篇文章对你有帮助，欢迎收藏或转发给你身边正在折腾博客的朋友。点击关注，我会持续更新更多 GitHub 高性价比实战教程。

相关推荐：

https://github.com/whitakerjames3976/dxnvjy/blob/main/C%E1%BB%91c%20Games%20%F0%9F%A5%8A%EF%BC%9A%E9%95%BF%E5%BE%81%E6%B3%A8%E5%86%8C_%E6%80%82%E4%BB%93%E6%85%95%E5%80%8C%E9%98%9Fflxxx.md

<img src="https://i.postimg.cc/TYyY6mPw/changzheng1-00005.png" />

相关推荐：

https://github.com/whitakerjames3976/dxnvjy/commit/f2bed08c50edd78685ed8bded86d8d9080b24329

<img src="https://i.postimg.cc/3Nq8GrtN/changzheng1-00001.png" />
相关推荐：

https://github.com/wellsjoseph501/owmunv/blob/main/Th%E1%BB%83%20thao%20%E2%9A%BD%EF%B8%8F%EF%BC%9A%E9%95%BF%E5%BE%81%E5%AE%98%E7%BD%91_%E8%A1%99%E6%94%98%E5%90%9E%E5%AF%B9%E8%B0%A2zgfnn.md

<img src="https://i.postimg.cc/W4V2gHww/changzheng1-00013.png" />
相关推荐：

https://github.com/wellsjoseph501/owmunv/commit/6562dfd043fe7fbd63cdf975f0c1e8aad589474b

<img src="https://i.postimg.cc/7hRHzPKT/changzheng1-00002.png" />

资讯来源：新华网、人民网、央视新闻、中新网、凤凰网、澎湃新闻、界面新闻、新浪新闻、搜狐网、财新网、观察者网、第一财经等主流平台，以独树一帜的观察视角与扎实的深度报道能力，在资讯领域收获广泛关注。


# 中文版本

# 学术页面模板
**Academic Pages 是一个基于 GitHub Pages 的学术网站模板。**

![学术页面模板示例](screenshot.jpg "学术页面模板示例")

# 快速开始

1. 注册 GitHub 账户并验证邮箱（必需步骤）
1. 点击右上角 "Use this template" 按钮
1. 在新建仓库页面，输入仓库名为 "[你的GitHub用户名].github.io"，这将成为你的网站地址
1. 配置全局设置并添加内容
1. 上传文件（如PDF、压缩包等）至 `files/` 目录，可通过 https://[你的GitHub用户名].github.io/files/示例.pdf 访问
1. 在仓库设置的 "GitHub pages" 版块查看部署状态
1. （可选）使用 `markdown_generator` 目录中的 Jupyter notebook 或 Python 脚本，通过TSV文件自动生成出版物和演讲的Markdown文件

## 📖 详细教程

如果你希望按照更详细的图文步骤来搭建自己的学术主页，请参考我在 CSDN 上发布的完整教程：

👉 [**DIY搭建网站（学术个人介绍主页）**](https://blog.csdn.net/qq_63129682/article/details/144175266)

该教程涵盖了从创建仓库、修改内容到 GitHub Pages 部署的全过程。

更多信息请访问：https://academicpages.github.io/

## 本地运行

开发网站时，建议先在本地预览修改内容再推送到GitHub。本地运行需要：

1. 克隆仓库并进行上述修改
1. 确保已安装 ruby-dev、bundler 和 nodejs
    
    Linux系统及[WSL](https://learn.microsoft.com/en-us/windows/wsl/about)安装命令：
    ```bash
    sudo apt install ruby-dev ruby-bundler nodejs
    ```
    MacOS安装命令：
    ```bash
    brew install ruby
    brew install node
    gem install bundler
    ```
1. 运行 `bundle install` 安装Ruby依赖。若报错可删除 Gemfile.lock 后重试
1. 执行 `jekyll serve -l -H localhost` 生成HTML并通过`localhost:4000`提供服务，本地服务器会自动重建页面并实时刷新

Linux系统可能需要额外安装依赖：`sudo apt install build-essential gcc make`

## 使用Docker

使用不同操作系统或不想安装依赖？可通过提供的`Dockerfile`构建容器（需先安装[Docker](https://www.docker.com/)）。

首先构建容器：
```bash
docker build -t jekyll-site .
```
然后运行容器：
```bash
docker run -p 4000:4000 --rm -v $(pwd):/usr/src/app jekyll-site
```

## 维护说明
模板的bug反馈和功能请求请通过GitHub提交。样式问题欢迎发起GitHub讨论。

本仓库由Stuart Geiger从Minimal Mistakes Jekyll主题fork并独立，原主题© 2016 Michael Rose，采用MIT许可证（见LICENSE.md）。当前由Robert Zupko维护，欢迎更多维护者加入。

## 提交改进
如需提交pull request修复bug或增强功能，需先fork仓库（而非直接使用模板）。这样可同步更新你的fork版本。

需要注意的是，此类模板主题在同步核心更新时容易产生冲突。如果已进行自定义配置，建议保存.yml配置文件和markdown文件后重新fork，或手动合并更改。

---

# ENGLISH TYPE

# Academic Pages
**Academic Pages is a Github Pages template for academic websites.**

![Academic Pages template example](screenshot.jpg "Academic Pages template example")

# Getting Started

1. Register a GitHub account if you don't have one and confirm your e-mail (required!)
1. Click the "Use this template" button in the top right.
1. On the "New repository" page, enter your repository name as "[your GitHub username].github.io", which will also be your website's URL.
1. Set site-wide configuration and add your content.
1. Upload any files (like PDFs, .zip files, etc.) to the `files/` directory. They will appear at https://[your GitHub username].github.io/files/example.pdf.
1. Check status by going to the repository settings, in the "GitHub pages" section
1. (Optional) Use the Jupyter notebooks or python scripts in the `markdown_generator` folder to generate markdown files for publications and talks from a TSV file.

## 📖 Detailed Tutorial

For a complete step-by-step guide on how to use this template to build your own academic homepage, please refer to my tutorial on CSDN:

👉 [**DIY搭建网站（学术个人介绍主页）**](https://blog.csdn.net/qq_63129682/article/details/144175266)

This tutorial covers everything from creating the repository, customizing content, to deploying with GitHub Pages.

See more info at https://academicpages.github.io/

## Running locally

When you are initially working your website, it is very useful to be able to preview the changes locally before pushing them to GitHub. To work locally you will need to:

1. Clone the repository and made updates as detailed above.
1. Make sure you have ruby-dev, bundler, and nodejs installed
    
    On most Linux distribution and [Windows Subsystem Linux](https://learn.microsoft.com/en-us/windows/wsl/about) the command is:
    ```bash
    sudo apt install ruby-dev ruby-bundler nodejs
    ```
    On MacOS the commands are:
    ```bash
    brew install ruby
    brew install node
    gem install bundler
    ```
1. Run `bundle install` to install ruby dependencies. If you get errors, delete Gemfile.lock and try again.
1. Run `jekyll serve -l -H localhost` to generate the HTML and serve it from `localhost:4000` the local server will automatically rebuild and refresh the pages on change.

If you are running on Linux it may be necessary to install some additional dependencies prior to being able to run locally: `sudo apt install build-essential gcc make`

## Using Docker

Working from a different OS, or just want to avoid installing dependencies? You can use the provided `Dockerfile` to build a container that will run the site for you if you have [Docker](https://www.docker.com/) installed.

Start by build the container:

```bash
docker build -t jekyll-site .
```

Next, run the container:
```bash
docker run -p 4000:4000 --rm -v $(pwd):/usr/src/app jekyll-site
```

# Maintenance

Bug reports and feature requests to the template should be [submitted via GitHub](https://github.com/academicpages/academicpages.github.io/issues/new/choose). For questions concerning how to style the template, please feel free to start a [new discussion on GitHub](https://github.com/academicpages/academicpages.github.io/discussions).

This repository was forked (then detached) by [Stuart Geiger](https://github.com/staeiou) from the [Minimal Mistakes Jekyll Theme](https://mmistakes.github.io/minimal-mistakes/), which is © 2016 Michael Rose and released under the MIT License (see LICENSE.md). It is currently being maintained by [Robert Zupko](https://github.com/rjzupkoii) and additional maintainers would be welcomed.

## Bugfixes and enhancements

If you have bugfixes and enhancements that you would like to submit as a pull request, you will need to [fork](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo) this repository as opposed to using it as a template. This will also allow you to [synchronize your copy](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/syncing-a-fork) of template to your fork as well.

Unfortunately, one logistical issue with a template theme like Academic Pages that makes it a little tricky to get bug fixes and updates to the core theme. If you use this template and customize it, you will probably get merge conflicts if you attempt to synchronize. If you want to save your various .yml configuration files and markdown files, you can delete the repository and fork it again. Or you can manually patch.

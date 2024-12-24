---
title: "How to Start Blogging with Hugo"
date: 2024-12-24
slug: how-to-start-blogging-with-hugo
category: blog
summary:
description:
cover:
  image:
  alt:
  caption:
  relative: true
showtoc: true
draft: false
---

This is my first blog post, ever. And because I've built this website by using [Hugo](https://gohugo.io/), why not starting this journey of self-learning by a blog post on how to start with amazing framework?

**Note**: _The following how-to has been tested on a Windows (10) operating system only._

### Build from Source

As mentioned in the [Hugo Windows Installation](https://gohugo.io/installation/windows/) guide, three are three main components when working with **Hugo**:

- Git
- Go
- Dart Sass

To begin with, **Git** and **Go** are mostly necessary to start with Hugo development, where **Git** plays the role of the Version Control System. It is good practice to _git_ your progress and, in case needed, revert your current work to a previous version.

Therefore:

1. Install Git: [Git Installation](https://git-scm.com/downloads/win)
2. Install Go: [Go Installation](https://go.dev/dl/)
3. Install Clang: [Clang](https://releases.llvm.org/download.html) (needed to compile any native code dependencies or tools used by **Hugo** and because we are building [Hugo from Source](https://github.com/gohugoio/hugo#build-from-source))
4. Update your `PATH` environment variable [Go Wiki: Setting GOPATH](https://go.dev/wiki/SettingGOPATH#:~:text=Click%20the%20%E2%80%9CEnvironment%20Variables%E2%80%9D%20button,the%20%E2%80%9CVariable%20value%E2%80%9D%20field.). Look for the `Windows` section.
5. Install Hugo: [Hugo Installation](https://gohugo.io/installation/windows/). It is recommended to install the _extended_ version to have all the features needed since the beginning.
   1. In short, open a CLI (I'm using [Hyper](https://hyper.is/) for Windows), and install _Hugo_ by typing/copy-pasting the following to build the _standard version_ of Hugo:
   ```sh
   CGO_ENABLED=1 go install tags extended github.com/gohugoio/hugo@latest
   ```
6. Test your installation: once done, type `hugo version` and you should see something like `hugo v0.140.0 windows/amd64 BuildDate=unknown` ([Hugo - Basic Usage](https://gohugo.io/getting-started/usage/))

In addition, follow the [detailed instructions](https://discourse.gohugo.io/t/gcc-compiler-required-to-build-hugo-from-source-on-windows/41370) to install **GCC** on Windows.

### Git it!

A possible next step is to _Git_ your folder. By _gitting_ it, you keep track of any changes you do during the development.

In order to do that, you can follow the instructions [Initializing a Git repository](https://docs.github.com/en/migrations/importing-source-code/using-the-command-line-to-import-source-code/adding-locally-hosted-code-to-github#initializing-a-git-repository).

### Starting with a Theme

Starting with a theme is the easiest way to look at a setup already done. From there, you can edit it as you wish with your own data and style.

Let's say you want to start with the most common Theme available for **Hugo**, [PaperMod](https://github.com/adityatelange/hugo-PaperMod).

1. Follow the [installation guide](https://github.com/adityatelange/hugo-PaperMod/wiki/Installation), the _recommended method 2_.
2. You can use the [Data Professor](https://github.com/dataprofessor) [config.yml](https://github.com/dataprofessor/chanin.tech/blob/main/config.yml) file to get inspiration of what he already did and then edit the available configuration settings.
   1. In case you have the **hugo.toml** file and not the **config.yml** file, you can use the [YAML TO TOML Converter](https://transform.tools/yaml-to-toml) to convert the **config.yml** file into the **hugo.toml**.
3. `cd` into your project directory and type `hugo server -D` (where the `-D` will run the _drafts_ pages as well) and go to `//localhost:1313/` to see your current locally deployed blog.
4. If everything went correctly, you should see something like the official [hugo.PaperMod Webpage](https://adityatelange.github.io/hugo-PaperMod/) with the editing from the **Data Professor** _config.yml_ file.
5. Pat yourself in the back, you now have a blog! 🎉🎊
6. To improve/edit your newly created blog, you can have a look into the official repo for more info or the following other great resources:
   1. [Hugo-PaperMod](https://github.com/adityatelange/hugo-PaperMod)
   2. [The Data Professor PaperMod Github Example](https://github.com/dataprofessor/chanin.tech/tree/main)
   3. [The Data Professor - How to build a portfolio website for data science | Hugo + Hostinger](https://www.youtube.com/watch?v=sm3IuE7zkYQ&t=722s)
   4. [How to Set Up This Blog](https://kpwn.de/2021/09/how-to-set-up-this-blog/)

### Publish your blog on gh-pages

And now, what? After you have built your own blog _locally_, you can think of showing it to the world. But how? Here, the **gh-pages** comes into _action_. Because we are not using _Jekyll_ as a SSG (Static Site Generator), the [About GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/about-github-pages#types-of-github-pages-sites) page suggests to use the **GitHub Actions** in order to publish our _Hugo_ website.

You can follow the [Host on GitHub Pages](https://gohugo.io/hosting-and-deployment/hosting-on-github/) how-to for hosting and deployment to understand what are the necessary steps to easily and freely host your own blog online.

References:

- https://gohugo.io/hosting-and-deployment/hosting-on-github/
- https://docs.github.com/en/pages/getting-started-with-github-pages/about-github-pages#types-of-github-pages-sites
- https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site
- https://medium.com/@magstherdev/github-pages-hugo-86ae6bcbadd

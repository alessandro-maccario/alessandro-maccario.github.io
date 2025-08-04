---
title: "Poetry Environments, Simplified"
date: 2025-08-03
slug: poetry-environments-simplified
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


### A one line command tool to create Poetry-Python environments
While developing more and more projects in Python by following the [100 Days of Code: The Complete Python Pro Bootcamp](https://shorturl.at/JpasI), I've found myself creating new Poetry environments for each and every one of them. I used to keep an [Obsidian](https://obsidian.md/) note open whenever I had to create a new one with a series of steps to follow, to speed up the process.
But why the need of manually typing each and every command in the terminal if it is possible to package them in a Python script?

That is why I've decided to create my own [Poetry-Python environment creation tool](https://github.com/alessandro-maccario/poetry-cli-app): a very simple Python script that packages those needed commands in order to create a Poetry environment by using only one command through the terminal.

### How does it work?
Head to [Poetry-Python environment creation tool](https://github.com/alessandro-maccario/poetry-cli-app) GitHub page and follow the [Readme.md](https://github.com/alessandro-maccario/poetry-cli-app/blob/master/README.md) page.

Once installed, the way you can create a new environment and use it in your VS Code setup is simple:
```sh
poetry_cli_app <folder_destination> <folder_name>
```

The console output will deliver the newly created Poetry environment name, something like:

```sh
Using virtualenv: <environment_name>
```

You can now copy the new **environment name** inside your VS Code project by activating `Python:Select Interpreter` and then choosing `Enter interpreter path...`.

Anytime you need a new isolated environment for a new project, you can easily create it with just one line in the terminal.

That is all! ✨


References:
- [poetry-cli-app](https://github.com/alessandro-maccario/poetry-cli-app)
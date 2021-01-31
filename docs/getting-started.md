# Quick Start

This guide covers getting started with the `blog-build-tools`.

## Installation 

In this _Getting Started_, you need `git`, `docker` and `docker-compose`.

### Git

* Windows: Download & install [git](https://git-scm.com/download/win).
* Mac: Install it with [Homebrew](https://brew.sh/), [MacPorts](http://www.macports.org/) or [installer](http://sourceforge.net/projects/git-osx-installer/).
* Linux (Ubuntu): `sudo apt-get install git-core`

### Docker

* Windows / Mac
  * https://www.docker.com/products/docker-desktop
* Linux (Ubuntu)
  * `docker`: https://docs.docker.com/engine/install/ubuntu/
  * `docker-compose`: https://docs.docker.com/compose/install/

Make sure the following commands are successful:

```shell
$ git
$ docker
$ docker-compose
```

## Create a new CSS Blog

### Get sample project

Clone [jpaztech/blog-build-tools](https://github.com/jpaztech/blog-build-tools) repository and copy example blog directory.

```shell
$ git clone https://github.com/jpaztech/blog-build-tools.git
$ cp -r blog-build-tools/example {YOUR_WORKING_DIR}/blog
```

### Initialize Git repository

```shell
$ cd {YOUR_WORKING_DIR}/blog
$ git init
```

### Setup blog theme

[jpazureid/hexo-theme-jpazure](https://github.com/jpazureid/hexo-theme-jpazure)

```shell
# First, cleanup themes directry
$ rm -rf themes/*

# Add jpazure blog theme as git submodule
$ git submodule add https://github.com/jpazureid/hexo-theme-jpazure.git themes/jpazure
```

### Customize site configuration file

You can configure most settings here.

```shell
$ vim _config.yml
```

### Start / Stop local server

Starts a local server. This is at `http://localhost:4000/`.

```shell
$ docker-compose up
 ...
blog_1  | INFO  Start processing
blog_1  | INFO  Hexo is running at http://localhost:4000 . Press Ctrl+C to stop.
```

To stop server, press `Ctrl+C` and `docker-compose down`.

```shell
^CGracefully stopping... (press Ctrl+C again to force)
Stopping example_blog_1 ... done

$ docker-compose down
```


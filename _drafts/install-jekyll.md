---
layout: default
---

安装 jekyll
====

安装ruby环境
------------

    # 安装ruby 的依赖
    sudo apt-get install -y zlib1g-dev libpq-dev libmysqlclient-dev \
        libsqlite3-dev libxslt-dev libxml2-dev build-essential zlib1g-dev \
        libreadline-dev libssl-dev libcurl4-openssl-dev
    
    # 安装 ruby 的版本管理程序 rbenv
    git clone https://github.com/sstephenson/rbenv.git ~/.rbenv
    echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.bashrc
    echo 'eval "$(rbenv init -)"' >>~/.bashrc
    . ~/.bashrc
    type rbenv
    git clone https://github.com/sstephenson/ruby-build.git \
        ~/.rbenv/plugins/ruby-build

    # 利用 rbenv 安装 ruby， 版本为 1.9.3-p484
    rbenv install  1.9.3-p484
    rbenv global 1.9.3-p484

    # 查看 ruby 的版本
    ruby -v
    # 查看 ruby 路径
    which ruby
    which gem
    
    # 修改 ruby 源，改为 taobao 维护的源
    gem sources --remove http://rubygems.org/
    gem sources -a http://ruby.taobao.org/
    # 安装 bundler
    gem install bundler
    rbenv rehash
    
安装jekyll
----------
    # 解决 jekyll 的依赖，安装 nodejs 和 execjs
    # 没有安装的话，在运行 `jekyll serve` 的时候，会提示`Could not find a JavaScript runtime.`
    $ sudo apt-get install nodejs
    $ gem install execjs

    # 安装 jekyl
	$ vi Gemfile
	source 'https://rubygems.org'
	gem 'github-pages'
    $ bundle


常用命令
--------
    # 新建一个网站
    $ jekyll new blog
    $ cd blog

    # 运行守护进程 daemon
    $ jekyll serve
    # 浏览器打开 http://localhost:4000


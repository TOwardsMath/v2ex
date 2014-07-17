# Project Babel 2（修改版）

# 最近在不断地进行修改，请谨慎下载使用
在进行比较大的修改之前会试着上传zip包，供不想修改的人使用

在搭建[V2ENYO](http://v2enyo.appspot.com)过程中，针对自己的需要，对原来的代码进行了修改，包括去掉一些广告和不需要的功能。

### 部署步骤

* 复制 app.yaml.example 中的内容到 app.yaml，将 application 改为自己的 app id
* 复制 config.py.example 中的内容到 config.py，填入自己的 recaptcha key
* 上传
* 注册成为第一个用户，进入后台进行站点设置，其中，域名和 Host Email 必须填写正确，Host Email 为 GAE 邮箱。

### 修改记录

2012-10-24（ 版本 0.1 ）
* 默认关闭又拍云功能
* 去掉页面中的一些广告
* 去掉了 twitter 的一些功能
* 删除了topic.py中的can continue代码段
* 修复区域节点的问题
* 将foot中“关于”等页面直接改为静态html
* 将搜索与后台域名关联
* 可以在后台填写“重置密码”用到的邮箱

Project Babel 2 is an open source software package for creating and supporting communities. It's written in Python and running on [Google App Engine](http://code.google.com/appengine), which is a free and robust cloud hosting infrastructure.

[V2EX](http://v2ex.appspot.com/), a community about sharing and discovering interesting stuff of the world, is proudly powered by Project Babel 2.

## Features

* Topics are organized under Nodes (Discussion Areas), you can have many Nodes in one community
* Nodes can have header, foot and category property, or organized under Sections
* Two clean themes: one for desktop browser, another for iPhone and Android
* Optimized for modern browsers
* Built-in WebDAV avatar facility, you can host all avatars with MobileMe or other WebDAV servers
* Atom feed output
* HTML5
* Built-in MapReduce tasks for optimizing community data
* Built-in OAuth Twitter client for tweeting and syncing topics/replies
* Built-in Notes feature
* Gravatar support

## Installation

It's recommended to get the latest codebase of Project Babel 2 with git:

    git clone http://github.com/livid/v2ex.git v2ex
    
Then you can rename *v2ex* to whatever you want to match your own App Engine AppID. And follow the steps:

1. Copy app.yaml.example to app.yaml and change its *application* to match your own AppID.
2. Copy config.py.example to config.py, and if you want to use the built-in Twitter features, please fill in your own OAuth consumer key and secret. And callback address for Twitter is http://your_app_id.appspot.com/twitter/oauth .
3. Add this folder to Google App Engine Launcher as an existing application, and click Deploy. It's done and quite simple, right?

If you have any questions or feature requests, feel free to discuss it in official development node at V2EX:

[http://www.v2ex.com/go/babel](http://www.v2ex.com/go/babel)

## Troubleshooting

## FAQ

### Why I got an error page says it needs index?

For newly deployed App Engine app, it took some time for Google to build indexes so that your data can be fast accessed. It usually take up to an hour to build all indexes required for a new installation of Project Babel 2.

### How about performance?

According to our actual operation data, Project Babel 2 is able to support 100,000 pageviews under App Engine free quota. If you don't mind enabling billing, Project Babel 2 is able to support large sites with millions pageviews/day as long as you have enough budget for traffic.

Performance is always our area of focus, we'll keep improving it.

## License

Project Babel 2 is licensed under very liberal BSD license.

Copyright (c) 2010, Xin Liu
All rights reserved.

Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:

* Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
* Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
* Neither the name of the OLIVIDA nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

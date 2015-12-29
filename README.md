alpine-ruby
=============

###适合中国用户的最小Ruby语言镜像

* 基于 [alpine](https://hub.docker.com/_/alpine/)

* RubyGrems 源更换为<https://ruby.taobao.org/>


###Tags

* `x.x.x`: 只包含ruby及bundler，适合用于运行生产环境的应用程序。
* `x.x.x-dev`: 包含`build-base`,可以编译`native gem extensions`，适合开发环境。
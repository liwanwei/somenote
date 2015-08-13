
[Github上的page设立帮助页面](https://help.github.com/categories/github-pages-basics/ "https://help.github.com/categories/github-pages-basics/")

###安装jekyll

- 安装Ruby
	- 下载
		
		Win下下载相应的[RubyInstaller](http://rubyinstaller.org/downloads/ "http://rubyinstaller.org/downloads/")
	- 安装
		- 下载完后解压安装
- 安装Bundler

- Win下必须下载Development kit
	- [Development kit安装配置教程](https://github.com/oneclick/rubyinstaller/wiki/Development-kit "https://github.com/oneclick/rubyinstaller/wiki/Development-kit")
	- 提示：
		
			Please update your PATH to include build tools or download the DevKit
			from 'http://rubyinstaller.org/downloads' and follow the instructions
			at 'http://github.com/oneclick/rubyinstaller/wiki/Development-Kit'
		- 解决方案
		- 下载安装Development kit
	- Win下下载相应的[Dekit](http://rubyinstaller.org/downloads/ "http://rubyinstaller.org/downloads/")
	- 初始化
	
			ruby dk.rb init
			#生成config.yml，这里会检查将要添加DevKit支持的Ruby列表，只支持通过RubyInstaller安装的Ruby
	- 配置路径
			打开Dekit安装路径下config.yml文件，添加`- G:\Ruby22-x64\Ruby22-x64`，即Ruby的安装根目录
	- `ruby dk.rb review`  `#检查要添加DevKit支持的Ruby列表是否有误，可以略过`
	- 安装ruby
	
			ruby dk.rb install

- 安装Jekyll
	- 安装
	
			gem install jekyll
	- 检验是否安装成功
	
			jekyll --version
- 安装Rdiscount
	- 这个用来解析Markdown标记的包，使用如下命令：`gem install rdiscount`



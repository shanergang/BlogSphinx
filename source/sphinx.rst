
使用sphinx管理文档
==================


配置sphinx
----------

安装sphinx
~~~~~~~~~~

在Mac的terminal下输入如下命令安装sphinx::

	pip install sphinx

新建sphinx工程
~~~~~~~~~~~~~~

新建一个文件夹，并在该文件夹下创建一个sphinx工程::

	mkdir Blog
	cd Blog
	sphinx-quickstart

创建工程时，分离source和build目录，方便管理::

		Separate source and build directories (y/N) [n]: y


配置conf.py文件
~~~~~~~~~~~~~~~

.. code-block:: console

    html_theme = 'sphinx_rtd_theme'
    language = 'zh_CN'


同步sphinx到github
------------------

在github个人主页上新建一个repository BlogSphinx，然后通过如下命令将本地sphnix工程下的所有文件push到新建的repository::

	git init
	git add .
	git commit -m 'initial commit'
	git remote add origin https://github.com/shanergang/BlogSphinx.git
	git push -u origin master
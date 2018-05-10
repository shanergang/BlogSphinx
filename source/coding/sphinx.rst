
使用 sphinx 管理文档
====================


配置 sphinx
-----------

在 Mac 的 terminal 下输入如下命令安装 sphinx:

.. code-block:: console

	pip install sphinx

新建一个文件夹，并在该文件夹下创建一个 sphinx 工程:

.. code-block:: console

	mkdir Blog
	cd Blog
	sphinx-quickstart

创建工程时，分离 source 和 build 目录，方便管理:

.. code-block:: console

		Separate source and build directories (y/N) [n]: y

配置 conf.py 文件

.. code-block:: console

    html_theme = 'sphinx_rtd_theme'
    language = 'zh_CN'


同步 sphinx 到 github
---------------------

在 Github 个人主页上新建一个 repository BlogSphinx，然后通过如下命令将本地 sphnix 工程下的所有文件 push 到新建的 repository:

.. code-block:: console

	git init
	git add .
	git commit -m 'initial commit'
	git remote add origin https://github.com/shanergang/BlogSphinx.git
	git push -u origin master

ReadtheDocs
-----------

在 GitHub 里选择仓库，然后依次点击 Setting => Integrations & Service => Add service => ReadtheDocs，激活这个选项。

到 ReadtheDocs 个人主页 import 这个仓库，导入成功后，点击阅读文档，便可看到 Web 效果了


配置目录结构
------------

配置 source 目录下的 index.rst 文件，即主目录:

.. code-block:: console
	
	目录:
	^^^^^
	
	.. toctree::

	   :maxdepth: 2
	   :glob:

	   reading/index
	   learning/index
	   coding/index


在 source 目录下创建对应的目录，每个目录下创建一个 index.rst 文件，即二索引文件。

.. code-block:: console

	mkdir reading learning coding
	touch reading/index.rst learning/index.rst coding/inde.rst 

配置二级索引文件:

.. code-block:: console

	.. toctree::

	   :maxdepth: 2
	   :numbered:

	   sphinx
















ipynb查看程序运行时间
=====================

.. code-block:: python
	
	%%time



并行的实现
==========

``multiprocessing.Pool``


.. code-block:: python

	from multiprocessing import Pool

	def f(x):
		print (x*x)

	pool = Pool(5)
	pool.map(f, range(5))
	pool.close()


文件重命名
==========

``os.listdir()``, ``os.rename()``

.. code-block:: python

	import os

	fileAllName = os.listdir("./<folder name>")
	for name in fileAllName:
		os.rename("./<folder name>/"+name, "./<folder name>/"+<new file name>)

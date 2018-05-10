lsit to string
==============

``''.join()``

.. code-block:: python
	
	numList = [1,2,3]
	str_of_numList = ','.join(str(i) for i in numList)


日期类型的数据
==============

将字符串转变为日期
~~~~~~~~~~~~~~~~~~

``pandas.to_datetime()``

.. code-block:: python
	
	import pandas as pd

	pd.to_datetime('2017-07-01')


产生时间序列
~~~~~~~~~~~~

``pandas.date_range()``

.. code-block:: python
	
	import pandas as pd

	date_list = pd.date_range(start='2017-01-01', end='2017-02-01')
	[str(i).split()[0] for i in date_list]


计算两个日期之间的天数
~~~~~~~~~~~~~~~~~~~~~~

``pandas.Timedelta(<value>, unit='D').days``

.. code-block:: python

	start = '2017-07-01'
	end = '2017-02-01'
	(pd.to_datetime(start) - pd.to_datetime(end)).days



读写文件
========

write to csv file
~~~~~~~~~~~~~~~~~

``open(<file name>,'a')``

.. code-block:: python

	f = open('output.csv', 'a')
	f.write('1,2,3\n')
	f.close()


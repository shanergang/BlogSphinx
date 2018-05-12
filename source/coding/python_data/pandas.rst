Pandas
======

合并 Dataframe
--------------

将两个 Dataframe 按行组合:

.. code-block:: python

	df = pd.DataFrame([[1,2],[3,4]], columns=['a','b'])
	sub1 = pd.DataFrame([[5,6],[7,8]], columns=['a','b'])
	pd.concat([df,sub1], axis=0, ignore_index=True)

将两个 Dataframe 按列组合:

.. code-block:: python
	
	sub2 = pd.DataFrame([[5,6],[7,8]], columns=['c','d'])
	pd.concat([df,sub2], axis=1)
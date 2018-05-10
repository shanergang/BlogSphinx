ARIMAX的实现
============

**目标**：根据辅助时间序列 X，预测时间序列 Y

.. code-block:: python

	from pyramid.arima import auto_arima

	model = auto_arima(train_y, train_x)


安装 ``pyramid.arima``

.. code-block:: console

	pip install pyramid-arima

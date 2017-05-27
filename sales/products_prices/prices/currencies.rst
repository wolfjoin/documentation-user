=================================
如何以外币出售
=================================

价目表也可用于管理外币价格。

* 在菜单 :menuselection:`会计 --> 配置 --> 设置` 中勾选 **允许多种货币**.
  作为管理员，您需要开发票/会计应用程序的顾问访问权限。

* 为每种货币创建一个价目表。一个新的 *货币* 字段以价格表的形式出现

.. tip::
    要激活新货币，请转到 :menuselection:`会计 --> 配置 --> 货币`，
    在列表中选择它，然后按下右上角的激活。现在它将以货币下拉列表显示。

外币价格可以用两种方式定义。

从公开价格自动转换
======================================

公开价格是贵公司的主要货币（见 :menuselection:`会计 --> 设置`），并以产品详细表格设定。

.. image:: ./media/public_price.png
   :align: center

转换率可在
:menuselection:`会计 --> 配置 --> 货币` 中找到. 
他们可以从雅虎或欧洲中央银行更新：手动，每日，每周等。
请参阅 :menuselection:`会计 --> 设置`.

.. image:: ./media/currency_rate.png
   :align: center

.. image:: ./media/prices_conversion.png
   :align: center

设定你自己的价格
===================

如果您不希望您的定价随货币汇率变化，建议您。

.. image:: ./media/pricing_currency.png
   :align: center

.. seealso::

  * :doc:`pricing`

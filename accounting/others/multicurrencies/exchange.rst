=================================
在付款时登记汇率
=================================

概述
========

任何公司做国际贸易时都会面临这个情况 : 不同的货币支付。

在收到付款时, 可转换成公司货币。多货币支付意味着有利率的波动。
Odoo将自动记录汇率的差异。

配置
=============

启用多币种
-----------------------

会计模块, 去 :menuselection:`配置 --> 设置`勾选 **允许多货币** , 然后点击 **应用** 。

.. image:: media/exchange_rate03.png
   :align: center

汇率配置 :menuselection:`配置 --> 汇率.写下汇率, 确保货币是活跃的。

.. image:: media/exchange_rate02.png
   :align: center

在本文档中, 基础货币是 **欧元** , 我们将收付款记录在 **美元** 。

.. image:: media/exchange_rate08.png
   :align: center

.. tip:: 
    您可以从 **European Central Bank** 或 **Yahoo** 自动获取欧洲央行的汇率。请阅读文档 : 
    :doc:`how_it_works`.

配置你的日记账
----------------------

为了用其他货币登记收付款, 你必须在账上 **删除币种默认值，保留空白** 。
去会计应用程序, 点击 :menuselection:`更多 --> 设置`.

.. image:: media/exchange_rate06.png
   :align: center

检查外币的字段是否为空, 或者需要在哪个货币下登记收付款。
如果货币已填写, 这意味着你可只能用这种货币登记收付款。


.. image:: media/exchange_rate10.png
   :align: center

用其他币种记录付款
========================================

在会计应用程序中, 至 :menuselection:`销售 --> 付款`. 登记收付款并注明已用外币登记。
然后点击 确定 。

.. image:: media/exchange_rate05.png
   :align: center

会计分录已过账但没有分配。

回到发票 (:menuselection:`销售 --> 客户发票`) 并点击 **添加** 分配付款。


.. image:: media/exchange_rate04.png
   :align: center

用其他币种记录银行对账单
===============================================

创建或导入付款的银行对账单。 **金额** 以公司货币。有两个补充的字段，
**外币金额** 是实际支付的金额，而 **货币** 是支付的币种。

.. image:: media/exchange_rate07.png
   :align: center

调节的时候, Odoo将直接与正确的 **发票** 匹配。
你会看到的发票货币下的金额及本位币下的总额。

.. image:: media/exchange_rate09.png
   :align: center

检查汇兑损溢
===================================

去  :menuselection:`顾问 --> 日记账分录`  , 找到 **汇兑损溢**  日记账分录。
所有的汇率差异将记录在此。

.. image:: media/exchange_rate01.png
   :align: center

.. tip::
    在会计设置上, 可以更汇兑损溢的设置.

.. seealso::
    * :doc:`../../bank/reconciliation/configure`
    * :doc:`../../bank/reconciliation/use_cases`
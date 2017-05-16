==========================
配置分录模型
==========================

概述
========

在Odoo中你可以预设一些会计分录, 这样在计提例如银行费用这些经常性会计分录的时候就省事多了。

我们将下面的例子来说明这一概念 :每个月, 我公司收到银行费用成本, 
这取决于我们的银行账户当前余额。这个费用是变量。

创建对账模型
============================

首先, 我们需要配置两个调节分录。为此, 会计应用程序仪表盘。在银行账点击 :menuselection:`更多More --> 调节模型Reconciliation Models`.

.. image:: media/configure01.png
   :align: center

我们希望能够轻松地预订我们的银行手续费。我们银行根据我们的余额扣除费用，这意味着每月可能会有所不同。

我们创建一个名为银行费用的按钮标签, 选择正确的科目记录这些费用。此外我们还需要指定类型是" 余额百分比Percentage of balance", 比例为100%。这个参数将告诉Odoo考虑整个费用。

.. image:: media/configure02.png
   :align: center

当完成时保存变更。

.. note::

	如果你的银行费用是固定的, 也可以选择 **固定的(Fixed)** 以及定义金额。

.. seealso::

	您还可以使用此功能来处理折扣。请参阅
	:doc:`../../receivables/customer_invoices/cash_discounts`

基于对账模型登记付款
======================================================

通过导入你的银行对账单来登记付款, 这会影响银行的支付费用。

进行调节时, 您可以选择一个未清的余额, 点击 **调节模型Reconciliation Model**  按钮(在这种情况下,  **银行费用Bank Fees**) 立即获得所有相关的数据。

.. image:: media/configure03.png
   :align: center

最后, 点击 **调节Reconcile** 完成过程.

.. seealso::

	* :doc:`../feeds/manual`
	* :doc:`../feeds/ofx`
	* :doc:`use_cases`

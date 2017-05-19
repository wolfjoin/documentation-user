=====================================
Odoo多币种是如何工作的？
=====================================

概述
========

在Odoo选择使用多种货币选项, 在销售发票, 报价和采购订单或收到账单和支付货款时, 
可选择货币而不是本位币。用多种货币, 还可以用外币设置银行账户, 也可用于报表。

配置
=============

开启多币种
----------------------

会计模块, 去 :menuselection:`配置 --> 设置` , 选择 **允许多货币** , 然后点击 **应用** 。

.. image:: media/works01.png
   :align: center

汇率分类账
---------------------

The **Rate Difference Journal** records the differences between the payment
registration and the expected amount. For example, if a payment is paid
1 month after the invoice was issued, the exchange rate has probably
changed. The fluctuation implies some loss or profit that are recorded
by Odoo.
该 **比率差异日记账** 记录支付登记和预期量之间的差异。
例如，如果付款在发票发出1个月后支付，汇率可能已经改变。
波动意味着Odoo记录的一些损失或利润。

查看或编辑正在使用的汇率

.. image:: media/works02.png
   :align: center

查看或编辑正在使用的汇率
----------------------------

You can manually configure the currency rates in  Open the currencies you want to use in Odoo and edit it.
Make sure the currency is active.
您可以手动配置的汇率 :menuselection:`配置 --> 多币种 --> 币种`.打开你想要使用的货币并编辑它。确保货币状态是有效的。

.. image:: media/works03.png
   :align: center

点击 **查看汇率** 编辑并查看历史记录 :

.. image:: media/works04.png
   :align: center

点击 创建 **添加汇率**, 输入日期和汇率。完成后点击 **保存** 。

.. image:: media/works05.png
   :align: center

实时货币比率(付费企业版功能)
------------------

默认情况下,货币需要手动更新。但是你可以同步 `Yahoo <https://finance.yahoo.com/currency-converter/>`__ 或是
 `欧洲中央银行 <http://www.ecb.europa.eu>`__. 在 
:menuselection:`Configuration --> Settings`, 转到 **实时货币汇率** 部分。

Choose the interval : Manually, Daily, Weekly or Monthly. You can always
force the update by clicking on **Update Now**. Select the provider, and you
are set !

.. image:: media/works06.png
   :align: center

.. note::

	只有 **有效的** 货币会被更新

配置科目表
--------------------------------

在会计应用程序中, 去  :menuselection:`顾问 --> 科目表`.
在每个科目, 您可以设置一个货币。所有这个账目的账都使用这个货币。

如果留空, 就意味着可以处理所有有效的币别。

.. image:: media/works07.png
   :align: center

配置日记账
-----------------------

用外币登记收付款, 需在日记账上去除货币限制。去会计仪表板, 点击 **更多** 和 **设置** 。

.. image:: media/works08.png
   :align: center

检查外币的字段是否为空, 或者需要在哪个货币下登记收付款。
如果货币已填写, 这意味着你可只能用这种货币登记收付款。

.. image:: media/works09.png
   :align: center

Odoo多币种是如何工作的？
=====================================

现在你在多种货币环境中, 所有科目将链接一个货币, 国内或国外。

销售订单和发票
-------------------------

你现在可以设置不同的货币而不是销售订单和发票上的货币。货币设置将应用到整个文档。

.. image:: media/works10.png
   :align: center

采购订单和供应商账单
---------------------------------

你现在可以设置不同的货币比公司对你的采购订单和供应商的账单。货币被设置为整个文档。

.. image:: media/works11.png
   :align: center

付款登记
---------------------

在会计应用程序中, 去  **销售 > 付款登记** 。登记收付款, 设置货币。

.. image:: media/works12.png
   :align: center

银行对账单
---------------

当创建或导入银行对账单, 是本位币的金额。
但是现在有两个字段, 实际支付的金额和原币支付的金额。

.. image:: media/works13.png
   :align: center

当调节时, Odoo将收款直接与正确的发票匹配。你会得到的发票金额和公司本位币金额。

汇率分类账
---------------------

去 :menuselection:`顾问 --> 日记账分录` 找到 **汇兑损溢** 日记账分录。
所有的汇率差异将记录在此。

.. image:: media/works14.png
   :align: center

.. seealso::

	* :doc:`invoices_payments`
	* :doc:`exchange`

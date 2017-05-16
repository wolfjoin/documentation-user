=============
使用支票支付
=============

当支付供应商账单时,你可选择用支票来支付。然后,在一天结束的时候,
可批量打印所有支票。最后,银行将支付的支票和银行对账单核销。

配置
=============

安装必须的模块
---------------------------

用支票来付款,必须安装* 支票填写 模块 **Check Writing** module.
这个模块登记支票处理。其他模块用来打印支票, 国家不同也不同。
举个例子,美国 支票打印模块根据美国的支票来设计。 **U.S. Check Printing**

.. note::

	根据所在国家和所使用的科目表,这些模块可默认安装。(例如:美国用户不用安装,已默认配置)。

激活支票付款方式
-------------------------------

如需用支票支付,必须在银行账上激活付款方式。从会计仪表板(进入会计应用程序的界面),点击你的银行账户，点击更多‣设置选项: :menuselection:`More --> Settings` 。
在 付款方式字段中，设置支票。

.. image:: ./media/check01.png
  :align: center

打印支票的兼容支票纸张
===============================================

美国
-------------

对于美国, Odoo默认支持支票格式 :

- **Quickbooks & Quicken**: check on top, stubs in the middle and bottom
- **Peachtree**: check in the middle, stubs on top and bottom
- **ADP**: check in the bottom, and stubs on the top.

也可以通过自定义自定义您自己的检查格式。

用支票支付供应商账单
================================

用支票支付采购发票, 需要三个步骤:

1. 在账单上登记付款
2. 批量打印所有的已登记付款
3. 调节银行对账单

用支票登记付款
---------------------------

如需在账单上登记付款,在此点开发票
:menuselection:`Purchases --> Supplier Bills`. 一旦采购发票审核,可登记付款。在对话框内, 将 **支付方式**设置为 **支票**


.. image:: ./media/check02.png
  :align: center

付款界面字段的解释 :

.. demo:fields:: account.action_account_payments

.. demo:action:: account.action_account_payments
	
	Try paying a supplier bill with a check

.. _PrintChecks:

打印检查
------------

从会计仪表盘,银行账户,可看到一个链接“X支票打印”"X checks to print"。
点击这个链接,会得到所有未打印的支票清单。从这个界面,可批量打印或是逐个检查。

如果你想在打印前查看每笔付款,打开支付界面,点击* 打印支票 [UNKNOWN NODE problematic]。对话框会问你检查的编号。它会自动提出你下一个编号,但是,如果编号不匹配, 可修改。

如需批量打印,从列表中选择所有支票, 点击顶部“打印”菜单。

.. image:: ./media/check03.png
  :align: center

.. _ReconicleBankStatements:

调节银行对账单
-------------------------

当处理银行对账单时,支票已从银行账户支出,Odoo将自动与付款匹配。这标志着付款 **调节** .

.. tip::

	检查尚未记入的支票，打开付款清单并在发送状态下进行过滤。查看超过2周前的日期的付款。

用支票支付任何东西
=========================

可登记与发票没有关系的付款。使用顶部菜单购买‣付款。: :menuselection:`Purchases --> Payments`. 
登记付款, 选择付款方式。

如果您支付特定的供应商账单，请将账单的引用放在 **备注** 字段中。

.. image:: ./media/check04.png
  :align: center

一旦您通过支票支付付款，请不要忘记确认。一旦 **确认**，您可以直接使用 **打印支票** 或按照上述流程批量打印支票：

-  `Print checks <PrintChecks_>`_

-  `Reconcile bank statements <ReconicleBankStatements_>`_

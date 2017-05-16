=================================
手工登记银行对账单
=================================

概述
========

通过Odoo, 你可以导入你的银行对账单并与你的银行同步，
当然你也可以手动创建你的银行对账单。

配置
=============

登记发票不需要任何特殊配置。所有您需要做的就是安装会计应用。

.. image:: media/manual01.png
   :align: center

手工登记银行对账单
=================================

创建银行对账单
---------------------------

在仪表板中, 点击相关银行账目的按钮 **新对账单** 。如果某些调节需要完成, 
新的对账单链接将会出现在下面。

.. image:: media/manual02.png
   :align: center

只需在你的银行对账单中填写字段的信息。参考信息可以手动填写或者不填。
我们建议填写合作伙伴来简化调节进程。

期初余额和期末余额之间的差异该等于计算的余额。

.. image:: media/manual03.png
   :align: center

做完这些后, 点击 保存 .

调节银行对账单
------------------------------

您可以选择直接调节对账单, 通过单击按钮“调节” |manual04|

.. |manual04| image:: media/manual04.png

你也可以在仪表板上开始调节进程, 通过点击"调节#项目" **Reconcile # Items**.

.. image:: media/manual05.png
   :align: center

Click onto reconcile your bank statement. If the partner
is missing, Odoo will ask you to.
点击 验证 **Validate** 调节你的银行对账单。如果没有业务伙伴信息, 
Odoo会让你选择一个业务伙伴 **select a partner**。

.. image:: media/manual06.png
   :align: center

.. tip::

		按ctrl + enter调节表格里所有平衡过的项。

从调节关闭银行对账单
---------------------------------------------

如果余额正确, 你可以直接关闭调节, 点击调节 |manual07|.

.. |manual07| image:: media/manual07.png

否则, 单击 |manual08| 打开对账单并纠正这个问题。

.. |manual08| image:: media/manual08.png

关闭银行对账单
---------------------

在会计仪表板, 点击银行账的更多按钮, 然后点击银行对账单。

.. image:: media/manual09.png
   :align: center

关闭银行对账单, 只需点击 **验证** 。

.. image:: media/manual10.png
   :align: center

.. seealso::

	* :doc:`../reconciliation/use_cases`
	* :doc:`../feeds/synchronize`

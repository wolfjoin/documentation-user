==========================
导入OFX 对账单文件（付费企业版功能）
==========================

开放金融交易所(OFX)是一个统一规范金融机构之间的电子金融数据交换平台, 企业和消费者通过互联网交易。

Odoo, 您可以从你的银行或财务软件下载一个OFX文件并将其直接导入Odoo。
这将创建所有银行对账单。

.. tip::

	现在测试OFX文件的功能 `with this sample OFX file <https://drive.google.com/file/d/0B5BDHVRYo-q5Mmg4T3oxTWszeEk/view>`__

配置
=============

为了能导入OFX对账单, 您需要在Odoo激活特性。在会计应用程序中, 
进入菜单 :menuselection:`Configuration --> Settings`. 
从会计设置, 检查银行对账单选项 **Import in .OFX Format** 和应用.

.. image:: media/ofx01.png
   :align: center

一旦你安装这个功能, 你可以设置你的银行账户, 允许导入银行对账单文件。要做到这一点, 
去会计仪表板, 在银行账户点击 更多 按钮 **More** 。
然后, 点击 **Import Statement** 加载第一个OFX文件。

.. image:: media/ofx02.png
   :align: center

在下面的屏幕加载OFX文件, 单击 导入 创建你所有的银行对账单。

.. image:: media/ofx03.png
   :align: center

如果成功加载该文件, 您会被重定向到银行核对屏幕, 所有的交易会被重新核对。

导入OFX 文件
===================

在导入你的第一个文件之后, Odoo会计仪表板将自动建议你导入更多文件。在接下来的文件导入, 
你不需要去 **More** 菜单了, 您可以直接点击链接 **Import Statement**.

.. image:: media/ofx04.png
   :align: center

每次你得到一个新客户/供应商的相关对账单时, Odoo将要求您选择正确的调节对象。
从此操作信息, Odoo将自动完成下一个付款或是这些联系。这将加快调节过程。

.. seealso::

	* :doc:`qif`
	* :doc:`coda`
	* :doc:`synchronize`
	* :doc:`manual`

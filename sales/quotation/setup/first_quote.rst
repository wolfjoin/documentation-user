=================================
如何创建我的第一个报价？
=================================

概述
========

报价单是发送给客户的用于提供产品或者服务预估成本的文档。客户可以接收报价, 
这时候销售人员就需要发布一个销售订单。或者客户不接受。

例如, 我们的公司销售电子产品并且我的客户Agrolait有兴趣购买 ``3 iPads``。
我会发给他们一个这些Ipad的报价单, 报价 ``320 USD`` , ``5%`` 的折扣。

本节将告诉您如何进行。

配置
=============

安装 销售管理 模块
-----------------------------------

为了能发出你的第一个报价单, 你需要在Odoo后台的APP模块中安装 
**销售管理（Sales Management）** 模块。

.. image:: media/first_quote01.png
    :align: center

允许指定销售行的折扣信息
-----------------------------------

在报价单上允许设置折扣是一个常见的销售活动, 它可以改进把潜在客户变成正式客户的机会。

在我们的示例中, 我们想要给 ``Agrolait`` 一个 ``5%`` 的销售折扣。要想使用该特性, 
进入 **销售** 应用, 选择 :menuselection:`配置(Configuration) --> 设置(Settings) ` ,
然后在 **报价单和销售** 勾选 **折扣** 中的 **允许在销售订单明细行上折扣**  (见下图)
并且点击 **应用** 确认。

.. image:: media/first_quote02.png
    :align: center

创建销售询价单
=====================

To create your first quotation, click on and
click on **Create**. Then, complete your quotation as follows:
要创建你的第一个报价单, 点击 :menuselection:`销售(Sales) --> 报价单(Quotations)` ,
并点击 **创建** 。然后, 按照以下步骤完成报价 :

客户与产品
---------------------

添加到报价单中的基本信息是客户(你要发送的那个人)和要卖的产品。 从报价单视图中, 
在 **客户** 的下拉列表中选择客户, 并且在 **订单行** 点击 **添加项目** 并选择产品。
不要忘了在 **订单数量** 手工的更改数量以及折扣(如果安装了此特性)。

.. image:: media/first_quote03.png
    :align: center

如果在你的Odoo环境中还没有客户或者产品, 你可以在创建报价单的时候随手创建客户或者产品 :

-   添加一个新的客户, 点击 **客户** 的下拉菜单并且点击 **创建并编辑** 。在新的窗口中,
    你将能记录客户所有的详细信息, 例如地址, 网址, 电话号码和个人联系信息。

-   要添加一个新的产品, 在 **订单行** 中点击添加一个新项目并在下拉列表中选择
    **创建并编辑** 。你就可以记录按照以下图片记录产品信息(产品类型, 成本, 销售价格, 开票规则等)

税金
-----

To parameter taxes, simply go on the taxes section of the product line
and click on **Create and Edit**. Fill in the details (for example if you
are subject to a ``21%`` taxe on your sales, simply fill in the right amount
in percentage) and save.
要设置税的参数, 只需要在产品行的税字段点击 **创建并编辑** 。填写详细信息(例如你们的销项税是" 21% ")并保存。

.. image:: media/first_quote04.png
    :align: center

条款和条件
--------------------

你可以选择报价单的到期日期并且可以直接在报价单中添加公司的条款和条件(见下图)。

.. image:: media/first_quote05.png
    :align: center

预览并发送报价
==========================

在发送报价单之前, 如果想预览报价单。可以点击 **打印** 按钮(顶部)。
它会给你呈现出一个带有详细信息的PDF版本

.. image:: media/first_quote06.png
    :align: center

.. tip::
    更新你的公司的详细信息(地址, 网址, 图标等)会显示在报价单上的 :进入
    :menuselection:`设置 --> 用户 --> 公司`.

点击 **通过电邮发送** 可以自动的把报价单作为电子邮件的附件发送给你的客户。
你可以在发送邮件之前调整邮件内容, 甚至可以把它保存, 作为以后可以重复使用的模板

.. image:: media/first_quote07.png
    :align: center

.. seealso::
    * :doc:`../online/creation`
    * :doc:`optional`
    * :doc:`terms_conditions`
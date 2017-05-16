===========================================
如何管理银行的外币？
===========================================

在Odoo，每一笔交易以公司的默认币种记录。报告都是基于公司的币种。
对于以其他币种发生的交易, Odoo同时以公司的币种的价值，以及以交易币种的价值存储。

当你有一个外币的银行账户, 对于每笔交易, Odoo都保存两个值 :

-  公司币别中的借方／贷方

-  银行账户币别中的借方／贷方

汇率会自动更新, 使用yahoo.com, 或者欧洲央行的在线服务。

配置
=============

激活多币种功能
-----------------------------------

为了允许贵公司使用多种货币，您应该启用多种货币模式。在会计应用程序中，
进入配置‣设置‣会计和财务功能 确保允许 **多币种** 框被勾选。
提供货币兑换收益/损失会计科目 **Currency Exchange Gain / Loss** ，然后单击应用。

配置货币
--------------------

Once the Odoo is configured to support multiple currencies, you should
activate the currencies you plan to work with. To do that, go the menu
:menuselection:`Configuration --> Currencies`. All the currencies are created by default,
but you should activate the ones you plan to support. (to activate a
currency, check his active field)
一旦Odoo配置为支持多种货币，您应该激活您计划使用的货币。请选择 配置-->多币种-->币种 启用。默认情况下都会创建所有货币，但应激活您计划支持的货币。（激活货币，移动到右上角字段显示激活，点击）

激活货币后，您可以配置参数以自动执行货币汇率更新。这些选项也在会计应用程序的
设置中，位于页面底部：

该功能在社区版无，社区版点开币种后，导航栏有“查看货币比率”人工新建或者导入。

.. image:: media/foreign01.png
   :align: center

点击 **现在更新** 链接到目前最新的汇率。

创建银行账户
-------------------------

在会计应用程序中, 我们首先去配置‣会计/银行账户 :menuselection:`Configuration -->
Accounting / Bank account`, 我们创建一个新的账户。

.. image:: media/foreign02.png
   :align: center

一旦你保存这个银行帐户，Odoo将为你创建所有的文件：

- 试算表的科目

- 将此帐簿显示在仪表盘上

- 如果选择框 **在发票页脚显示** , 银行信息将在发票页脚显示

例如 :外币的供应商账单
============================================

根据上面的例子中, 我们假设我们收到中国供应商的发票。

在采购‣供应商账单中，您可以看到： :menuselection:`Purchase --> Vendor Bills` 

.. image:: media/foreign03.png
   :align: center

一旦你已经准备好支付这个账单, 点击登记付款记录付款。

.. image:: media/foreign04.png
   :align: center

这是你所要做的。Odoo将在调节时, 自动将发票日和付款日的汇率差计入外汇损益。

注意, 您可以用另一种货币支付外汇发票。在这种情况下, Odoo将自动完成两种货币之间的转换。

客户对账单
====================

客户和供应商的报表是用发票货币来管理的。所以, 客户(供应商)的到期金额总是用发票的货币表示。

如果同一客户有几个不同货币的发票, Odoo将按货币分类, 如下报告所示。

.. image:: media/foreign05.png
   :align: center

在上面的报告, Camptocamp相关的应收帐款没有用第二种货币管理, 这意味着, 
每笔交易都使用自己的货币。如果你喜欢, 你可以为该客户的应收帐款设置第二种货币,
他所有的债务将自动转换货币。

在这种情况下, 客户对账单总是只有一种货币。一般来说, 这不是什么客户所希望的, 
他更喜欢看到他收到发票的货币金额;

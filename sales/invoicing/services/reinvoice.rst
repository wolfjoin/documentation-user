=============================================
如何为你的客户重开费用发票?
=============================================

如果你的员工在为您的客户的项目工作时经常花自己的个人的钱。比如, 在与您的客户开会时
我们的员工支付了停车位费用。作为一家公司, 你希望能够将此花费开票给你的客户。

在该文档中, 我们将看到两个用例。
第一, 非常基本的, 一个简单的费用的开票给您的客户就像为一个产品所做的那样。
第二个, 更先进, 由您的员工进入你的费用系统直接开票给你的客户。

用例 1 :简单的费用开票
====================================

以下作为示例, 你正在给其中的一个客户(``Agrolait``)升级并且你需要打印很多复印件, 
这些复印件作为公司的费用并且需要为之开票

配置
-------------

为了销售服务和发送发票, 你需要从 **Apps** 图标安装 **销售** 模块。

.. image:: media/reinvoice01.png
    :align: center

创建费用产品
-----------------------------

那么现在你就需要创建一个命名为“复印" 的产品

在 **销售** 模块下, 进入 :menuselection:`销售 --> 产品`  并创建一个如下产品 :

-   **产品类型  **: 可消耗

-   **开票策略**: 已交货数量(您将手动将数量设置为销售订单上的发票)

.. image:: media/reinvoice02.png
    :align: center

创建销售订单
-------------------

Now that your product is correctly set up, you can create a sale order
for that product (from the menu :menuselection:`销售 --> 销售订单`) 
with the ordered quantities set to 0. 
Click on **Confirm the Sale** to create the sale
order. You will be able then to manually change the delivered quantities
on the sale order to reinvoice the copies to your customer.
现在产品已经设置好了, 就可以创建该产品的销售订单(从 :menuselection:`销售 --> 销售订单` ), 
数量设置为0。点击 **确认订单** 确认为销售订单。
随后你可以手工的在销售订单上更改产品数量在同一张发票单上给客户重复开票

.. image:: media/reinvoice03.png
    :align: center

费用开票给客户
------------------------------

到了月末, 你已经为客户打印了 ``1000`` 份并且你想要对他们重新开票。
就可以从相关的销售订单上点击 **订单数量** , 手工的输入复印件数量并点击 **保存** 。
点击 **交货** 验证数量，订单行就变为蓝色, 意味着可以开票。然后点击 **创建发票**

.. note::
    销售订单上的总数量是0因为发票是基于发货数量的。
    发票会根据发给该客户的正确的数量进行计算

生成的发票是草稿状态, 所以你总是可以控制数量并且变更总量。
你能注意到要开票的数量是基于发货的数量

.. image:: media/reinvoice04.png
    :align: center

点击确认让客户付款

用例2 :通过报销模块给费用开票
===================================================

要解释这个, 让我们假设你的公司卖给你的顾客 ``Agrolait``一些咨询服务
并且双方都同意贵司顾问的路费作为成本来开票

配置
-------------

现在, 你需要再安装两个模块

-   费用追踪

-   需要在会计模块的设置中激活分析会计

.. image:: media/reinvoice05.png
    :align: center

创建一个费用类别的产品
-------------------------------

现在你需要创建一个称之为 ``公里`` 的产品。

在 **销售** 模块下, 进入 :menuselection:`销售 --> 产品`  并创建一个如下产品 :

-   可用于费用

-   产品类型 : 服务

-   开票策略 :基于时间和材料开票(invoice based on time and material)
    社区版，没有这个选项，选择已交货数量，试一下

-   费用类的开票原则 :基于成本(Expense invoicing policy: At cost)

-   追踪服务 :手工的在订单上设置数量(Track service: manually set quantities on order)

.. image:: media/reinvoice06.png
    :align: center

创建销售订单
--------------------

仍是从销售模块, 进入菜单项 :menuselection:`销售 --> 销售订单`  并在订单行上添加产品 **咨询** 。

.. tip::
    如果您的产品尚不存在，您可以从SO中即时配置。只需在 **产品** 字段中输入名称，
    然后单击 **创建并编辑** 即可对其进行配置。


根据产品的配置, 一个 **分析科目** 可以自动的生成, 如果没有的话, 你也可以容易的创建一个, 用来在销售订单上链接费用（社区版：点击 **其他信息** 标签，分析窗户，创建）。不要忘了确认销售订单

.. image:: media/reinvoice07.png
    :align: center

.. note::
    Refer to the documentation :doc:`../../../accounting/others/analytic/usage` 
    to learn more about that concept.

创建相关费用单据并关联到销售订单(SO)
-------------------------------------

假设你们公司的顾问在十月份在咨询项目上的路程是" 1.000公里 "。
你就可以创建一个费用并且通过分析账户和相关的销售订单关联起来

进入 **费用** 模块并点击 **创建** 。输入以下费用 :

-   **费用说明**: 公里2015年10月

-   **产品**: 公里

-   **数量**: 1.000

-   **分析账户**: SO0019 - Agrolait

.. image:: media/reinvoice08.png
    :align: center

点击 **提交给经理** 。只要费用被批准并登录到日记账分录, 
一个和费用一致的分录记录就会咋订单上自动生成

费用开票给客户
------------------------------

现在就可以把所有发票行开票给你的客户了

.. image:: media/reinvoice09.png
    :align: center

.. seealso::
    * :doc:`support`
    * :doc:`milestones`

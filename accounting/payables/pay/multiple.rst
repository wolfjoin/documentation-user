=================================
如何一次性支付几个账单？
=================================

Odoo提供了一种简单而有效的方式，可以一次处理多个账单，并提供各种快速或复杂的选项。
通过一个单一的过程，任何人只需点击几下即可处理帐单和付款。

一次支付多个账单
===================================

登记一些付款
-----------------------

在以下示例中,我们将生成一些账单。可在会计仪表板控制整个过程(
打开会计应用程序后的界面)。

.. image:: ./media/multiple01.png
  :align: center

要创建帐单，请打开 **仪表板** 菜单，然后单击 **供应商账单** 。
在 **供应商账单** 窗口中，单击 **创建** 。

.. image:: ./media/multiple02.png
  :align: center

Choose the vendor from which you wish to purchase the product, and click
on Add an item to add one (or more) product(s). Click on **Save** and then
**Validate**.
选择供应商,并点击添加项目, 可添加一个(或更多)产品(s)。点击 **保存** , 
然后点击 **确认** 

一个接一个地支付供应商账单s
---------------------------------------

.. image:: ./media/multiple03.png
  :align: center

我们现在将记录一笔付款。打开账单，然后点击 **登记支付** 。插入付款方式，日期和金额，然后单击 **验证**。

.. image:: ./media/multiple04.png
  :align: center

确认支付后,系统将自动将付款和发票核销,发票将到 **已支付**状态。系统会自动生成一个凭证。

多个账单一块支付
----------------------------


为了彻底说明这个过程,按要求至少创建2张发票。**确保所有发票来自于同一个供应商** 。

.. image:: ./media/multiple05.png
  :align: center

在“供应商账单”中，选中刚刚创建的新账单，方法是选中每个账单。在页面中间的 **动作** 菜单中，单击 **登记付款** 。

.. image:: ./media/multiple06.png
  :align: center

插入付款的详细信息。系统计算了两个账单的总金额，但您可以自由修改。点击 **验证** 。

登记付款, 随后调节
----------------------------------------

你也可以在付款登记之后对付款进行调节。

首先, 我们来创建一个付款

这将从仪表板处理‣银行日记‣更多选项‣付钱 :menuselection:`Dashboard --> Bank journal -->
More Option --> Send Money`

.. image:: ./media/multiple07.png
  :align: center


使用支票付款方式创建支付单。选择相关的供应商和剩余的金额。填写所有详细信息后，
确认付款。。

.. image:: ./media/multiple08.png
  :align: center

如你所见, 账单的状态显示什么已经过账什么还没有过账。

收到银行对账单后, 可在仪表板上进行核销。它会自动核对金额。

.. seealso::
	
	详情参见银行调节过程, 请参阅 :

	* :doc:`../../bank/reconciliation/use_cases`

多个供应商账单的部分付款
==========================================

如何同时支付几个有现金折扣的供应商的发票?
----------------------------------------------------------------

你已经学会了如何以各种方式支付账单，但是部分付款呢？我们正在采取另一个例子，我们将对各种账单进行部分支付。

我们创建多个账单，并通过银行对账单部分支付。

我们添加付款条款，允许一些现金折扣，供应商提供我们提前支付折扣。

.. image:: ./media/multiple09.png
  :align: center

用以上的付款条款来创建发票。

.. image:: ./media/multiple10.png
  :align: center

我们创建了以下账单：

.. image:: ./media/multiple11.png
  :align: center

我们可通过创建银行对账单来支付款项,付款时可调整现金折扣。

.. image:: ./media/multiple12.png
  :align: center

核销银行对账单之前,需要先创建一个现金折扣模型。

.. image:: ./media/multiple13.png
  :align: center

现在我们回到银行对账单，并打开调节视图。

.. seealso::

	For bank statement reconciliation with model option, see

	* :doc:`../../bank/reconciliation/configure`


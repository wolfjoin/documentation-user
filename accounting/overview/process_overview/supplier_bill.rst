==================================
从供应商账单到付款
==================================

Once vendor bills are registered in Odoo, you can easily pay vendors for
the correct amount and at the right time (not too late, not too early;
depending on your vendor policy). Odoo also offers reports to track your
aged payable balances.
一旦供应商账单在Odoo注册，您可以轻松地向供应商支付正确的金额，
并在适当的时间（不要太晚，不能太早;取决于您的供应商政策）。
Odoo还提供跟踪您的应付账款余额的报告。

如果你想管理供应商发票, 可使用Odoo采购应用程序, 程序可基于过去的采购订单控制和自动完成发票管理。


从供应商账单到付款
===========================

登记一张新的供应商账单
------------------------

当收到供应商单据时，您可以从会计应用程序中的采购‣供应商帐单记录 :menuselection:`采购 --> g供应商账单` 
作为快捷方式，
您还可以使用会计仪表板上的“ 新建账单”功能。

.. image:: ./media/vendor_bill05.png
   :align: center

登记一张新的供应商发票, 首先选择一个供应商并在 **供应商参考**
输入发票信息, 然后添加并确认产品行, 确保正确的产品数量、税收和价格。

.. image:: ./media/vendor_bill01.png
   :align: center

在屏幕的下部, 更新税收和含税金额, 保存发票。
将产品的价格配置成不含税, Odoo自动计算税收。

.. 注解:: 
    On the bottom left corner, Odoo shows a summary table of all taxes on the vendor bill. 
    在左下角,Odoo汇总了这张发票的所有税额。
    在一些国家,计算的方法不同(每行计算或是总的计算)。
    默认的方式是每行计算(可能不同的产品有不同的税率。例如酒精和香烟)。如果采购发票上的税额不同,你可以调整左下角的表, 使税额与之匹配。

验证供应商帐单
------------------------

验证供应商账单后，将根据发票上的配置生成日记账分录。
根据您选择使用的会计包，此日记账分录可能会有所不同。

对于大多数欧洲国家，日记帐分录将使用以下帐户：

-  **Accounts Payable:** defined on the vendor form

-  **Taxes:** defined on the products and per line

-  **Expenses:** defined on the line item product used

For Anglo-Saxon (US) accounting, the journal entry will use the
following accounts:

-  **Accounts Payable:** defined on the vendor form

-  **Taxes:** defined on the products and per line

-  **Goods Received:** defined on the product form

在确认一些采购发票后, 你可以检查损益表或资产负债表, 以验证发票对账的影响。

支付账单
----------

在采购发票上直接付款, 你可以点击顶部的 **登记付款** 。

从那里，您选择付款方式（即检查帐户，信用卡，支票等）和您要支付的金额。
默认情况下，Odoo将提交付款单上的剩余余额。在备忘录字段中，
我们建议您将供应商发票号设置为参考（如果正确设置，Odoo将从供应商帐单自动填充此字段）。

.. image:: ./media/vendor_bill06.png
   :align: center


.. 注解::
    不在采购发票上直接支付, 也可以付款。
    在此登记, :menuselection:`Purchases --> Payments`.  
    然后在采购发票上直接核销.

打印供应商支票
----------------------

如果你选择用支票支付你的供应商。
Odoo提供一个方法直接从你的供应商付款来做。
不管你每日做，还是在每周结束时做，你总是可以批量打印支票。

如果你要打印支票,Odoo仪表盘有一个待办事项清单,提醒你还有多少需要打印。

.. image:: ./media/vendor_bill02.png
   :align: center

通过选择支票的数量, 可进到准备付款的一个列表。

选择需要打印的所有支票(使用第一个复选框, 选择所有), 并设置 **打印支票**.
Odoo将要求您设置打印序列, 之后将打印所有的支票。

.. image:: ./media/vendor_bill03.png
   :align: center

报告
=========

到期应付余额
--------------------

为了获得开放供应商账单及其相关到期日的列表，
您可以使用报告菜单下的 **应付账款报告**（在 :menuselection:`报告 --> PDF报告 --> 到期的业务伙伴余额`）来获取所有未清账单的视觉效果。

.. image:: ./media/vendor_bill04.png
   :align: center

从这里，您可以直接点击供应商名称，以打开所有未结帐单和应付金额的详细信息，
或者您可以注释管理信息的任何行。
在查看报表时的任何时间点，您可以直接打印到Excel或PDF，
并准确地看到您在屏幕上看到的内容。

在ODOO社区版只有直接导出为pdf格式的，无EXCEL表格导出功能

.. seealso::
    * :doc:`customer_invoice`
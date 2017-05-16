================================
如何设置一个新的银行账户？
================================

在Odoo，您可以管理多个银行帐户。在此页面中，将引导您创建，修改或删除银行或信用卡账户。

编辑银行帐户
--------------------

为了简化这一过程, 银行账户已经存在。我们建议你在填写银行信息前先编辑它。

 :menuselection:`Accounting --> Configuration --> Bank
Accounts` 转到会计‣配置‣银行账户，然后单击银行项目。编辑它

.. image:: media/image04.png
   :align: center

.. note::

    Odoo将检测银行账户类型(例如 IBAN), 允许类似于SEPA等的支付方式


创建银行账户
---------------------

Go to :menuselection:`Accounting --> Configuration --> Bank
Accounts`. Click on **create** 转到会计‣配置‣银行账户。点击 创建 和填写表格。你可以决定在文件上显示银行帐号, 就如销售订单或发票。选择银行账户的支付方式。

.. image:: media/image06.png
   :align: center

.. note::

    如果你在多公司环境内工作, 如你添加、编辑或删除银行账号, 需要在首选项中切换公司。

.. demo:fields:: base.action_res_partner_bank_account_form

.. demo:action:: base.action_res_partner_bank_account_form

   View *Bank Account* in our Online Demonstration

.. todo:: add inherited field tooltip

    **Display on reports :** Display this bank account on the documents that
    will be printed or send to the customers

    **Bank Identifier Code** = BIC : SWIFT Address assigned to a bank in
    order to send automated payments quickly and accurately to the banks
    concerned

The initial balance of a bank statement will be set to the closing balance of the previous one within the same journal automatically.

删除银行帐户或信用卡帐户
--------------------------------------------

从银行账户列表中, 选择要删除的项, 从行动菜单删除它们, 或者去表单和在行动菜单中删除

.. |image5| image:: media/image05.png
	:class: btn-group


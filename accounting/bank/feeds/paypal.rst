=================================================
在Odoo如何同步你的PayPal账户?（付费企业版，中国不适用）
=================================================

使用Odoo, 可以同步你的PayPal账户。
这样, 你不需要在你喜爱的会计软件里记录所有你的PayPal交易了。
每4小时同步完成, 您点击一下就可以开始调节PayPal支付了。

配置
=============

安装 account_yodlee 模块
----------------------------------

首先请安装 account_yodlee 模块,如果尚未安装。要做到这一点,到菜单 
:menuselection:`Accounting --> Configuration --> Settings` 。
在 银行和现金 这部分,设置选项 **Bank Interface - Sync your bank feeds automatically**.

.. image:: media/paypal01.png
    :align: center

完成后点击使用按钮

设置你的PayPal帐户
-------------------------

在Odoo, PayPal账户的管理就像一个银行账户。设置你的PayPal账户, 使用菜单
 :menuselection:`Configuration --> Bank Accounts`.
创建一个新的银行账户并命名为 **PayPal**. 在银行领域, 可以设置 **PayPal**.

.. image:: media/paypal02.png
    :align: center

一旦创建PayPal帐户, 回到 **Accounting** 仪表板, 点击 **Synchronize** button. 
在对话框中, 选择  **PayPal** 作为在线机构和点击配置按钮。

.. image:: media/paypal03.png
    :align: center

然后, 你必须提供连接到PayPal的凭证。

.. note::

	你的Paypal  **must be in English**  (如果它不是这样, 你必须改变你的Paypal账户), 如果你使用Paypal业务帐户必须切换回旧的接口才能使用在线提交(从新老界面可以切换你的Paypal账户)。

	如果你不这样做, 你会得到一个消息, 要么说把Paypal切换成英文要么不支持该网站。

如果你正确地配置您的Paypal帐户, 你应到下一步的在线提交配置。有一个屏幕显示获取交易的日期和供选择账户的列表。你必须选择 Paypal balance 帐户。

Once everything is done, you should see your PayPal transactions right
in Odoo and you can start reconciling your payments.

一切都完成之后, 在Odoo中, 你应该看得到你的PayPal交易, 你可以开始调节你的付款了。

.. note::
    你只需在第一次提供你的凭证。一旦完成, Odoo将与PayPal 每4个小时自动同步。

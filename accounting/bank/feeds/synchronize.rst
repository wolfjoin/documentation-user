=======================================
如何与银行同步odoo？（付费企业版功能，中国不支持）
=======================================

Odoo能够每4小时直接获得所有银行对账单并自动导入Odoo, 与你的银行同步。在做这步之前, 你应该检查你的银行是否对予支持。你可以从“Odoo会计中找到相关功能” `Odoo Accounting Features <https://www.odoo.com/page/accounting-features>`__

.. image:: media/synchronize01.png
   :align: center

在上面的页面中寻找你银行的名字。如果你的银行出现在其中, 这意味着它受Odoo支持。
完全支持的国家(即超过95%的银行)包括 :美国、加拿大、新西兰、奥地利。
30多个国家部分支持, 包括: 哥伦比亚、印度、法国、西班牙等。

为了与银行连接, Odoo 使用两个 web-services :

-  Plaid：美国的主要银行

-  Yodlee : 对于其他银行

配置
=============

Odoo 在线用户
-----------------

如果我们支持你们国家的银行, 银行特性应该已经被安装集成。如果没有安装, 您可以手动安装模块 **account_yodlee**.

Odoo 企业用户
---------------------

如果你计划使用Odoo企业版中的银行接口, 你不需要做什么特别的, 
只是确保数据库已在Odoo企业合同注册。


.. note::
   你可能需要检查一下, 没有防火墙/代理屏蔽以下地址
   
   * https://onlinesync.odoo.com/
   * https://api.plaid.com/


同步银行费用
====================

一旦Plaid或Yodlee接口安装后, 您可以将Odoo连接到你的银行。这样做, 
在银行会计仪表板上点击 More 。在菜单中, 单击设置配置该银行账户。

.. image:: media/synchronize02.png
   :align: center

在银行界面, 从银行帐户选项卡, 设置银行选项为 **Bank Synchronization**.

.. image:: media/synchronize03.png
   :align: center

一旦完成, 回到你的会计仪表板。在你的银行卡上, 您应该能看到一个
**Online Synchronization** 的按钮. 点击这个按钮, 填写你的银行凭证。

一旦你填写了你的凭证,你的银行订阅将会每4小时进行一次同步。

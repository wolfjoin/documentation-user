==========================================================
如何将日历与Google日历同步（国内目前无法访问谷歌，需翻墙）
==========================================================

- 连接到您的Google帐户，然后访问 `https://console.developers.google.com/ <https://console.developers.google.com/>`_.

- 单击 **+** **创建项目**...并输入项目名称，如果需要，更改您的ID。不要忘记接受服务条款

.. image:: media/google_calendar_credentials01.png
    :align: center

- 在顶侧的菜单中，选择子菜单API（从菜单API和auth），然后单击“Calendar API”。
  通过点击蓝色按钮“启用”激活日历API。
  完成后，Calendar API概述将可用

.. image:: media/google_calendar_credentials02.png
    :align: center

.. image:: media/google_calendar_credentials03.png
    :align: center

.. image:: media/google_calendar_credentials04.png
    :align: center

-  **创建凭据**


.. image:: media/google_calendar_credentials05.png
    :align: center

- 您从哪里调用 API？选择 '网络浏览器（Javascript)', 您要访问哪些数据？选择“用户数据”，
  接着点击“我需要哪些凭据”，跳转到下一个窗口，输入odoo网址（如果包含非标准端口比如8069也需要
  输入）。


.. image:: media/google_calendar_credentials06.png
    :align: center

.. image:: media/google_calendar_credentials07.png
    :align: center

您现在应该配置将被重定向到的允许页面。要做到这一点，您需要填写"Authorized redirect URI"
“授权重定向URI”字段并设置为值（您自己的域后跟'/ google_account / authentication'）：==> 
http://mydomain.odoo.com/google_account/authentication 您现在可以点击“创建客户端ID”

.. image:: media/google_calendar_credentials08.png
    :align: center

- 一旦完成，您将有两个信息（客户端ID和客户端密码），您需要插入下面的2个字段！
  （点击创建的谷歌凭据，查看ID、密码信息）

.. image:: media/google_calendar_credentials09.png
    :align: center

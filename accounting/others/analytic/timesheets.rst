======================================================
如何使用工时表跟踪人力资源成本？
======================================================

人力资源当然是有成本的。有趣的是, 多大的一个特定的人力合同成本, 
公司会将成本关联到相应发票金额。

我们采用以下例子 :我们两位雇员 **Harry Potter** and
**Cedric Digory** 都为我们的客户 **Smith&Co** 提供  **Consultancy pack** 工作.
 Harry 每小时支付18€. and Cedric 的工资是每小时 12€ .
 我们用会计应用中跟踪他们的工时费, 并比较他们咨询服务收益。


配置
=============

首先, 安装必要的三个应用程序, 即 **会计Accounting**, **销售Sales** and **工时表Timesheet**. 
进入应用程序模块, 并安装它们。

.. image:: media/timesheets14.png  
   :align: center

.. image:: media/timesheets05.png
   :align: center

.. image:: media/timesheets11.png
   :align: center

接下来您将需要启用分析会计。这样, 进入
**会计Accounting**. 选择  :menuselection:`配置Configuration --> 设置` 和点击
**采购的分析会计（社区版）Analytic accounting** 选项(见下图)

.. image:: media/timesheets06.png
   :align: center

应用变更。

创建员工
------------------

为了检查员工的收入, 你需要有一个。进入 **员工Employee** 创建一个员工。
选择 **员工Employees** , 并创建一个新员工, 填写名称和基本信息。

在员工表上进入 **HR设置HR settings** 选项卡。
在这里你可以指定员工的 **工时表成本Timesheet Cost** 。
在这种情况下, Harry花费18欧元/小时。在这个字段我们将填写18。

.. image:: media/timesheets07.png
   :align: center

.. note:: 
    如果你希望员工能够进入工时表, 他需要设置相关用户。

重复操作, 创建员工Cedric Digory。别忘了指定相关用户和 **工时表成本Timesheet Costs**.

发布销售订单 
--------------------

我们在 员工（Employee） 创建了两个员工, Harry Potter 和 Cedric Diggory。
他们将为Smith&Co 工作, 他们会将工时填入咨询合同。

因此我们需要创建一个 销售订单 **sales order** , 产品是 服务 **service** , 基于时间和材料 开票, 公式以小时为单位。

.. image:: media/timesheets03.png
   :align: center

有关如何根据时间和材料创建销售订单的更多信息，请参阅: *如何根据时间和材料开具发票*（正在进行中）。

.. todo::
    Add a link, and the document is under 
    Sales --> Invoicing Methods --> Services --> How to invoices blabla

We save a Sales Order with the service product **External Consulting**. An
analytical account will automatically be generated once the **Sales Order**
is confirmed. Our employees will have to point to that account (in this
case **SO002-Smith&Co**) in order to be able to invoice their hours (see
picture below).
我们保存一个销售订单, 订单内产品为 "External Consulting" . 销售订单一旦确认, 分析科目会自动生成。我们的员工将被指定一个科目(在本例中 SO002-Smith&Co ), 是为了将工时开票给客户(见下图)。

.. image:: media/timesheets10.png
   :align: center

填写工时表
-----------------

一个员工链接到一个用户, Harry可以进入 工时表 应用, 为工时单指定相应的合同。登入Harry的帐户, 进入 Timesheet 应用程序, 输入明细行, 指定上面所讨论的 分析账户 。

Harry 为Smith&Co付出了三个小时的SWOT analysis。

.. image:: media/timesheets01.png
   :align: center


同时, Cedric与客户讨论需要1小时, 指定到他个人的工时表, 也指向 Analytic Account .

在 **销售订单** 中, 我们注意到交付的时间会自动计算(见下图)。

.. image:: media/timesheets02.png
   :align: center

分析会计
-------------------

由于分析科目, 我们能够对人力资源成本和收入有个总的概念。所有交易的收入和成本都将登记在  **SO002-Smith&Co** 科目.

在该情景下我们可以使用两种方式。

不要过滤
~~~~~~~~~~~~~~~

如果所有项目的成本和收入的分析科目都正确, 我们可以轻松地检索相关的成本和收益。输入  *Accounting* 应用, 选择 
:menuselection:`顾问Adviser --> 分析账户Analytic Accounts --> 打开Open Charts`.

注意 :您可以为 **Analysis** 指定一个时间。如果你想打开当前状态, 你应该保持空的字段。我们可以看到借贷方余额。

.. image:: media/timesheets12.png
   :align: center

如果我们单击科目, 提供了成本和收入的细节(见下图)。

.. image:: media/timesheets13.png
   :align: center

点击按钮 **成本/收入Cost/Revenue** 可以了解成本和收入的相关描述。

带过滤器
~~~~~~~~~~~~

因此我们可以在 **分析分录 Analytic Entries** 中过滤该信息。

进入**会计Accounting** 程序, 点击 :menuselection:`顾问Adviser --> 分析分录Analytic Entries`.
在这个菜单中, 我们有几个选项来分析人力资源成本。

1. 筛选 **分析账户Analytic account** , 我们可以看到项目的成本和收入。添加一个自定义的 过滤器: **分析账户Analytic Account** 包括  **销售订单Sales Order**

   .. image:: media/timesheets04.png
      :align: center

   结果, 我们看到时间表活动, 和成本和收入的相关开票行。

   .. image:: media/timesheets09.png
     :align: center

2. 我们可以组合不同的分析科目, 检查各自的收入。简单的组合 分析账户 并选择 图形视图 , 会提供一个清晰的概况。

   .. image:: media/timesheets08.png
      :align: center

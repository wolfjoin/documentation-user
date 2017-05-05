===========================
Odoo用户使用说明1
===========================

创建环境要求:

* Python 2.7
* 最新的 `Sphinx <http://sphinx-doc.org>`_ (至少 Sphinx 1.2)

  您可以通过尝试启动来检查是否安装了Sphinx

  .. code-block:: console

     $ sphinx-build --version

  有关 本地安装说明，请参阅 `sphinx 文档 <http://sphinx-doc.org/install.html>`_
  
* `git <http://www.git-scm.com>`_ 

* 使用git克隆该存储库，然后在存储库的根目录中，在控制台中，
  
  .. code-block:: console

     $ make html

  这应该将文档编译成HTML，并将生成的HTML放入 ``_build/html/index.html``.

贡献
=============

对于简单版（打字错误，只需添加不带标记的文本段落），可以直接使用Github Web界面。

对于更复杂的版本，要添加图像或高级指令，请在本地编辑。如果在构建文档时首先出现警告或错误，请勿提交。
rST对空格和换行符非常敏感（特别是缺少换行符）。这有点烦人，但不难学习。

问题可以像往常一样在存储库的错误跟踪器上报告。

自定义功能
===============

扩展
----------

提供了两个定制指令，用于与Odoo的演示系统集成：

* ``demo:fields:: {external_id}`` 使用工具提示 (``help``) 列出所有字段提供``external_id`` .

  - 默认使用视图``form`` , 通过使用``:view:``.进行自定义。
  - ``:only:``显示的字段列表可以被过滤，应该是要显示的空格分隔字段的列表。请注意，这将进一步减少显示的字段数量，
  当没有 ``help``不会强制字段在列表中。

  .. code-block:: restructuredtext

     .. demo:fields:: account_asset.action_account_asset_asset_list_normal_sale
        :only: name

 这将只显示 ``name`` 和 ``help`` (如果 ``name`` 没有``help``，则不显示)字段的表

* ``demo:action:: {external_id}`` 将在演示网站上创建链接按钮(由外部ID指定 ). 
该按钮的文本应作为指令的内容提供:

  .. code-block:: restructuredtext

     .. demo:action:: account_asset.action_account_asset_asset_list_normal_sale

        View *Asset Types*

主题自定义
--------------------

* Odoo主题支持文档顶部的 *Banner Images* 。 
这些横幅是通过在文档顶部设置一个字段（在页面标题之前） ``:banner:``来设置的, 
  横幅图像将在项目根目录下的文件夹``_static`` 中查找 
  .. code-block:: restructuredtext

     :banner: banners/accounting.png

     ==========
     Accounting
     ==========

     [...]

  .. 警告::

     因为横幅图 banners是比较宽的图片，每个页面可能只有一张，强烈建议压缩下。
     对于PNG,使用
     `pngquant <https://pngquant.org>`_ (or a UI to it) 减少图像中像素,
    常规的PNG重新压缩工具，如
    `pngcrush     <http://pmt.sourceforge.net/pngcrush/>`_ 和 `pngout
     <http://www.advsys.net/ken/util/pngout.htm>`_.



导入现有文档
============================

对于已经以其他格式或Google文档存在的文档，
可以通过使用`Pandoc <http://pandoc.org>`_转换现有文档来开始.
主要问题是除了微不足道的原始文档需要修改来适应rST.


例子::

  pandoc -f docx -t rst path/to/document.docx -o new_doc.rst --extract-media=.

将 ``path/to/document.docx`` 转换 成``new_doc.rst`` 并且导出所有图像到 ``./media`` (从文件链接他们). 
虽然导出的文档有问题，但是比手动重新输入原件更方便。

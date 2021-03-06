# 通过SQL条件过滤待迁移数据 {#concept_610729 .concept}

在配置数据迁移任务的迁移对象时，您可以设置SQL过滤条件，过滤待迁移数据。只有满足过滤条件的数据才会被迁移到目标数据库。该功能可应用于数据的定期增量迁移、拆分数据表等多种应用场景。

## 功能限制 {#section_sls_2xb_b3b .section}

SQL过滤条件只作用于全量数据迁移阶段，不会作用于增量数据迁移阶段。

## 操作步骤 {#section_npm_fxb_b3b .section}

配置数据迁移任务时，在设置**迁移类型及列表**

1.  将要迁移的对象移动到已选择区域框中后，把鼠标指针放置在要修改的数据表上，并单击数据表后出现的**编辑**。

    ![选择表](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/17121/156091550249113_zh-CN.png)

2.  在弹出的**编辑表**对话框中，填入**过滤条件**。

    ![配置SQL过滤条件](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/17121/156091550349114_zh-CN.png)

    **说明：** 过滤条件支持标准的SQL WHERE语句，只有满足WHERE条件的数据才会被迁移到目标数据库中。本案例填入`orderid>100`。

3.  单击**验证语法**，确认语法正确性。

    **说明：** 

    -   如果语法正确，则弹出提示对话框，并显示**验证通过**。
    -   如果语法错误，则弹出错误对话框，您需要根据对话框中的提示，对WHERE语句进行调整。
4.  单击**确定**。
5.  根据提示，完成后续的数据迁移任务配置。


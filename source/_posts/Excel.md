---
title: Excel函数
---

> 1、count()函数 //统计某一列的个数

> 2、="'"&A1&"'," //给某一列加引号，用于sql查询

> 3、=RIGHT(A2,11) //PBM_HANSI：发送TPA理赔数据异常 可以将列分离 ，从右边截取 分离后 发送TPA理赔数据异常  =LEFT(A2,11) //从左边截取

> 4、=CONCAT("update jy_collaborate_mis.coll_stmt_collection_task set remark = '提交成功' where id ='"&A1&"';") 拼接sql // =CONCAT(""&A1&"")

> 5、=VSTACK(吴国!A1:C17,蜀国!A2:C17,魏国!A2:C17) //=VSTACK（）合并多个表格数据到一个表格 注意：每选择一个表格数据之后，公式后面要加一个,    都选择完成之后点击对号

> 6、ctrl+D //向下填充
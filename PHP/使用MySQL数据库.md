﻿# 5.使用mysql数据库

 __首先确保自己已经了解SQL的相关内容__
 
###建立连接
	我大概倾向于用mysqli
	面向过程的写法: $db=mysqli_connect('hostname','usename','password','database');
	面向对象的写法: $db=new mysqli('hostname','usename','password','database');
	
###选择使用的数据库
	$db->select_db(db_name);
	mysqli_select_db(db_resource,db_name);

###查询数据库
	$query="select * from dbname where ".$type." like '%".$item."%'";
	$result=$db->query($query);
	或$result=mysqli_query($db,$query);

###检测查询结果
	$num_result=$result->num_rows;
	$num_result=mysqli_num_rows($result);
	
	$fetch_row $fetch_array什么的……
	
###关闭数据库
	$db->close();
	mysqli_close($db);
	
 __面向过程的写法就该离开世界啊……__

## PHP判断文件是否存在，是否可读，目录是否存在

- 1.文件是否可读

`is_readable()` 函数判断指定文件名是否可读. 
指定的文件或目录存在并且可读,则返回 `TRUE`

	<?php 
	$file = 'jb51.net.php'; 
	if (is_readable($file) == false) { 
		die('文件不存在或者无法读取'); 
	} else { 
		echo '存在'; 
	} 
	?> 

- 2.检查文件或目录是否存在 

`file_exists ( string filename )`
如果由 filename 指定的文件或目录存在则返回 TRUE,否则返回 FALSE. 

	<?php 
	$filename = 'jb51.net.php'; 
	if (file_exists($filename)) { 
		echo "The file $filename exists"; 
	} else { 
		echo "The file $filename does not exist"; 
	} 
	?> 

- 2-1.目录是否存在 

`is_dir`:目录是否存在

	if(is_dir($dir))
	{
	    echo "当前目录下，目录".$dir."存在";
	}
	else
	{
	     echo "当前目录下，目录".$dir."不存在";
	}


- 3.判断给定文件名是否为一个正常的文件

`is_file ( string filename)` 
如果文件存在且为正常的文件则返回 TRUE.

	<?php 
	$file = 'jb51.net.php'; 
	if (is_file($file) == false) { 
		die('文件不存在或者无法读取'); 
	} else { 
		echo '存在'; 
	} 
	?> 



- 4.删除文件

`unlink ( string $filename  )`
参数$filename 表示文件的路径，可以是相对路径也可以是绝对路径。

> 另外删除目录用函数：`rmdir()`；用法与`unlink ()`相同

- 5.创建文件夹

`mkdir()` 函数创建目录。
若成功，则返回 `true`，否则返回 `false`。

mkdir(path,mode,recursive,context)

参数  	  | 描述
----------|------
path	  | 必需。规定要创建的目录的名称。 
mode	  | 必需。规定权限。默认是 0777。  
recursive | 必需。规定是否设置递归模式。
context   | 必需。规定文件句柄的环境。Context 是可修改流的行为的一套选项。
如果需要获取本机的rsa文件
在windows 上 可以打开 C:\Users\用户名\.ssh 中查看id_rsa 和 id_rsa.pub
linux 可以通过命令 cat ~/.ssh/id_rsa.pub

生成id_rsa文件
可以使用命令
ssh-keygen -t rsa -C "邮箱名"
代码参数含义：

-t 指定密钥类型，默认是 rsa ，可以省略。
-C 设置注释文字，比如邮箱。
-f 指定密钥文件存储文件名。

检查ssh是否可以连接git
ssh -T git@github.com


生成完成后，可以通过 cd 进入到对应的目录中，将id_rsa.pub 复制到git的ssh管理中。

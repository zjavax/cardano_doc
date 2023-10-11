#cardano节点长时间不恢复

创建文件：

`touch $CNODE_HOME/db/clean`        

删除文件：
`rm -f $CNODE_HOME/db/clean`

原因：

简单的说, 就是在 db 路径下新建一个名为`clean`的空文件。节点启动的时候检查到有这个文件就会跳过自检。

但以上方法慎用，当你无法保证数据正确完整的时候跳过自检可能导致自己的chain db 进入错误的分叉

guagua哥解决：https://gen8.orz.com.cn/blog/index.php/archives/380/










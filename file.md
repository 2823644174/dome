.版本 2
.支持库 iext
.支持库 spec

.子程序 刷新文件
.参数 路径, 文本型
.局部变量 文件名, 文本型
.局部变量 数组, 文本型, , "0"
.局部变量 索引, 整数型

超级列表框1.全部删除 ()

文件名 ＝ 寻找文件 (路径 ＋ “\*.txt”, 32 ＋ 16 ＋ 4 ＋ 2 ＋ 1)
.判断循环首 (文件名 ≠ “”)
    索引 ＝ 超级列表框1.插入表项 (, , , , , )
    超级列表框1.置标题 (索引, 0, 到文本 (索引 ＋ 1))
    超级列表框1.置标题 (索引, 1, 取文本左边 (文件名, 取文本长度 (文件名) － 4))
    超级列表框1.置标题 (索引, 2, 路径 ＋ 文件名)
    文件名 ＝ 寻找文件 (, 32)
    加入成员 (数组, 文件名)

.判断循环尾 ()
调试输出 (数组)

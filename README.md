# HyperBackup更新日志
用Python写的文件备份脚本
> 环境：` Windows 10 64.bit `, ` Python 3.6.4 `


>文件备份的小项目基本完成—————2018.06.09


***

2018.06.09

V0.1.5
内容：
 1. 修复：修复logging 输出日志文件时，报错UnicodeEncodeError
 2. 添加：备份指定格式的文件（.mp3, .pdf, .jpg, .） 已完成 2018.06.07
 3. 不单独写scriptinfo
 4. 优化




***

2018.06.08

V0.1.3
内容：
 1. 修复：多级目录问题: 已修复2018.06.07
 2. 添加：详细备份日志，以单独的文本输出。 已添加2018.06.07
 3. 添加：对有改动的文件，执行备份，保留原有文件，以备份时间为命名方式。已添加2018.06.07
 4. 添加：统计文件总数，已备份数量。 已添加2018.06.07
 5. 添加：备份耗时记录
 6. 编译成可执行文件EXE

 7. 遗留问题：备份时提示`--- Logging error ---`,写入日志错误，但不影响文件备份
 `UnicodeEncodeError: 'gbk' codec can't encode character '\xa0' in position 56: illegal multibyte sequence`




***

2018.06.06

V0.1.1
内容：
 1. 实现文件备份功能（源文件地址 old_source, 备份地址 new_source ）
 2. 备份选项：
    00 --- 初次备份：简单粗暴直接复制文件夹
    11 --- 更新备份：遍历每个文件夹每个文件，计算每个文件的MD5值，比对MD5值，查找文件变动，如文件有改动则执行备份
 3. 空文件夹处理:
    标出空文件夹(打印出)
 4. 对于隐藏文件也进行备份，但备份后不再隐藏

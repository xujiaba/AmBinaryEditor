# AmBinaryEditor

AndroidManifest Binary Editor

http://ele7enxxh.com/AndroidManifest-Binary-Editor.html

## 用法示例：
**增加一个tag（-d选项指定新增tag的起始位置，如1表示添加在manifest节点之后；-c选项指定新增tag经过的节点数，以此确定新增tag的结尾位置）：**

editor tag --add activity -d 1 -c 0 -i input.xml -o output.xml

**改一个tag的名字（-d选项指定要修改的tag是从manifest节点开始出现的第几个同名tag，-n选项指定tag的新名字）：**

ameditor tag --modify application -d 1 -n test -i input.xml -o output.xml

**删除指定tag（-d选项指定要修改的tag是从manifest节点开始出现的第几个同名tag）：**

ameditor tag --remove application -d 1 -i input.xml -o output.xml

**增加一个attr（-d选项指定要修改的tag是从manifest节点开始出现的第几个同名tag，-n选项指定attr的名字，-t选项指定attr的类型（后面会有更多介绍）-v选项指定attr的值，-r选项指定attr的属性ID（可选））：**

ameditor attr --add application -d 1 -n name -t 3 -v test -i input.xml -o output.xml

**修改一个attr（-n选项指定需要修改的attr，其他同上）：**

ameditor attr --modify application -d 1 -n name -t 3 -v new -i input.xml -o output.xml

**批量修改某attr（-n选项指定需要修改的attr，-p 表示需要被替换的值，-v表示新值）：**

ameditor a --batch provider -n authorities -t 3 -p com.vbooster.vbooster_private_space -v com.vbooster.wxtest -i AndroidManifest.xml -o output.xml
**或**
ameditor a --batch activity -n taskAffinity -t 3 -p com.vbooster.vbooster_private_space -v com.vbooster.wxtest -i AndroidManifest.xml -o output.xml

**删除一个attr（-n选项指定需要删除的attr，其他同上）：**

ameditor attr --remove application -d 1 -n name -i input.xml -o output.xml
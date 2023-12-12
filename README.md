https://www.cnblogs.com/xieshengsen/p/6727064.html
# test
test  description
python os.walk 用法  topdown=False
![图片](https://github.com/yanzhou1618/test/assets/36185388/f1aa6a58-af5a-477d-879c-c0ab24a10df1)
# 使用os.walk自底向上扫描目录
import os

for curDir, dirs, files in os.walk("test", topdown=False):
    print("====================")
    print("现在的目录：" + curDir)
    print("该目录下包含的子目录：" + str(dirs))
    print("该目录下包含的文件：" + str(files))
![图片](https://github.com/yanzhou1618/test/assets/36185388/c38960c8-47da-4987-b884-08c5bcc2f153)


也可以利用os.walk输出test文件夹下指定后缀名（比如.txt）文件：
# 使用os.walk输出某个特定后缀(比如.txt)的文件
import os

for curDir, dirs, files in os.walk("test"):
    for file in files:
        if file.endswith(".txt"):
            print(os.path.join(curDir, file))


同样地，我们也可以利用os.walk输出test文件夹下所有的子目录（子文件夹）：
# 使用os.walk输出所有的目录
import os

for curDir, dirs, files in os.walk("test"):
    for dir in dirs:
        print(dir)



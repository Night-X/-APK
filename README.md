# -APK
反编译（mac版，windows只需要将命令换成对应的 .bat即可）
[反编译工具下载地址](https://ibotpeaches.github.io/Apktool/)
1. 获取资源文件：
    打开命令行，进入apktool文件夹，将apk拷贝到该文件夹下，输入命令：apktool d -f xxx.apk -o xx (xx为资源所存放的文件夹)。
    如果你想将反编译完的文件重新打包成apk，那你可以：输入apktool.bat   b    test（你编译出来文件夹）便可。
2. 得到JAVA源代码（这里得到的是经过混淆后的代码）
    将apk用解压文件打开并解压，得到其中的额classes.dex文件（它就是java文件编译再通过dx工具打包而成的），将获取到的classes.dex放到之前解压出来的工具dex2jar-0.0.9.15 文件夹内，命令行定位到该文件夹下，输入：./ dex2jar.sh classes.dex，在改目录下会生成一个classes_dex2jar.jar的文件，然后打开工具jd-gui文件夹里的jd-gui.exe，之后用该工具打开之前生成的classes_dex2jar.jar文件，便可以看到源码了。

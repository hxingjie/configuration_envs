## 1.完成编译环境

[MinGW-w64](https://www.mingw-w64.org/)

[MinGW-w64 - for 32 and 64 bit Windows - Browse /mingw-w64/mingw-w64-release at SourceForge.net](https://sourceforge.net/projects/mingw-w64/files/mingw-w64/mingw-w64-release/)

![image-20230714092541124](https://github.com/hxingjie/configuration_envs/assets/66415951/b83f17b2-9a6a-4d63-b363-e411a041bf2c)


下载x86_64_win32_seh

高级系统设置中配置环境变量,如图最后一行

![image-20230714092835545](https://github.com/hxingjie/configuration_envs/assets/66415951/8171d092-8efd-4ffc-9d0a-21f80c595a8f)


## 2.VSCode设置

安装扩展

![image-20230714092957876](https://github.com/hxingjie/configuration_envs/assets/66415951/1691c6a4-466f-4a7f-a481-01ed5875b578)


新建文件夹，打开文件夹

ctrl+shift+p 打开>C/C++:Edit Configurations (UI)

![image-20230714093041429](https://github.com/hxingjie/configuration_envs/assets/66415951/c90c4709-77f7-4a07-acf1-5adf03ece8df)


![image-20230714100401056](https://github.com/hxingjie/configuration_envs/assets/66415951/60e35c54-0102-44a8-89b3-0193463d74f9)


compiler path: C:\Application\envs\mingw64\bin\g++.exe

intellisense mode: windows-gcc-x64

创建.cpp文件

```c++
#include <iostream>
using namespace std;

int main(){
    cout << "hello" << endl;

    return 0;
}
```

![image-20230714101027877](https://github.com/hxingjie/configuration_envs/assets/66415951/c657ddda-5c92-4a14-b76c-725c6480bb49)


![image-20230714101049615](https://github.com/hxingjie/configuration_envs/assets/66415951/950135ae-d9f2-46da-b41d-45a5f00ad38d)


![image-20230714101109603](https://github.com/hxingjie/configuration_envs/assets/66415951/ff00133c-7551-45a6-9501-f2197b9ef82b)


![image-20230714101130080](https://github.com/hxingjie/configuration_envs/assets/66415951/80fb5c17-6276-48f1-81fe-a5f33bae0f40)



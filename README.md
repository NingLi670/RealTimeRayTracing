## Real-Time Ray Tracing
### 部分文件说明
* `RealTimeRayTracing\src`：源代码
* `RealTimeRayTracing\assets`：模型、贴图以及着色器代码

### 从可执行文件运行
#### 要求
* Windows10/11
* [Visual Studio 2019](https://blog.csdn.net/qq_45662588/article/details/122761200)
  
#### 运行
* 双击`RealTimeRayTracing\EXE\rt\Debug\rt.exe`启动程序
* 双击`RealTimeRayTracing\EXE_WITHOUT_MODEL\rt\Debug\rt.exe`启动未导入网格模型的程序

如果直接运行.exe程序不能正常加载光线追踪场景，这是因为OpenGL相关库依赖较为复杂，请通过下面的编译方式运行。
### 从项目文件编译运行（推荐）
#### 要求
* [CMake (>= 3.0.2)](https://blog.csdn.net/qq_42598221/article/details/121952160)
* GPU (提供OpenGL(>=3.3)支持)
* GLM (已包含在项目文件中)
* GLFW (Linux: `sudo apt install libglfw3-dev`; Windows系统不需额外安装，需要装有Visual Studio 2019)

#### 编译
以下指令中的`bin`文件夹也可以使用其他名字
```sh
cd RealTimeRayTracing
mkdir bin
cd bin
cmake ..
cmake --build .
```
#### 运行
* 将`RealTimeRayTracing\assets`文件夹复制到`RealTimeRayTracing\bin\rt\Debug`目录下，双击`RealTimeRayTracing\bin\rt\Debug\rt.exe`开始运行
* 也可以在Visual Studio 2019中打开工程文件`RealTimeRayTracing\bin\RayTracing_OpenGL.sln`进行调试运行，同时要将`RealTimeRayTracing\assets`文件夹复制到`RealTimeRayTracing\bin`目录下


### 运行时的镜头控制
- 使用鼠标改变相机的方向
- 使用键盘上的`Esc`键退出
- 使用键盘上的`W S A D Space Ctrl`键控制前后左右上下的移动
- 同时按住`Shift`键加快移动速度，同时按住`Alt`键减慢移动速度


### Reference
https://github.com/engilas/raytracing-opengl
https://github.com/AKGWSB/EzRT


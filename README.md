# 简介

构建面向RISC-V的操作系统(RVOS)。

- 支持: RVOS Linux、RVOS Yocto嵌入式Linux、RVOS ISCAS-FreeRTOS嵌入式等版......, 面向不同场景的版本共享同一套共同维护的RVOS核心源码。
- 支持: C/C++、Python3等运行时环境，[腾讯NCNN](https://github.com/Tencent/ncnn)、[TensorFlow Lite](https://github.com/tensorflow/tensorflow)等神经网络编程框架, Yolov3目标检测等神经网络推理应用, Nginx等服务, 性能优化, 模型压缩等, 持续更新。
- 打造OS的新型架构模式、新型构建模式, 进行中......

## RVOS-rvos

使用说明。

**引导**
  - 如果硬件环境为QEMU-RV64模拟器: 使用`rvos/boot`目录下`bbl.payloaded`, 其payload是`vmlinux.5.1.y.aspayload (Linux version 5.1.15)`。
  - 如果硬件环境为SiFiVE HiFive板卡: 使用`rvos/boot`目录下`uboot.bin`, `bbl.bin`, `vmlinux.bin`, `hifiveu.fit`, 和`uEnv.txt`，并设置MicroSD卡引导模式。
  - ......

**文件系统**
  - `rvos/rvos-minbase.tar.gz`: rvos的基础小根文件系统，为专用领用应用构建提供共享的基础小环境, 持续优化......
  - `rvos/rvos-gcc.tar.gz`: 提供C/C++运行时环境和编译开发环境的专用版本, 共享`rvos-minbase`。
  - `rvos/rvos-python.tar.gz`: 提供Python3运行时环境的专用版本, 共享`rvos-minbase`。
  - `rvos/rvos-nginx.tar.gz`: 提供Nginx服务运行环境的专用版本, 共享`rvos-minbase`, 持续更新面向边缘微服务运行环境; `注意:` 首次引导需执行`systemctl start nginx.service`启动Nginx后台服务进程,并执行`systemctl enable nginx.service`设置Nginx开机引导时启动。
  - `rvos/rvos-ncnn`: 提供腾讯ncnn神经网络框架,并集成了Yolov3等神经网络推理应用,基于`rvos-gcc`, 共享`rvos-minbase`; `注意:` 首次引导需执行`ldconfig`。
  - ......

## RVOS-iscasfreertos

## RVOS-rvosyocto

## RVOS-upstreamsrcs

将Fetch From [开源软件可靠供应链平台]()。

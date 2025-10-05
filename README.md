# build-artifacts-archive - 编译产物存档仓库说明

## 仓库概述
本仓库用于个人编译产物的存档与备份，包含 Linux、Windows 及 HarmonyOS 等多系统的各类编译产物，方便后续复用并避免重复编译。

仓库内容为个人自用，包含二进制文件、库文件及应用包等。

## 仓库结构

采用 "产物名 - 系统 - 指令集 - 字节位 - 版本" 的文件名命名规则，结合轻量目录结构进行组织：
```plaintext
build-artifacts-archive/
├─ README.md          # 本说明文件
├─ OpenSSL/           # 按产物名分类的目录
│  ├─ v1.1.1/         # 版本子目录
│  │  ├─ openssl-linux-x86_64-64bit.tar.gz
│  │  └─ openssl-win-x86_64-64bit.zip
│  └─ v3.2.0/
│     ├─ openssl-linux-x86_64-64bit.tar.gz
│     ├─ openssl-linux-arm64-64bit.tar.gz
│     └─ openssl-ohos-arm64-64bit-phone.hap
├─ Utils-Lib/
│  └─ ...
└─ App-Core/
   └─ ...
```
## 文件名命名规则

统一采用以下命名格式：`[产物名]-[系统标识]-[指令集]-[字节位]-[版本号].[后缀]`

## 系统标识
Linux: linux

Windows: win

HarmonyOS: ohos（鸿蒙系统需额外标注设备类型）

## 常见指令集

x86_64: 64 位 x86 架构

x86: 32 位 x86 架构

arm64: 64 位 ARM 架构

riscv64: 64 位 RISC-V 架构

## 字节位标识
64bit: 64 位

32bit: 32 位

## 示例文件名
|文件名|说明|
|--|--|
|openssl-linux-x86_64-64bit-v3.2.0.tar.gz | Linux 系统，x86_64 指令集，64 位，OpenSSL v3.2.0 版本|
|utils-lib-win-x86-32bit-v2.0.0.lib|Windows 系统，x86 指令集，32 位，Utils-Lib v2.0.0 版本|
|app-core-ohos-arm64-64bit-phone-v1.5.0.hap|HarmonyOS 系统，arm64 指令集，64 位，手机设备，App-Core v1.5.0 版本|
|driver-ohos-x86_64-64bit-sim-v2.0.0.so|HarmonyOS 系统，x86_64 指令集，64 位，模拟器，driver v2.0.0 版本|

## 产物信息说明

每个压缩包或产物目录中均包含info.txt文件，记录以下关键信息：

* 编译时间
* 编译器及版本（如 gcc 12.2、VS2022、DevEco Studio 4.0）
* 依赖库及版本
* 编译参数（关键配置）

## 版本管理
* 版本号遵循语义化版本规范：主版本.次版本.修订号（如 v1.0.0）

* 同一产物的不同版本通过版本子目录区分

* 重要更新会在本 README 的 "更新日志" 部分记录

## 更新日志

## 版权信息

本仓库内容为个人存档, 使用本仓库内容时，请保留原始项目版权信息。详细条款见仓库根目录的LICENSE文件。

## 注意事项

本仓库仅供个人存档使用

部分产物可能依赖特定系统环境，使用前请参考对应info.txt

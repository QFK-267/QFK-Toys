# QFK-Toys

一些小玩意 / 开源小工具

全部使用 **MIT License**

## 包含内容

### 1. μLang 编译器 (`mulang.py`)
极简图灵完备语言编译器，把 μLang 源码编译成 Python 再执行。  
虽然图灵完备但绝对不好用。

支持指令：
- `SET var value`
- `MOV dest src`
- `INC / DEC var`
- `ADD / SUB dest src`
- `JZ / JNZ var label`
- `OUT var` (输出 ASCII 字符)
- 标签 `label:`

运行示例：
```bash
python mulang.py
# 或
python mulang.py your_program.mul
```

### 2. Windows 版 sudo (`sudo.cpp`)
在 Windows 上实现类似 Linux 的 `sudo` 体验：
- 密码验证（3次尝试）
- 5分钟缓存
- 自动获取 SYSTEM / TrustedInstaller Token
- 自安装到 System32 并清理微软官方 sudo
- 支持以高权限运行任意命令

编译（MSVC）：
```bash
cl /EHsc /O2 sudo.cpp /link advapi32.lib user32.lib shell32.lib userenv.lib
```

### 3. AI版GCC解释器提示词 (`ai-gcc-prompt.md`)
给大模型用的纯模拟 GCC 编译器角色提示词。  
只输出编译报错或程序运行结果，支持输入处理。

## License
MIT

# BUTTON

这是一个目标为高可移植性的按键驱动库。支持按键的单击/双击/长按/持续长按(可配置)。需要设置按键询问函数和事件处理函数。另外为矩阵键盘做了一定的简化。

## 快速开始


### 添加库

将button文件夹拷贝到你的项目中的被includePath包含的文件夹中。
需要使用到该按键库的文件中添加include
```c
#include "button/button.h" 
```

### 使用

首先调用 button_init 对该按键库进行初始化

然后调用 set_button_query_func 设置按键的电平询问函数，调用 set_button_event_func 设置按键触发的事件函数。

最后将 button_turn_query 函数放在定时器内，每隔一段时间运行一次。触发周期和config文件中匹配。

可在 button_config.h 中进行一定的配置

button.h 和 button_config.h 中有详细注释

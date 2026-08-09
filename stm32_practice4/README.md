# 练习 4：按键控制蜂鸣器 | Practice 4: Button Control Buzzer

## 功能 | Function
- 使用阻塞式延时函数实现按键消抖。 | Use blocking delay function to implement button debouncing.
- 通过检测按键状态的改变来控制蜂鸣器。 | Control buzzer by detecting button state change.

## 硬件连接 | Hardware Connection
- BEEP 连接在 PA2 引脚。 | BEEP connected to pin PA2.
- KEY1 连接在 PC2 引脚。 | KEY1 connected to pin PC2.

## 功能说明 | Description
按下 KEY1 按键，蜂鸣器开始鸣叫（100ms响，100ms停）；
再次按下 KEY1，蜂鸣器停止鸣叫。
使用软件消抖机制确保按键检测的准确性。

Press KEY1 button to activate buzzer (100ms on, 100ms off);
Press KEY1 again to stop buzzer.
Software debouncing mechanism ensures accurate button detection.
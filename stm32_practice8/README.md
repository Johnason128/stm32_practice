# 练习 8：系统滴答定时器与中断闪灯 | Practice 8: SysTick Timer and Interrupt LED Blink

## 功能 | Function
- 使用系统滴答定时器（SysTick）中断实现LED定时闪烁。 | Use SysTick timer interrupt to implement timed LED blinking.
- 每500ms翻转一次LED状态，实现1秒周期的闪烁效果。 | Toggle LED state every 500ms to achieve a 1-second blinking cycle.

## 硬件连接 | Hardware Connection
- LED 连接在 PA1 引脚。 | LED connected to pin PA1.

## 功能说明 | Description
利用STM32的系统滴答定时器（SysTick），默认每1ms触发一次中断：
- 在中断服务函数中累计计数，当计数达到500次（即500ms）时，翻转LED引脚状态。
- 使用静态变量保持计数值，实现非阻塞的定时控制。

Utilize STM32 SysTick timer, which triggers an interrupt every 1ms by default:
- Accumulate count in the interrupt service routine; when count reaches 500 (500ms), toggle the LED pin state.
- Use a static variable to maintain the count, achieving non-blocking timing control.
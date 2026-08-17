# 练习 9：外部中断应用与回调函数实现非阻塞式按键控制LED | Practice 9: External Interrupt and Callback Function for Non-blocking Button Control LED

## 功能 | Function
- 使用外部中断（EXTI）检测按键按下事件。 | Use External Interrupt (EXTI) to detect button press events.
- 在中断回调函数中设置标志位，主循环中处理按键逻辑。 | Set flag in interrupt callback function, process button logic in main loop.
- 实现非阻塞式按键消抖和LED控制。 | Implement non-blocking button debouncing and LED control.

## 硬件连接 | Hardware Connection
- Key_EXTI0 连接在 PA0 引脚。 | Key_EXTI0 connected to pin PA0.
- LED 连接在 PA1 引脚。 | LED connected to pin PA1.

## 功能说明 | Description
### 工作原理 | Working Principle
1. **中断触发**：按键按下时，PA0 引脚产生下降沿，触发 EXTI0 中断。
   - **Interrupt Trigger**: When button is pressed, PA0 pin generates falling edge, triggering EXTI0 interrupt.

2. **中断回调**：在 `HAL_GPIO_EXTI_Callback()` 中设置标志位 `key_pressed_flag = 1`。
   - **Interrupt Callback**: Set flag `key_pressed_flag = 1` in `HAL_GPIO_EXTI_Callback()`.

3. **主循环处理**：在 `while(1)` 中检测标志位，进行消抖和LED翻转。
   - **Main Loop Processing**: Detect flag in `while(1)`, perform debouncing and LED toggle.

### 优点 | Advantages
- **非阻塞**：主循环不会被按键检测阻塞，可以同时处理其他任务。
  - **Non-blocking**: Main loop is not blocked by button detection, can handle other tasks simultaneously.
  
- **响应快速**：中断立即响应按键，无需轮询。
  - **Fast Response**: Interrupt responds to button press immediately, no polling needed.

- **效率高**：CPU 只在按键按下时才处理，节省资源。
  - **High Efficiency**: CPU only processes when button is pressed, saving resources.

## 应用场景 | Applications
- 实时控制系统 | Real-time control system
- 多任务处理界面 | Multi-tasking interface  
- 低功耗设备按键 | Low-power device buttons
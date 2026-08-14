# 练习 5：光敏传感器触发LED | Practice 5: Light Sensor Trigger LED

## 功能 | Function
- 通过检测光敏传感器的DO输出来控制LED。 | Control LED by detecting DO output from light sensor.
- 光强度足够时点亮LED，光线不足时熄灭LED。 | Turn on LED when light intensity is sufficient, turn off when insufficient.

## 硬件连接 | Hardware Connection
- DO 连接在 PA2 引脚。 | DO connected to pin PA2.
- LED 连接在 PA1 引脚。 | LED connected to pin PA1.

## 功能说明 | Description
光敏传感器实时检测环境光强度：
- 当光强度足够时（DO输出低电平GPIO_PIN_RESET），点亮LED
- 当光强度不足时（DO输出高电平GPIO_PIN_SET），熄灭LED

Light sensor detects ambient light intensity in real-time:
- When light intensity is sufficient (DO outputs low level GPIO_PIN_RESET), turn on LED
- When light intensity is insufficient (DO outputs high level GPIO_PIN_SET), turn off LED
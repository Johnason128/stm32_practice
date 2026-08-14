# 练习 6：反射传感器触发LED | Practice 6: Reflective Sensor Trigger LED

## 功能 | Function
- 通过检测红外反射传感器的输出来控制LED。 | Control LED by detecting output from infrared reflective sensor.
- 检测到白色区域时点亮LED，检测到黑色区域时熄灭LED。 | Turn on LED when detecting white area, turn off when detecting black area.

## 硬件连接 | Hardware Connection
- Ir_DO 连接在 PA2 引脚。 | Ir_DO connected to pin PA2.
- LED 连接在 PA1 引脚。 | LED connected to pin PA1.

## 功能说明 | Description
红外反射传感器实时检测物体表面颜色/反射率：
- 当检测到白色区域（高反射率，输出低电平 GPIO_PIN_RESET），点亮LED
- 当检测到黑色区域（低反射率，输出高电平 GPIO_PIN_SET），熄灭LED

Infrared reflective sensor detects object surface color/reflectivity in real-time:
- When detecting white area (high reflectivity, outputs low level GPIO_PIN_RESET), turn on LED
- When detecting black area (low reflectivity, outputs high level GPIO_PIN_SET), turn off LED

## 应用场景 | Applications
- 循迹小车（检测黑线）
- 物体颜色识别
- 计数传感器

Line following robot (detect black line)
Object color recognition
Counting sensor
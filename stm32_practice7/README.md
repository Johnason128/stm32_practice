# 练习 7：热敏传感器触发蜂鸣器警报 | Practice 7: Thermal Sensor Trigger Buzzer Alarm

## 功能 | Function
- 通过检测热敏传感器的输出来控制蜂鸣器。 | Control buzzer by detecting output from thermal sensor.
- 温度高于阈值时蜂鸣器闪烁报警，温度低于阈值时蜂鸣器静默。 | Buzzer flashes alarm when temperature is above threshold, remains silent when below threshold.

## 硬件连接 | Hardware Connection
- Hot_DO 连接在 PA2 引脚。 | Hot_DO connected to pin PA2.
- Beep 连接在 PA1 引脚。 | Beep connected to pin PA1.

## 功能说明 | Description
热敏传感器实时检测环境温度：
- 当温度高于阈值（输出低电平 GPIO_PIN_RESET），蜂鸣器以100ms间隔闪烁报警
- 当温度低于阈值（输出高电平 GPIO_PIN_SET），蜂鸣器静默

Thermal sensor detects ambient temperature in real-time:
- When temperature is above threshold (outputs low level GPIO_PIN_RESET), buzzer flashes alarm at 100ms intervals
- When temperature is below threshold (outputs high level GPIO_PIN_SET), buzzer remains silent

## 应用场景 | Applications
- 温度监控系统
- 过热警报器
- 智能温控器

Temperature monitoring system
Overheat alarm device
Smart thermostat
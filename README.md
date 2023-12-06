# 直线电机辨识Matlab脚本使用说明

## 写在前面

- 本脚本仍存在不足，请仔细阅读使用说明。
- 本脚本采取Excel制作并读取实验数据，也可采用实验中自动保存得到的txt数据。
- 仅用于交流学习，不代表正确结果。

## 实验数据说明

- 实验过程中会自动保存数据为txt文件(第一列为输入值，第二列为位置信息)
- 3号电机数据文件夹中的 "输入" 代表cSPACE中的输入值
- 实际输入信号仍为 "终值1V 阶跃时间1s的阶跃信号"
- 每一组数据都可使用，其中"输入25"包含多组数据，旨在多次实验求均值。

## 使用步骤
## 1. 制作实验数据
- 打开需要绘制的txt数据文件，并从第二列开始发生改变的数据开始复制。
- 打开data_Motor.xlsx数据存放表。
- 将所复制的数据粘贴至数据存放的第一列。注意：从第二列值1000处所在行粘贴。
- 补全第一列其余数据：0或者数据的最大值。
### (简易方法 数据来源：3号电机 输入25)
- 移动data_Motor.xlsx中底部标签至第一个。
- 脚本默认读取第一个标签数据。

## 2. 绘制实际响应曲线
- 打开MotorModeling.mlx实时脚本(Matlab R2023a)。
- 运行脚本 即可获得实际响应曲线。
- 其中峰值和0.632处已在图中标出。
- 此时程序进入断点暂停。

## 3. 计算模型参数
- 根据一阶系统建模方法计算增益K和时间常数τ
- 代入MotorModeling.mlx中的"设置用于模型验证的增益及时间常数"
- 修改 K & t ，再次点击运行即可得到模型参数验证曲线。

## BUG反馈
- 待完善
- ……
- ……

## 更新记录
- //2023.12.06// 更新data_Motor.xlsx数据，提供更为简易的使用方法，如需更改数据来源，仍需按原步骤。

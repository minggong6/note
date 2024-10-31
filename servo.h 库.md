#  servo.h 库



1. **头文件**

   在Arduino程序中，首先需要包含servo.h头文件，以便使用Servo库中的函数。使用`#include <Servo.h>`语句即可。

2. **创建Servo对象**
   创建一个Servo对象。这个对象将用于控制特定的舵机。例如，`Servo myservo；`

3. **attach()函数**

   `attach(int pin)`

   此外，`attach(int pin, int min, int max)`函数允许您指定PWM信号的最小和最大脉冲宽度（以微秒为单位）

4. **write()函数**

   `write(int angle)`函数用于设置舵机的目标角度。该函数的参数是角度值（0到180度之间）。例如，`myservo.write(90);`语句将舵机设置到90度的位置。

5. **writeMicroseconds()函数**

   `writeMicroseconds(int microseconds)`函数允许您直接设置PWM信号的脉冲宽度（以微秒为单位）。这对于需要更精确控制舵机位置或速度的场景非常有用`attach(int pin, int min, int max)`函数设置了最小和最大脉冲宽度。

6. **read()函数** 
   读出舵机的角度

7. *attached()函数**

   `attached()`函数用于检测Servo对象是否已成功连接到Arduino板上的对应引脚上。如果连接成功，则返回true；否则返回false。

8. **detach()函数**

   `detach()`函数用于将Servo对象从对应的引脚上分离。如果不再需要控制某个舵机，可以使用这个函数来释放与该舵机关联的资源。
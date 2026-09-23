# ESP32_9_Level_Inverter
ESP32 project file which i wrote for my final year 9 level inverter project
This inverter logic runs at 50kHz where the cpu utilization is only about 20% from my testing..so there is still some cpu power left (Around 80%) for to run advanced PID loops with some additional sensor input for closed feedback system. Currently it is in Open Loop,  but the modulation index can be dynamically adjusted so it can be made into a closed loop system . I tried my maximum to optimize the code to work at this speed with much lesser CPU utilization so that later this code can be modified to make it closed loop without the reduction in current performance. Also i tried to avoid the use of floating point math to provide its full speed for example the LUT values for the sine reference wave and triangular modulating wave which are precalculated values (which may seen as big integer values due to the integer scaling i used to convert the floating point values to its corresponding integer values) so CPU doesn't want to waste its CPU cycles to calculate it repeatedly .

Its total RAM and flash usage is given below:
RAM:   [=         ]   9.1% (used 29892 bytes from 327680 bytes)
Flash: [==        ]  21.4% (used 279929 bytes from 1310720 bytes)

So in terms of speed and space, i tried my maximum to optimize it.

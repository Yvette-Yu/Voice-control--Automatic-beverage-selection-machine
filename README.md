# Voice-control--Automatic-beverage-selection-machine
## 屏幕
``` c
#include "LCD12864RSPI.h"
#define AR_SIZE( a ) sizeof( a ) / sizeof( a[0] )
 
unsigned char show0[]= { 0xA3, 0xE3,
  0xA3, 0xE8,
  0xA3, 0xF2,
  0xA3, 0xEF,
  0xA3, 0xED,
  0xA3, 0xE5};  
unsigned char show1[]="chrom ";

 
void setup()
{
LCDA.Initialise(); // 屏幕初始化
delay(100);
LCDA.CLEAR();//清屏
}
 
void loop()
{
LCDA.DisplayString(0,0,show0,AR_SIZE(show0));//第一行第三格开始
delay(100);
LCDA.DisplayString(2,0,show1,AR_SIZE(show1));;//第三行第二格开始
delay(500);

}
```

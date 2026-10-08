


> ITek相机倍频设计

- 海康相机`SetTriggerMode_Line`模式

```cpp
  //  全部Line0，1，3都设置为差分
  nRet  =  MV_CC_SetEnumValue(handle,  "LineSelector",  0);
  nRet  =  MV_CC_SetEnumValue(handle,  "LineFormat",  2);  //  Differential  Enum  Entry  Value:  2
  
  nRet  =  MV_CC_SetEnumValue(handle,  "LineSelector",  1);
  nRet  =  MV_CC_SetEnumValue(handle,  "LineFormat",  2);  //  Differential  Enum  Entry  Value:  2

  nRet  =  MV_CC_SetEnumValue(handle,  "LineSelector",  3);
  nRet  =  MV_CC_SetEnumValue(handle,  "LineFormat",  2);  //  Differential  Enum  Entry  Value:  2
```
```cpp
//  帧信号参数配置，不启动
  nRet  =  MV_CC_SetEnumValue(handle,  "TriggerSelector",  6);  //  FrameBurstStart  Enum  Entry  Value:  6
  if  (frameTrigger  !=  100)
  {
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbOTMxNzM5MTE5LC0yMDgzOTMxNzgyLDgzOT
I5MDA1XX0=
-->
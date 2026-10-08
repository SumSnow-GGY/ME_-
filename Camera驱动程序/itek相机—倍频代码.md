


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
	  nRet  =  MV_CC_SetEnumValue(handle,  "TriggerSource",  uint(frameTrigger));  //  HIK相机，一共只有3组差分输入
      nRet  =  MV_CC_SetEnumValue(handle,  "TriggerActivation",  1);  //  FallingEdge  Enum  Entry  Value:  1
  }
```

```cpp
//  行信号参数配置，不启动
  nRet  =  MV_CC_SetEnumValue(handle,  "TriggerSelector",  9);  //  LineStart  Enum  Entry  Value:  9
  if  (lineTrigger  !=  100)
  {
      nRet  =  MV_CC_SetEnumValue(handle,  "TriggerActivation",  1);  //  FallingEdge  Enum  Entry  Value:  1
  }
```

```cpp
  //  行触发缓存使能
  nRet  =  MV_CC_SetBoolValue(handle,  "LineTriggerCacheEnable",  true);  //  打开行缓存使能
if  (lineTrigger  <  10)
{
	// 设置TriggerSource
}
else  if  (lineTrigger  >=  10  &&  lineTrigger  <=  99)
{
	//设置TriggerSource"
  //设置EncoderSourceA
  //设置EncoderSourceB
  //设置InputSource", 

    // 根据LineTrigger
	// 设置PreDivider
	// 设置Multiplier
	// 设置PostDivider
}
else  if  (lineTrigger  ==  100) //  全部不设置
```

### 海康相机参数-触发
//  全部Line0，1，3都设置为差分
线路选择器 线路0，1，3
I/O类型（单端/差分） 差分

//  帧信号参数配置，不启动 //  行信号参数配置，不启动
触发器选择器 6 帧触发
触发源
触发极性 下降沿

//  行触发缓存使能
```cpp
if  (lineTrigger  <  10)
{
	// 设置TriggerSource
}
else  if  (lineTrigger  >=  10  &&  lineTrigger  <=  99)
{
	//设置TriggerSource" 分频器
  //设置EncoderSourceA 编码器源A 线路0
  //设置EncoderSourceB 编码器源B 线路1
  //设置InputSource", 变频器控制，输入源 编码器模块输出

    // 根据LineTrigger
	// 设置PreDivider 预分频器
	// 设置Multiplier 乘法器
	// 设置PostDivider 后分频器
}
else  if  (lineTrigger  ==  100) //  全部不设置
```

内部
触发器选择器  帧触发开始

外部触发
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTIwODg1MTg2NTMsMTUzNDY4NDc2OSwtMT
c0NjU5OTUyOCwyODYxODgyMzAsLTIwODM5MzE3ODIsODM5Mjkw
MDVdfQ==
-->
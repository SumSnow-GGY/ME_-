


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

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTIwODM5MzE3ODIsODM5MjkwMDVdfQ==
-->
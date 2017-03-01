﻿# Scaling
_namespace: [Microsoft.VisualBasic.Data.ChartPlots](./index.md)_

将数据坐标转换为绘图坐标



### Methods

#### #ctor
```csharp
Microsoft.VisualBasic.Data.ChartPlots.Scaling.#ctor(System.Collections.Generic.IEnumerable{System.Double},System.Boolean)
```


|Parameter Name|Remarks|
|--------------|-------|
|data|-|
|horizontal|
 所进行绘制的条形图是否是水平的？
 |


#### __scaling
```csharp
Microsoft.VisualBasic.Data.ChartPlots.Scaling.__scaling(System.Single[],System.Single@,System.Boolean)
```
返回``max-min``

|Parameter Name|Remarks|
|--------------|-------|
|array!|-|
|min!|-|
|absoluteScaling|-|


#### ForEach
```csharp
Microsoft.VisualBasic.Data.ChartPlots.Scaling.ForEach(System.Drawing.Size,System.Drawing.Size)
```
返回的系列是已经被转换过的，直接使用来进行画图

#### ForEach_histSample
```csharp
Microsoft.VisualBasic.Data.ChartPlots.Scaling.ForEach_histSample(System.Drawing.Size,System.Drawing.Size)
```
返回的系列是已经被转换过的，直接使用来进行画图

#### Scaling
```csharp
Microsoft.VisualBasic.Data.ChartPlots.Scaling.Scaling(Microsoft.VisualBasic.Data.ChartPlots.Histogram.HistogramGroup,System.Func{Microsoft.VisualBasic.Data.ChartPlots.Histogram.HistogramData,System.Single[]},System.Single@,System.Boolean)
```
返回dx或者dy

#### YScaler
```csharp
Microsoft.VisualBasic.Data.ChartPlots.Scaling.YScaler(System.Drawing.Size,System.Drawing.Size,System.Double)
```


|Parameter Name|Remarks|
|--------------|-------|
|size|-|
|margin|-|
|avg|当这个参数值是一个有效的数字的时候，返回的Y将会以这个平均值为零点|



### Properties

#### dx
x,y轴分别的最大值和最小值的差值
#### dy
x,y轴分别的最大值和最小值的差值

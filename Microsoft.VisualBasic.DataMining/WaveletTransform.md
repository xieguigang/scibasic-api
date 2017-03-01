﻿# WaveletTransform
_namespace: [Microsoft.VisualBasic.DataMining](./index.md)_

小波变换工具

> 
>  
>  The first DWT was invented by the Hungarian mathematician Alfréd Haar. For an input represented by a 
>  list of 2n numbers, the Haar wavelet transform may be considered to simply pair up input values, 
>  storing the difference and passing the sum. This process is repeated recursively, pairing up the sums 
>  to provide the next scale: finally resulting in 2n-1 differences and one final sum.
>  
>  Suppose you are given N values
>  
>  x = (x1, x2, … xN)
>  
>  where N is even.(X向量的元素的个数必须是偶数)
>  
>  We take pair-wise average of numbers
>  
>  sk = (x2k + x2k+1)/2 for k=0, …, N/2 -1
>  
>  For example,
>  
>  x = (6, 12, 15, 15, 14, 12, 120, 116) -> s = (9, 15, 13, 118)
>  
>  We need second list of data d so that the original list x can be recovered from s and d.
>  
>  For dk (called directed distances), we have:
>  
>  dk = (x2k - x2k+1)/2 for k=0, …, N/2 -1
>  
>  The process is invertible since:
>  
>  sk + dk = (x2k + x2k+1)/2 + (x2k - x2k+1)/2 = x2k
>  
>  sk - dk = (x2k + x2k+1)/2 - (x2k - x2k+1)/2 = x2k+1
>  
>  
>  So we map x = (x1, x2, … , xN) to (s | d) = (s1, … , sN/2 | d1, … , dN/2).
>  
>  Using our example values, we have:
>  
>  (6, 12, 15, 15, 14, 12, 120, 116) -> (9, 15, 13, 118 | -3, 0, 1, 2)
>  
>  This process is repeated recursively for s:
>  
>  (9, 15, 13, 118 | -3, 0, 1, 2) -> (12, 65.5 | -3, -52.5 | -3, 0, 1, 2)
>  
>  (12, 65.5 | -3, -52.5 | -3, 0, 1, 2) -> (38.75 | -26.75 | -3, -52.5 | -3, 0, 1, 2)
>  
>  So final result is:
>  
>  (38.75, -26.75, -3, -52.5, -3, 0, 1, 2)
>  
>  Why might people prefer the data in this form?
>  
>  We can identify large changes in the differences portion d of the transform.
>  It is easier to quantize the data in this form.
>  The transform concentrates the information (energy) in the signal in fewer values.
>  And the obvious answer: fewer digits!!
>  In case of images, we need 2D FWT. First, we perform 1D FWT for all rows, and next, for all columns. 
>  For color Images, we deal with RGB components of color, and perform Haar Transform for each component 
>  separately. Any component (R G B) has values from 0 to 255 to before transformation we scale this 
>  values. For displaying image after transformation, we scale back transformed values.
>  
>  


### Methods

#### FWT
```csharp
]@,System.Int32)
```
Discrete Haar Wavelet 2D Transform

|Parameter Name|Remarks|
|--------------|-------|
|iterations|Iteration must be Integer from 1 to|


#### IWT
```csharp
]@,System.Int32)
```
Inverse Haar Wavelet 2D Transform

|Parameter Name|Remarks|
|--------------|-------|
|iterations|Iteration must be Integer from 1 to|




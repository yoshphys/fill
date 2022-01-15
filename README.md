# fill
 A program to make a histogram from data in a text file


## Overview

 `fill` is a script to make a histogram from data in a text file.
 [ROOT](https://root.cern.ch) is used to show histograms.


## Requirement
 - python (> 3.9.9)
 - [ROOT](https://root.cern.ch) (> 6.24/06)


## Usage
 To make a histogram from following file (`data1.txt`),

 > ` 0.905957`  
 > ` 0.471139`  
 > `-0.607482`  
 > ` 1.003078`  
 > `-0.583407`  
 > `-0.994423`  
 > `-0.698762`  
 > `-0.289269`  
 > ` 2.345332`  
 > ` 2.110272`  

 you may just run the following command.

 ```
 $ fill data1.txt
 ```

 Suppose that you have following file (`data2.txt`).

 > `-0.393638    0.0549356`  
 > ` 0.8376      0.941336`  
 > ` 0.35987    -0.732858`  
 > `-1.09077    -1.25002`  
 > `-0.0680796   0.409349`  
 > `-1.17037    -0.341653`  
 > `-0.322438    0.192855`  
 > `-2.23153    -1.2349`  
 > `-0.323323    0.886307`  
 > ` 1.18789     1.80288`  

 If you run the command `fill data2.txt`, 1D-histogram with all elements in `data2.txt` will be shown.

 In the case you want to make 2D-histogram to see the correlation between the data in the column-1 and those of column-2, you may run the following command,

 ```
 $ fill data2.txt --xcol 1 --ycol 2
 ```

 You can also specify the number of bins for each axis, the range of each axis, delimiter used in data file, and comment delimiter used in data file.
 

<!--
## Features

## Reference
-->

## Author
 [yoshphys](https://github.com/yoshphys)

## Licence
 fill is under MIT license. See the [LICENSE](https://github.com/yoshphys/dot2pdf/blob/main/LICENSE) for more info.

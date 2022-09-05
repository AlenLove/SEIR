## SEIR: Selector-Embedded Iterative Regression
   A fast and extremely powerful R package for GWAS
  
   Written by Mengjin Zhu & GuangLiang Zhou
  
   Last update: Sep 5, 2022
## Installation
   install.packages("devtools")

   devtools::install_github("AlenLove/SEIR")
   ```R
   packageurl <- "https://raw.githubusercontent.com/AlenLove/SEIR/master/1.1.0/SEIR_1.1.0.zip"
   
   install.packages(packageurl,repos=NULL)
   ```

## Demo Data
   SEIR R version only support numeric data type
## Usage
   library(SEIR)

#### # genotype information data
    data(map)
#### # genotype data
    data(geno)
#### # phenotype data
    data(phe)
    We suggest to provide the phenotype file

| Taxa | trait1 | trait2 | trait3 |
| :---: | :---: |:---: |:---: |
|33-16|101.5|0.25|0|
|38-11|	102.7|0.23|1|
|4226	|101.2|-0.17|1|
|4722|	105.5|NA|0|
|A188	|108.1|0.57|1|
|A214N|	95.13|0.87|0|
|A239	|100.2|-0.16|1|

#### # association analysis
SEIR(Y=phe,X=geno,GM=map,CV=NULL,maxStep=10,
    selector="stepwise",fun.selection="fastLm",
    extraction="min",X.check="FALSE",chunk.num = NULL,
    file.output=TRUE,plot.style="CMplot",cutOff=0.05)
#### # more features   
More parameters explained [here]
### Issues
Bugs could be reported [here]
## The license notice
This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details
## Author
Mengjin Zhu & GuangLiang Zhou (glzhou@webmail.hzau.edu.cn)

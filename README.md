## SEIR: Selector-Embedded Iterative Regression
   A fast and extremely powerful R package for GWAS
  
   Written by Mengjin Zhu & GuangLiang Zhou
  
   Last update: Sep 27, 2021
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
#### # association analysis
SEIR(Y=phe,X=geno,GM=map,CV=NULL,maxStep=10,
    selector="stepwise",fun.selection="fastLm",
    extraction="min",X.check="FALSE",chunk.num = NULL,
    file.output=FALSE,plot.style="SEIR",cutOff=0.05)
#### # more features   
More parameters explained [here]
### Issues
Bugs could be reported [here]
## The license notice
This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details
## Author
Mengjin zhu (glzhou@webmail.hzau.edu.cn)

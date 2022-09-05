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
The map file is listed as follows:
    
<table>
<tbody>
<tr>
<td align="center">SNP</td>
<td align="center">Chr</td>
<td align="center">Pos</td>
</tr>
<tr>
<td align="center">rs3683945</td>
<td align="center">1</td>
<td align="center">3197400</td>
</tr>
<tr>
<td align="center">rs3707673</td>
<td align="center">1</td>
<td align="center">3407393</td>
</tr>
<tr>
<td align="center">rs6269442</td>
<td align="center">1</td>
<td align="center">3492195</td>
</tr>
<tr>
<td align="center">rs6336442</td>
<td align="center">1</td>
<td align="center">3580634</td>
</tr>
<tr>
<td align="center">rs13475699</td>
<td align="center">1</td>
<td align="center">3860406</td>
</tr></tbody></table>

#### # genotype data
    data(geno)
The genotype file is listed as follows:

<table>
<tbody>
<tr>
<td align="center">1</td>
<td align="center">1</td>
<td align="center">2</td>
<td align="center">1</td>
<td align="center">2</td>
<td align="center">…</td>
<td align="center">0</td>
</tr>
<tr>
<td align="center">1</td>
<td align="center">1</td>
<td align="center">0</td>
<td align="center">1</td>
<td align="center">0</td>
<td align="center">…</td>
<td align="center">2</td>
</tr>
<tr>
<td align="center">1</td>
<td align="center">2</td>
<td align="center">2</td>
<td align="center">1</td>
<td align="center">2</td>
<td align="center">…</td>
<td align="center">0</td>
</tr>
<tr>
<td align="center">1</td>
<td align="center">1</td>
<td align="center">2</td>
<td align="center">1</td>
<td align="center">2</td>
<td align="center">…</td>
<td align="center">0</td>
</tr>
<tr>
<td align="center">0</td>
<td align="center">0</td>
<td align="center">0</td>
<td align="center">0</td>
<td align="center">0</td>
<td align="center">…</td>
<td align="center">0</td>
</tr></tbody></table>

#### # phenotype data
    data(phe)
The phenotype file is listed as follows:

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
**phe**, phenotype data  
**geno**, genotype data  
**map**, map data 
#### # more features   
More parameters explained [here]
### Issues
Bugs could be reported [here]
## The license notice
This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details
## Author
Mengjin Zhu & GuangLiang Zhou (glzhou@webmail.hzau.edu.cn)

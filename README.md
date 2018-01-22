## BLINK
This is the R version of BLINK model. You can find the C version here: https://github.com/Menggg/BLINK
## Installation
install.packages("devtools")

devtools::install_github("YaoZhou89/BLINK")

## Demo Data
BLINK R version only support numeric data type.

## Usage
source("http://zzlab.net/GAPIT/gapit_functions.txt")

source("http://zzlab.net/FarmCPU/FarmCPU_functions.txt")

library(BLINK)

### #read genotype, genotype information, phenotypes
myGM=read.table("myData.map",head=T) # genotype information data

myGD=read.big.matrix("myData.dat",head=F,sep="\t",type="char") # genotype data

myY = read.table("myData.txt",head = T) # phenotype data

### # Association analysis
myBlink=Blink(Y=myY,GD=myGD,GM=myGM,maxLoop=10,time.cal=T) # more parameters explained in man/user manual

## Author
Dr.Yao Zhou (yao.zhou@genetics.ac.cn)

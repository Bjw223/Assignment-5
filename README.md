# Assignment-5
if (!require("data.table")) install.packages("data.table")
library("data.table")
 header <- read.table("UNRATE.csv", header = TRUE,
                       sep=",", nrow = 1)
  DF <- fread("UNRATE.csv", skip=1, sep=",",
              header=FALSE, data.table=FALSE,
              showProgress=FALSE)
  setnames(DF, colnames(header))
  rm(header)
  
  
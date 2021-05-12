# Files-for-CrossICC
Files for construction and prediction CrossICC

#####1.we use 1_for_crossicc.txt  2_for_crossicc.txt for construction######
library(CrossICC)
exp.files <- list.files(path = ".", pattern = "txt")
CrossICC.input <- CrossICCInput(exp.files)
CrossICC.object <- CrossICC(CrossICC.input, use.shiny = T, overwrite = TRUE, output.dir = '.')

#####2.then in the shiny,we first upload the default rds in the shiny( in shiny app but not in R)
#####3.then we upload the matrix for_prediction.txt in "Allocate new samples" modulem, submit
#####4. in our app, the bug "invalid subscript type 'list'" appeared.

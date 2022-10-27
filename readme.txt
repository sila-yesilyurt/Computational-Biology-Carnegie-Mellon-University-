Copy the Metagenomics folder into your "go/src" directory.

Then, write each of the missing functions in the Functions folder. If you need a subroutine, please feel free to place it in the same file.

To test a function, you should "cd" into the Functions directory and run

go test -run ^TestFunctionName$

where TestFunctionName is based on the specific function you are testing.

For example, after writing each appropriate function, you should call each of the following tests.

go test -run ^TestRichness$
go test -run ^TestEvenness$
go test -run ^TestBrayCurtisDistance$
go test -run ^TestJaccardDistance$
go test -run ^TestRichnessMatrix$
go test -run ^TestMultipleEvenness$
go test -run ^TestMultipleBetaDiversity$

Note: we are providing a function to produce a frequency map in frequency_map.go, since this was covered in the test materials.

To check that you have passed *all* tests, call "go test".

After you have passed all of these tests, navigate into the parent Metagenomics directory (using "cd .."). We will fill in main.go, after which you can call "go build" and then execute the resulting executable file.

The "Data" folder contains samples for our Three Rivers Metagenomics project. Our code will use the functions that you write and then write matrices to the "Matrices" folder.

To run our Metagenomics pipeline visualizing our data, we will need to use R. First, install R (https://www.r-project.org), as well as RStudio to make working with R a bit easier (http://rstudio.com).

Then, install the following packages by opening R, copying these over, and hitting enter:

install.packages("ggcorrplot")
install.packages("reshape")
install.packages("stringr")
install.packages("ggplot2")
install.packages("ape")

The "Metagenomics_Pipeline.R" file can then be opened in R. You will need to change your working directory in the appropriate line in the R file, and make sure that you have the packages installed that it imports. You can then run this file, and it will generate plots based on your data in the "Matrices" folder that will be placed into the "Plots" directory. We will then visualize and interpret these plots!
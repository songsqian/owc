This document introduces the use of the jupyter notebook on Google Colab to run the example.  

The example notebook is written in R but run through python (the R magic) to enable the connection of personal Google Drive on Google Colab. A jupyter notebook consists of text and code cells. We document the process in text cells and execute the code in code cells.  

## Mounting Google Drive
To run the example on your computer, you need to have a Google Drive account.  Once you saved the file `ExampleCWC.ipynb` into your Drive (e.g., in a folder called `CWC_Example`), you can download the content of this example into the folder. You should have a subfolder `Data` (with three `.csv` files) and a file named `owcTPma05SeasonSTDZ.RData`.

The first code cell includes three lines. The first line calls python's R extension and the next two lines mounts a local Google Drive.  To run the cell, we cal either hit `ctrl+enter` or click on the arrow on the top-left corner of the cell.  The program will ask for permission to access the intended Google Drive account.  Simply follow the link and log on to the Google Drive account to generate the code. Copy the code and paste it in the box and hit `enter`.  The Google Drive folder will appear in `/content/drive/My Drive/`. To access the content of this example, you need to edit the second line in the next code cell, `base <- "/content/drive/My Drive/..."`, replacing `...` with your folder path name. Now you are set to run this code cell.  This cell installs necessary packages, set up the `rstan` parameters, and load a few functions.  This cell will take a few minutes to complete.  Once it is done, we are ready for the analysis.

The next two code cells import data for the example.  The model fitting process is divided into six steps, each with its own code cell. The first four steps set up the Bayesian model, which will run relatively fast.  

Running the Bayesian model starts in the code cell starts (on line 2) with the line `fit <- stan_model(...)` (step 5).  This cell takes a few minutes to complete.  The results are processed in step 6 in the following code cell.

The last code cell runs the updated model using new data.


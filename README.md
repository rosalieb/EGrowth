# EGrowth
A global database of earthworm body growth curves

If you want to run the App from R, type the folowing code in the R Console:
``` 
 library(shiny)
 runGitHub( "EGrowth", "JeromeMathieuEcology") 
```
The app should appear in your web browser.

If you want to download the database from R, type the folowing code in the R Console:

library(RCurl)
``` 
url_curves	<- getURL("https://raw.githubusercontent.com/JeromeMathieuEcology/EGrowth/master/curves.txt")
url_mds <- getURL("https://raw.githubusercontent.com/JeromeMathieuEcology/EGrowth/master/curves_md.csv")
url_refs <- getURL("https://raw.githubusercontent.com/JeromeMathieuEcology/EGrowth/master/references.csv")


growth <- read.csv2(text = url_curves, h = T, na.strings = "na",sep = "\t")
EGrowth_metadata  <- read.csv2(text=url_mds, h = T,na.strings = "na", sep = "\t", dec = ".")
EGrowth_references <- read.csv2(text=url_refs, h = T,na.strings = "na", sep = "\t", dec = ".")
``` 
Then check the User Guide to use the database.

Enjoy!
Jerome

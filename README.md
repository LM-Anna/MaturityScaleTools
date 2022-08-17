# MaturityScaleTools
  This tool is a **guide for identifying maturity phases of fish of commercial interest**. It was set up as part of the project to harmonize maturity data collection methods.

  It is composed of identification sheets for males and females of each species of fish and provides simple comments and photos to ease the identification of maturity phases.

  The maturity phases identification presented in this tools is exclusively based on visual criteria described by the **ICES 2012/2018 "WKMATCH" scale**. This scale was created in the ideal of a universal scale, regardless of the species or the sex of the individual. It also falls within the respect of the species biology.
  
  This scale is divided into 6 maturity phases, corresponding to specific development periods of the gonads during the reproductive cycle. 

---

To generate new identification guides or update them, all files and scripts used are provided by the GitHub repository “MaturityScaleTools”. When being downloaded and used, the directories must remain the same in order to operate. The process described here is the process that should be used if wanted to generate new identification guides or to update them.

First of all, before launching the scripts, the photo_guides.xlsx data frame was checked out : there must be at least a row created with the NA photo for each species/group of species, each sex and each maturity phase and a fish picture must be added for each species/group of species that will have their identification guides. The “dataLOOPS.xlsx” must also have new rows for new parameters with any new species. Then, all photos links should be adapted depending on specific directories where the gonads’ photography database and the GitHub repository are being used. The scripts to generate identification guides were “LoopPDF.Rmd” and “LoopHTML.Rmd” scripts. They automatically generated identification guides on loops, depending on the parameters of the “dataLOOP.xlsx” data frame. The output files were set up to automatically generate in the “docs” GitHub’s directory so they would automatically be added to the GitHub pages. Likewise, the “LoopPhotoToTake.Rmd” script will automatically generate on the GitHub pages updated files with missing photos that must be taken to complete the identification guides.  It is really important to note that those “loop” scripts must not be knitr, only the chunks content must be launched. Moreover, before reading the loops, if it a loop that generates .pdf format files, the attached .Rmd file (ScaleFR.Rmd, ScaleENG.Rmd, PhotosManquantes.Rmd) must be have the pdf format output on top everything in the “YALM” section.

Finally, in order to be able to have access to identification guides for new species, a new section/link must be added to a list of script that produces GitHub pages : ENGHTML_AMM.Rmd, ENGHTML_MG.Rmd, ENGPDF_AMM.Rmd, ENGPDF_MG.Rmd, FRHTML_AMM.Rmd, FRHTML_MG.Rmd, FRPDF_AMM.Rmd, FRPDF_MG.Rmd. The new section to add is described at the beginning of the script. Then, those scripts must be “knitr” to produce html pages directly into the GitHub pages directory.

If new photos or new species were added, this all process would update the identification guides on the GitHub pages.


---

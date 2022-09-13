# MaturityScaleTools  

<div style="text-align: justify">

  This GitHub repository hosts all tools to automatically generate **guide for identifying maturity phases of fish of commercial interest** (https://lm-anna.github.io/MaturityScaleTools/). 
  
  Its creation falls within the harmonisation of maturity data acqusition methods for bony fish of commercial interest project carried out by **IFREMER SIH (Système d'Information Halieutique)**.
This project aims to harmonise and standardise the maturity staging process during scientific surveys, using the ICES maturity scale (2018) and Brown-Peterson et al. (2011) terminologies.

  The maturity identification guide is composed of identification forms for males and females of each species of fish and provides simple comments and photos to ease the identification of maturity phases. Photos used to elaborate identification forms come from the dataset **"A gonad photographs dataset for fish of commercial interest from the European and Caribbean coastal waters"** available on ZENODO.

  The maturity phases identification presented in this tools is exclusively based on visual criteria described by the **ICES 2018 "WKASMSF" scale**. This scale was created in the ideal of a universal scale, regardless of the species or the sex of the individual. It also falls within the respect of the species biology.
  This scale is divided into **6 maturity phases**, corresponding to specific development periods of the gonads during the reproductive cycle. 
  
  To have more details about the creation of these identification forms, please contact Anna Le Meleder (annalemeleder@orange.fr).  
  
---

### Data Records
#### *"data"*

The "data" file gathers 40 pictures/logos used to embellish the identification forms and 4 data frames :

**Photo_Guides** : archives in zip format of:  
- 6 pictures (.PNG; 1-187 Ko) that are : the NA and NAEng picture when not photo is available for a maturity phase, the female logo, the male logo, the “go back” logo and the GitHub’s main page picture   
- A directory (Image_Fish) containing 35 fish pictures (.PNG; 44-883 Ko) to illustrate  the species/groups of species of the corresponding identification form  

**photo_guides.xlsx** : data table (.xlsx) with two spreadsheets that have the same data but one is in French (FINAL_FR) and the other one in English (FINAL_ENG). Both of these sheets list the same data : photos that may potentially be used in the identification guide and their associated data. This table has the same 13 columns as photo_mat.xlsx, plus two more columns :   
- Guides : code id “yes”, “no” or “na”, with “yes if the picture appears in the identification forms (maximum 2 photos should be selected for a single maturity stage for each species), all other choices should be classified under “no”, and “na” is used for the default NA picture;  
- Phase : maturity phase name on forms  
- Name : Name of the photo;  
- Type : Type of gonad photo (INT = inside without organs, INT ORG = inside with organs, EXT = outside, EXT OUV = outside and open, FLUANT = fluent);  
- sppeng : English vernacular name of the species or species group established for identification forms;  
- Species : Scientific name of the species or species group established for identification guides;  
- Sex : Sex of the fish (M = male, F = female);  
- phase ID : visually estimated maturity phase (ICES WKASMSF scale : A, B, C, D, E or F);  
- Link : Link to the photo =LIEN_HYPERTEXTE(« (Your path to the database)\Photo_MATURITE\« &Hn& »\« &En& »\« &Fn& »\« &An& ».JPG »)  
- spplatTRUE : Scientific name of the species without taking species groups into account;  
- sppengTRUE : English vernacular name of the species without taking species groups into account;  
- Date : Date the photo was added to the dataset;  
- Campaign : Survey during which the photo was taken;  
- Area : Geographical area (ICES or not) where the scientific survey occurred;  
- Commentary : Comments about the photo.


**matu_scale.xlsx** : data table (.xlsx) with two spreadsheets that also have the same data but one is in French (SCALE_FR) and the other one in English (SCALE_ENG). They both list all the commentaries found in the in the identification guide, for each species, each sex and each maturity phase. One row corresponds to a single information. For each row, the associated columns are as followed :  
- Name : Vernacular name of the species or species group established for the identification guide;  
- Phase : maturity phase A, B, C, D, E or F (ICES, 2018);   
- Sex : Sex (F for female, M for male);  
- Text : Comment established for the species/sex/maturity phase;  
- Species : Scientific name of the species or species group established for the identification guide.

**FSM.xlsx** : data table (.xlsx) that lists all of the size range at first maturity for each species and each sex. For each row, the associated columns are as followed :  
- SubSpecies : Scientific name of the species without taking the species groups into account;  
Species : Scientific name of the species or species group established for the identification guide;  
- Sex : Sex (F for female, M for male);  
- FSM : Size range at first maturity

**dataLOOP.xlsx** : data table (.xlsx) listing all the parameters to generate in the identification guide. For each row, the associated columns are as  followed :   
- spplat : Scientific name of the species or species group established for the identification guide;  
- sppeng :  English vernacular name for the species or species group established for the identification guide;  
- sppfr : French vernacular name for the species or species group established for the identification guide;  
- sex : (F for female, M for male).



#### *"docs"*

The "docs" file gathers all the 15 html. pages that leads to all the different identification forms and sort them into the format (pdf or html) and language (English or French) :  
- **index.html**  
- **fr.html**  
- **frAMM.html**  
- **frMG.html**  
- **FRHTML_AMM.html**    
- **FRHTML_MG.html**  
- **FRPDF_AMM.html**  
- **FRPDF_MG.html**  
- **eng.html**  
- **engAMM.html**  
- **engMG.html**  
- **ENGHTML_AMM.html**    
- **ENGHTML_MG.html**  
- **ENGPDF_AMM.html**  
- **ENGPDF_MG.html**  

It also gathers in pdf format the "Fish's gonads photography protocol" in both English and French version **(ENG_P.pdf & FR_P.pdf)**, as well as 8 sheets (pdf and html) with the remaining maturity phases to take in photo in order to complete identification forms :  
- **PhotototakeAMM.html**  
- **PhotototakeAMM.pdf**  
- **PhotototakeGM.html**  
- **PhototakeGM.pdf**  
- **PhotoàPrendreAMM.html**  
- **PhotoàPrendreAMM.pdf**  
- **PhotoàPrendreGM.html**  
- **PhotoàPrnedreGM.pdf**  

Finally, it gathers the **280 identification forms**, so be it 70 identification forms in both html and in pdf format and in both English and French.  



#### *"script"*  

The "script" file gathers all the script that generate the identification forms :  
- **ScaleENG.Rmd** (visual format of an identification form in English)    
- **ScaleFR.Rmd** (visual format of an identification form in French)    
- **LoopHTML.Rmd** (to generate identification forms for every species in html format)  
- **LoopPDF.Rmd** (to generate identification forms for every species in pdf format)  

It also gathers scripts to generate the sheets with the missing fishes :  
- **PhotoManquantes.Rmd**  
- **LoopPhotoToTake.Rmd**  

Finally, it gathers the scripts to generate the 15 html pages for the GitHub page :  
- **index.Rmd**  
- **fr.Rmd**  
- **frAMM.Rmd**  
- **frMG.Rmd**  
- **FRHTML_AMM.Rmd**    
- **FRHTML_MG.Rmd**  
- **FRPDF_AMM.Rmd**  
- **FRPDF_MG.Rmd**  
- **eng.Rmd**  
- **engAMM.Rmd**  
- **engMG.Rmd**  
- **ENGHTML_AMM.Rmd**    
- **ENGHTML_MG.Rmd**  
- **ENGPDF_AMM.Rmd**  
- **ENGPDF_MG.Rmd**  

---

### Usage Notes

To update or generate new identification forms, all files and scripts needed are available in this GitHub repository “MaturityScaleTools”. When downloaded and used, directories must remain in the same order to operate properly.  

First of all, before launching the scripts, the *photo_guides.xlsx* data frame must be completed. Note that for each new species, 12 NA rows must be created with the link to the NA photo (a row for each maturity stage of each sex). It is also important for those rows to put the information “na” in the “Guides” column. Also, this new species picture should be added to the *“Image_Fish”* file. The *“dataLOOPS.xlsx”* must also have 2 new rows added per species, to account for both sexes (M & F). Then, all photo repository links should be adapted depending on the location of the gonads’ photograph database and the GitHub repository.  

The scripts to generate the identification guide are the *“LoopPDF.Rmd”* and *“LoopHTML.Rmd”* scripts. They automatically generate identification guides by using loops, depending on the sets of parameters in the *“dataLOOP.xlsx”* data frame. The output files are set up to automatically generate in the **“docs”** GitHub’s file so they would automatically be added to the GitHub pages. Likewise, the *“LoopPhotoToTake.Rmd”* script will automatically generate on the GitHub pages sheet that indicates missing photos on the identification forms.  It is important to note that those scripts (*“LoopHTML.Rmd”, “LoopPDF.Rmd”, “LoopPhotoToTake.Rmd”*) must not be knitr, only the chunks content must be launched, as noted within the scripts. Moreover, before reading the loops, if it is a loop that generates .pdf format files, the attached .Rmd file (*ScaleFR.Rmd, ScaleENG.Rmd, PhotosManquantes.Rmd*) must be have the pdf format first in the **“YALM”** section (further described in the scripts).  

Finally, in order to access the newly updated identification guide, a new link must be added to the scripts that produce the GitHub pages : *ENGHTML_AMM.Rmd, ENGHTML_MG.Rmd, ENGPDF_AMM.Rmd, ENGPDF_MG.Rmd, FRHTML_AMM.Rmd, FRHTML_MG.Rmd, FRPDF_AMM.Rmd, FRPDF_MG.Rmd.* Further information can be found  at the beginning of the previously stated script. Then, those scripts must be **“knitr”** to produce html pages directly into the GitHub pages directory.

</div>

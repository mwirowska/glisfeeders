# glisfeeders
Data connected with manuscript: Explorative behavior allows the successful finding of ephemeral food resources in the wild

This README file was generated on 2022-12-29 by Martyna Wirowska


# General information


1. Title of Dataset: Explorative behavior allows the successful finding of ephemeral food resources in the wild

2.  Corresponding Authors Information: <p>&nbsp;</p>

   * Name: Martyna Wirowska
   * Institution: University of Warsaw
   * Email: martyna.wirowska@gmail.com <p>&nbsp;</p>
   * Name: Jan S. Boratyński
   * Institution: Mammal Research Institute
   * Email: jan.boratynski@gmail.com
   <p>&nbsp;</p>

3. Date of data collection: 
	2020

4. Geographic location of data collection: 
	Kozienice Forest, Poland

5. Information about funding sources that supported the collection of the data: 
This research was supported by the Forest Research Institute, grant no. 900-128 awarded to Z.B.


# Sharing/Access Information


1. Licenses/restrictions placed on the data: 
	None

2. Links to publications that cite or use the data:  

  These data were used in the following manuscript:  
  * Manuscript number: BEAS-D-22-00356  
  * Manuscript title: Explorative behavior allows the successful finding of ephemeral food resources in the wild  
  * Manuscript authors: Wirowska M., Iwińska K., Borowski Z., Brzeziński M., Solecki P., Boratyński J.S.  
  * Manuscript journal: Behavioral Ecology and Sociobiology  

3. Links to other publicly accessible locations of the data: 
	N/A  
  
4. Links/relationships to ancillary data sets: 
	N/A  
  
5. Was data derived from another source? 
	No


# Data & File Overview


1. File List: 
pca_glis.csv
dat_glis.csv
reg_log_0_glis.csv
reg_log_1_glis.csv
reg_log_2_glis.csv

2. Relationship between files, if important:
	Variables PC1 and PC2 (included in files other than “pca_glis.csv”) were derived from PCA analysis run on data input from the file “pca_glis.csv”.

3. Additional related data collected that was not included in the current data package: 
	N/A

4. Are there multiple versions of the dataset? 
	No
	
  
 # Methodological information


1. Description of methods used for collection/generation of data: 

All methods are available in the publication:
Manuscript number: BEAS-D-22-00356
Manuscript title: Explorative behavior allows the successful finding of ephemeral food resources in the wild
Manuscript authors: Wirowska M., Iwińska K., Borowski Z., Brzeziński M., Solecki P., Boratyński J.S.
Manuscript journal: Behavioral Ecology and Sociobiology

2. Instrument- or software-specific information needed to interpret the data: 
All statistical analyses were performed in R 4.1.2 (R Core Team 2020). Specific packages are listed in the the associated manuscript.

R Core Team. 2020. R: A language and environment for statistical computing. Vienna, Austria: R Foundation for Statistical Computing. https://www.R-project.org.


# Data-specific information for each file


File: **“pca_glis.csv”**
Use in paper: Data input for PCA (described further in the associated manuscript).
Number of variables: 8 (+ lp)
Number of cases/rows: 66
Missing data codes: None
Variable terms:
-	lp = ID number of the behavioral test
-	N_jumps = total number of jumps during the behavioral test
-	N_rearing = total number of rearing (standing on hind legs) events during the behavioral test
-	N_grooming = total number of grooming events during the behavioral test
-	Latency_cent = latency to leave the central zone of arena [s] in the beggining of the behavioral test
-	Distance = total distance made by animal in the arena during the behavioral test [cm]
-	Central = relative time spent in the central zone of the arena during the behavioral test (excluding time before first central zone departure)
-	Corner = relative time spent in the corner zones of the arena during the behavioral test (excluding time before first central zone departure)
-	Walls = relative time spent in the remaining zones of the arena during the behavioral test (excluding time before first central zone departure)

File: **“dat_glis.csv”**
Use in paper: Data used to run LMEs (described further in the associated manuscript) and to calculate the repeatability of head width, body condition and PCs between behavioral tests.
Number of variables: 12 (+ lp)
Number of cases/rows: 66
Missing data codes: None
Variable terms:
-	lp = ID number of the behavioral test
-	ID = ID number of the tested animal (constant between behavioral tests)
-	Hw = Head width of the individual at the time of the behavioral test [mm]
-	mb = Body mass of the individual at the time of the behavioral test [g]
-	feeder = Binary variable of feeder fining success (0 - no feeders found during the whole experiment, 1 - at least one feeder found)
-	age = Approximate age of each individual in year 2020 [years]
-	cond = Body condition (obtained as residuals from the linear relationship between mb and Hw)
-	rhw = Residual head width (Hw) – obtained from second order polynomial regression between Hw and age
-	test = The order of behavioral tests for each individual (A - first test, B - second test)
-	PC1 = Values of first principal component (obtained from PCA on dataset described above) for each behavioral test
-	PC2 = Values of second principal component (obtained from PCA on dataset described above) for each behavioral test

File: **“reg_log_0_glis.csv”**
Use in paper: Data used to run logistic regression (described further in the associated manuscript). All animals are included.
Number of variables: 5
Number of cases/rows: 48
Missing data codes: None
Variable terms:
-	id = ID number of the animal
-	age = Approximate age of each individual in year 2020 [years]
-	feeder = Binary variable of feeder fining success (0 - no feeders found during the whole experiment, 1 - at least one feeder found)
-	age = Approximate age of each individual in year 2020 [years]
-	rhw = Residual head width (Hw) – obtained from second order polynomial regression between Hw and age. For animals tested twice we used mean values (further explained in the associated manuscript)
-	rPC1 = Residual first principal component values(obtained from the linear mixed model where rhw and age were included as covariates). For animals tested twice we used mean values (further explained in the associated manuscript)  

File: **“reg_log_1_glis.csv”**
Use in paper: Data used to run logistic regression (described further in the associated manuscript). Animals captured only at the most peripheral lines of the plot were excluded.
Number of variables: 5
Number of cases/rows: 27
Missing data codes: None
Variable terms:
-	id = ID number of the animal
-	age = Approximate age of each individual in year 2020 [years]
-	feeder = Binary variable of feeder fining success (0 - no feeders found during the whole experiment, 1 - at least one feeder found)
-	age = Approximate age of each individual in year 2020 [years]
-	rhw = Residual head width (Hw) – obtained from second order polynomial regression between Hw and age. For animals tested twice we used mean values (further explained in the associated manuscript)
-	rPC1 = Residual first principal component values(obtained from the linear mixed model where rhw and age were included as covariates). For animals tested twice we used mean values (further explained in the associated manuscript)  

File: **reg_log_2_glis.csv”**
Use in paper: Data used to run logistic regression (described further in the associated manuscript). Animals captured only at two most peripheral lines of the plot were excluded.
Number of variables: 5
Number of cases/rows: 19
Missing data codes: None
Variable terms:
-	id = ID number of the animal
-	age = Approximate age of each individual in year 2020 [years]
-	feeder = Binary variable of feeder fining success (0 - no feeders found during the whole experiment, 1 - at least one feeder found)
-	age = Approximate age of each individual in year 2020 [years]
-	rhw = Residual head width (Hw) – obtained from second order polynomial regression between Hw and age. For animals tested twice we used mean values (further explained in the associated manuscript)
-	rPC1 = Residual first principal component values(obtained from the linear mixed model where rhw and age were included as covariates). For animals tested twice we used mean values (further explained in the associated manuscript)

### Chapter 1

1. Introduction of data mining

Understanding of the process data cleaning 
data cleaning is an essential step


2. Second part
Why Pre-processing?
	real world data can be incomplete, noisy, inconsistent(different format, name, lab), biased abnormal...
	
	preparing the data, preparing the miner
		pprepare the data -> model is build right
		the miner -> right model is build quality of data
	
why data be incomplete?
	attribute of interest are not available
	data was not considered important at the time of transactions, -not recorded
	data were not recorded because of misunderstanding or malfunctions
	data deleted later to save space
	missing/unknown values for observations

Why can data be noisy?
	faulty instruments
	human error
	transmission error....
	techincal limitation
	inconsistencies in naming conventions or data codes
	duplicates 

high quality data?
	accuracy and precision
		no error, more money better! invest for accuracy
	legitimacy and validity
	reliability and consistency
	timeliness and relevance
	completeness and comprehensiveness
	availability and accessibility
	granularity and uniqueness

Tasks in data pre-processing
	data cleaning
	data integration
	data transformation
	data reduction
	data discretisation

Data cleaning
	ignore observation with missing values OR fill...  
	fill in missing values with imputation(by mean? )  
	identify outliers and smooth out noisy data  
	correct inconsistent data  

Data transformation  
	normalization/rescale  
	aggregation  
	generalization  
	variable construcion/feature extraction (replace or construct from existing attributes)

Data reduction  
	reducing the number of variables  
		aggregation  
		
	reducint the number of variable values  
		binning (by grouping them into intervals)  
		clustering, grouping values in clusters  
		aggregation or generalization  
	reducing the number of observations  
		sampling  


### Chapter 2
**Ethical Considerations in Data Mining**
	Data Ethics  
		 

**Information Security and privacy**
	

**Open data**
free access - not hidden behind a payall or anything
	login step might need but 
anyone can share, keep it open and tell where it came from
with sufficient metadata to enalbe anyone to use it meaningfully

Sharing is caring
	benefit of open data is

use and produce





### Chapter 3

1.
Know your data 
	understand basics of data collection to be critical

Data collection had gone bad!
	migraine study, devies gone missing
	IMU studies, bluetooth connectivity,
	sensor attachmen problems
	battery running out
	people do not read the instructions
	with mobile phones the daa collection stops when screen is turned off
Planing planing and planing
	Define the problem - collect data, big data problems, plan the procedures
	define the problem, goals and objectives
		data types, scale, intervals
		methodologies, devices used for data recording
		how to deliver and store the data
		rationale for collectiont the data
		what insight the data might provide
		DOcumentation!
		Repeatability, reproducibililty, accuracy and stability

Procedure
	Plan
	first data collection, one subject, one device
	plan and iterate
	final data collection
	reporting the problems in data collection

sample size:
	defineinig minimim sample size for statistal analysis
	drop out rate
	how often 
	long time scale
		
Methods of data collection
	background information collection
	quetionaries
	interviews
	direct observation (watching what happening)
	sensor observation (what sensor readings are, frequencey)
	
Planning
	keep it simple
	discuss the collections, learn from others mistake
	schedule the collection
	iterate learn from the data
	do not be afraid to stop data collection

Differences 
	Stationary stay similar during time
	Non-statioary elements	 	
		environmental objects, living object - change non-stationary
		seasonal change,
		processes due erosion of path ,

Time-series issues
	best to collect data from distinct time windows(min, days, weeks, years)
	help to avoid using the same data in modelling and testing


2. Humans

- Every humans is different
- Change/evolve in during time(NON-stationary)

Ethical aspects
	why?
	
	Respect the persons
	Beneficence -do not harm, maximize possible benefits, minimize possible harms
	Justice

	Informed consent:	
		give their consent freely and voluntarily
		have the decisional capacity to understand the information presented to them
		risks - physical psychological, social, legal, ecoomic
		benefit should be greater than the risk
		compensation should not be too attractive and blind the risks
		privacy and confidentiality

Rndomized controlled trial(RCT)
	Parallel-group (placebo or treatment)- a group get the other group not 
	crossover - over time, each participant receives an intervention
	cluster - pre-existing groups (schools and villages)
	Factorial - 

BIAS
	RCT is considered a golden standard to avoid bias in medical treatment tests but
	there are! still
	researcher bias - whose 
	respondent bias - do not tell truth
	Human data bias - 1 person data, mens data?, athletes data? 

Data colletion planning
	report: problems, be open with those problems, problem will bias your study, 
	
plan plan plan
know your data 

	

### Chapter 4
**Merging signal and balancing**

1. Merging Data
	
Data coming from Multiple sources 
	
Combine data via add more features or add more observations(same unit, frequencey, gathering protocal)

Formats
	different format, csv, txt, tabular, commar, header or not
	cultural differences (decimal thousand)
	different unit(inch meter)
	different timestamps (unix time stamp vs datetime)
	
Data Collection plan
	same label with different meaning (make it clear)
	different conditions (flat or hill, summer or winter?)
	seonsor placement (same position?, different devices?)
	differences in study subjects (collected from children or elderly)
	different sampling rates(frequnecy)
	it is possible that data collection plans of two datasets are so different that they cannot be combined

Undersampling
	greate common divider

Oversampling 
	least common muliplier

unit and frequency

do not use if not documented well enough

2. too much data or too less data?

Too much data 
	simple random sample with replacement
	simple random sample without relacement
	balanced sample -for imbalanced dataset
		combination of both, two classes problem -different sample sizes for each class
		class wise sampling, 

Not enough data
	simple random sample with replacement
	noise injection - add noise to original instances and add them to the dataset
	artificial data?? - synthetic data, describing original data set D using parameters such as mean and variances, distribution  
	SMOTE - find k nearest neighbours, take vector between knn and data sample, multiply vector random(0-1), add this to the original sample 

Biased data (imbalanced data)
	some classes have too much data and or some classes do not have enough data, approach class wise
	differnt approach for each class

Try sampling or create artificial data
 

3. Balancing

Imbalanced data 
	problem: why?
	it is not easy to get balanced data (sick person, healty person) ratio is not even always
	easy to obtain results that looks good but in reality is not good	

Performance metrics
	one metric not enough to measure performance

	accuracy = correctly classified / all instances - (TP + TN)/(TOTAL) 
		most commonly used performance metric but very dangerous especially imbalanced dataset
	accuracy paradox: misleading
		low accuracy does not mean model has low predictive power "Imbalanced data set"
	balanced accuracy? - ( TP/(TP+FN) + TN(TN+FP) )/2
	
	Precision - TP/(TP+FP)
	
	Recall - TP / (TP+FN)
	
	Specificity = TN(TN + FP)

	F1 score = 2*((precision*recall)/(precision+recall))



		


	



Confusion matrix
	    P   N (predicted)
	P  TP  FN 		20   5    0  25   same accuracy but  
	N  FP  TN		20 255    0 275


### Chapter 5
**Missing Values**

1. 
missing values in data sets are very common

cause reason for missnig data?  
	equipment errors
	incorrect measurements (out of range)
	human factor(mistakes, entering data)
	non-response in surveys

why is important Missing values? 
	modelling methods assume that data is complete!  
	
effect of missing data?  
	bias
	misleading conclusions
	limit the generalizability of the research findings


understand why some values are missing is important!!
	mechanism that caused the missing values
	conditional questions in a survey
	some data relevant only in some cases 

How to Handle?

Missing completely at random (MCAR)
	probatility that a value is missing does not depend on the missing value itself or the observed data
	ignore MV does not bias the results although some information is lost
	e.g. malfunctioning equipment or random sampling of population
	not realistic assumption 

Missing at random (MAR)
	probability an observation is missing depends on the observed data(there is reason brand?) but not ont he missing data
	e.g. certain sensor brand fails more ofthen than another brand or stratified sampling(population by races, but random missing in each group)

Missing not at ramdom(MNAR)
	the model for missingness is unknown(not explained by the observecd data)
	probatility of a value being missing could be explained by the missing value itself 
	e.g. sensor fails more often on certain data value range than in others or nonresponse in survey question is more frequent in people 		with a disease than without that disease
	MNAR analyses are difficult and do not necessarily perform better than metnods assuing MAR
	

2. what can we do to fix missing value problem?
	recollect the data - impossible or expensive
	
	delete the missing values or imcomplete cases 
		- if the data is MCAR 
		- it comes with cost, losing statistical power
	data is not often MCAR not realistic one
	BUT deletion is he most common method used.


Complet-case analysis/list wise deletion (very wasteful)
Available-case analysis/Pair-wise deletion
		
fill missing value -> imputation! how? with what?
Imputation (find good candidates)
	fill with similar instances if missing values are rare! hot deck, or cold deck
	mean imputation -easy!
		global - all available
		stratified - instances with same classes

	by Mean global or stratified
	by Regression
	by stochastic regression -underestimate 

what to impute
multiple imputation 
machine learning based 
Missing at random assumption still holds
 
- Muliple Imputation

- Maximum likelihood estimaion

- Time series/logitudinal data
	last observation carried forward (LOCF)
	baseline observation carreid forward 


3. 

### Chapter 6
 
**Noisy data signal saturation and outliers**
1. Noisy data

attribute noise: errors, 
level noise: 

robust learners
	normal variation
	models are similar with clean and noisy data

data polishing
	
data pollution
	
	
Signal saturation	
	threshold value, max min values are overrepresented in the data

2. Data quality issues (Outliers)
Data examples with behaviours that are very different from the expectation
	individual cases or clumps
It is important to investigate why there are outliers
type of outliers
	Global outliers (individually or clumps)
			
	Contextual outliers 
		whether a value is considered outlier or not depends on the context

	Collective outliers 
		
Detection
	supervised
			
	unsupervised
	semi-supervised


### Chapter 7
Normalization, standardation, transformation

Pre-processing

1. Normalization/scaling
	adjusting values measured on different scales to a notional 

why need this?
	to speed up some learning techniques
	to be required to learn learning technique require normalization
	help to prevent attributes with larget ranges to outweight ones with small ranges
	note that you may need to store your normalization parameters to return back to original scale ini reports 
		for scaling new data later

Min_max normalization
	raige[0,1]
		v = (v-vmin) / (vmax-vmin)
	any arbitrary range[a,b]
		v = (v-vmin)(b-a)/(vmax-vmin) + alpha

	log-sigmoidal, tan-sigmoidal
	
Standardization or z-score standardization
	transform the data to cener by remoin the mean value of each variable

Decimal scaling
	?	

2. Classification of the continuous variables
discretization of continuous variables is used?
	group oof observations 

	median split to create equal groups, discretization half group good, half bad

	qunatitative scale relfects meaningful qualitative differences


categorizaing, discretizating or dichotomizing continuous vaiables
	some methos accept only categorical variables
	may simplify analysis and interpretation
	simplicity may be gained at a high cost - new problems coming
	categorizing is not recommendable -avoid it if possible, plan differently

problem? from the classification?
	loss of information, what is boundary?
	categorization does not make use of within-category informaion, loss of within category information
	comparison with other studies that used differnt cut-points becomes impossible
	categorizing one continuous variable can make another variable appear associated with the outcome??? biased

information loss cased by dichotomization
	loss correlation 

what to do with categorical variables?
	depends on the methods
	choose method that allow the variable type factor
	dummy-coding (ont hot encoding)

How to classify?
	median split
	distinctive groups
	eqaul lengths 
	equal group sizes

3. Data reduction
efficiency:
	data warehouse my store TB of data, complex data analysis, mining takes a very long time o run on he complete dataset
	obtains a reduced representation of the dataset 

	reducing the number of variables
	reducing the number of varialbe values?
	reducing the number of observation

data aggregation and generalization

variable construction 
	-domain knowledge, combine or split existing variables into new one, that has higher predictive power or more meaningful

numerosity reduction  	
	technique of choosing smaller forms of data representation to reduce the volume of data
	parametric
		model(regression or non-linear models) is used to estimate the data
		the model paramters are stored instead of the actual data, polynomial
	nonparametric
		non parametric methods used for storing reduced representations of the data
		like histograms, clustering, sampling

principal component analysis (PCA)

discrete wavelet transform
	very high dimensionality data with less number of observations 

	
4. Transformation to normalitiry

why normality matters?
	epsilon do normal distribution 	
	test for normality (check is the data? normal or not)
	
solutions for non-normality
	use non-parametric methods (statistical test)
	transformations for normality after that 
	transformation may lead to more convenient way of representing information as well
	choose method that allows other distribuions

BOX-COX transformation family
	box-cox transformations are a family of useful transformations to achieve normality
	bc transformaion is not a guarantee for normality after that
	worth try
	bc works valid only for positive value
	



### Chapter 8

sample size
	size of sample, error rate is converge when training and test data is large enough
	overfiting

	larget training set may result 
better to have more data for predicive modeling 

partitioning for training and testing
	adjecent data, random selection is not good for temporally dependency measurements data set,
	avoid ramdom sampling, take sample different location, first part and second part
	sliding window with overlapping windows-avoid random , for partitioning 
	
model selection
	simpler models more generalizable, less overfitting
	interpretability
	computational complexity
	
 
predictive modeling need more larger dataset than explantory model


indivisual vs population

activity recognition


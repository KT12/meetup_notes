### New Haven Data Science Meetup  
#### Aetna Health Care Fraud Detection System  
Aleksandar Lazarevic  
Mark Kanner  

3/22/2017

Presentation slides [here](https://drive.google.com/open?id=0BzeY9Dxv2ToSRmF1V3pudFg0OHJWMTAwNHExMVY5TTJ0QmRj)

1B claims since beginning 2017

4 V's
Volume, variety, velocity, veracity

Use hadoop, SparkML, Python, R, SAS

Data preprocessing takes a long time

Partner with Fraud Special Investigation Unit of Aetna
Social network analysis to discover fraud rings
Anomaly detection

Waste - errors, incorrect claims, perhaps no ill intention
Abuse - gaming system, billing agencies help hospitals raise revenue
Fraud - intentionally submitting wrong claims, upcoding

Takes 6-8 months to prove fraud.  Try to change abusive behavior through communication with provider.

Feature generation also takes time

'Fraud' does not have much labelled data.  Setting the problem correctly is key.  Not solving a problem which already exists.

Deep learning helps but cannot use it all the time because need to explain to business partners.

Supervised machine learning models - use historical info about previously overpaid claims.
Problems:
Unbalanced classes (3-5%)
Partial/inaccurate labels (undetected overpaid claims in history)
Temporal nature of data
Heterogeneous nature of data (data differs depending on provider)
Many categorical variables (provider #, procedure)

Convert provider and member ID's into other variables.  Partner or not partner, rate from contract, service location.  Member ID > age, gender, plan benefits, COB, prescriptions.

Diagnosis codes > burn due to waterski on fire!

Technical approaches
Generate more actionalbe features
* Domain knowledge
* Characterize providers
* Better capture categorical data

Build several models to capture different overpay problems

Rare class modelling techniques
* Oversampling of small class/undersampling of majority class
* SMOTE/ROSE
* Cost sensitive learning
* Combine ensemble learning with methods above (random forests/boosting)

Active Learning
* Query human analysts to check on uncertain claims (near decision boundaries)

Update model frequently
* Data is near-streaming frequency

Fraud Detection
Provider features
Aggregate at provider level
Avg patients/time
Claim lines
Date of service on holiday
Behavioural changes
Velocity (no claims to 60 members in one day)
Geospatial (100 mi ambulance ride in Manhattan)
Social connections between provider and user, pharmacies (80 member company, half were haemophiliacs - company had interest in pharmacy, average cost of haemophiliac drugs is $80k/year.  Contract was terminated)

Extremely important to do analysis within peer group (cardiologists vs cardiologists, etc).

Labs are responsible for doing unnecessary procedures.

Harder to call out rural hospital on waste or fraud vs small provider in Manhattan.  Need rural coverage (so there is negotiation which goes on)

Can only capture 50% of fraud - better to do it in prepay phase

Not using enough data (utility bills, address, mobile usage etc).  Trying to partner with Lexis Nexis.  Need to know if provider is under financial duress.

Technical Approaches
Leverage SIU knowledge
* Fraud types already seen
* Hypothesis driven new rules developed in partnership

Supervised models for detecting variations of known fraud schemes
* Weighted random forests
* Gradient boosting w SMOTE oversampling
* Deep learning

ANomaly detection
* Z scores sum
* Distance/density

Stastical approach does not handle multimodal high D data
Provider features
* Diff from provider peer group
* Claim spike activity
* Geographic distance b/w provider and members
* Unusual $ paid per claim and per patient

* Nearest neighbor approach - outliers have greatetst distance to neighbors
* Density approach - takes into account density of neighbors
* Need good features then LOF in R

Anomaly detection != fraud
Miscoding procedures is a problem


Detecting overtreatment of patients (similar to recomendation engine)
High cost for low risk
* Spike in total paid amount
* More expensive procedures than other chiropractors
* High spend on patients
* Only 4 procedure codes used

Dealing with DS is not what you think
* Chase info
* Work w partners
* Be careful what you wish for
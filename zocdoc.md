## AWS Meetup
#### Leveraging AWS and Machine Learning to Power Search at Zocdoc
Hosted by [ZocDoc](https://www.zocdoc.com/)
4/18/2017

Introduction to Machine Learning [presentation](https://s3.amazonaws.com/meetup-ml/Intro+to+ML.pdf) by David Ping, AWS Solutions Architect  

#### How Zocdoc leverages machine learning and AWS
Pedro Rubio, Engineering Manager, Zocdoc
Brian D’Alessandro, Director of Data Science, Zocdoc

#### Engineering Section  
Everything they do is regulated (healthcare).

Search window on website is constantly being improved by engineering

Search window on website:
Uses a lot of elastic search
Need to parse intent of user

Need to take into account distance, availability, and ratings when ordering results.

Multi arm bandit is like mini AB test.  Sometimes randomize some part of the results.

#### Data Science Section  
Marketplace: find doctor
Two way market - patients and doctors finding each other
Some doctors only do certain procedures
Need search algorithm to meet regulations

2 stage data ETL
Redshift allows SQL users to utilize the data throughout the co

Interesting findings:
* 3rd week of January 2017 saw more searches for therapists (what could have happened this year?)  
* Doctors who smile see 10% higher click conversion (comparing smile vs no smile at every positional rank)  

#### Q/A section
Human review for recommendations through medical curation team.  They review matches between search terms and recommendations.

Use [mean reciprocal rank](https://en.wikipedia.org/wiki/Mean_reciprocal_rank) a lot in evaluating recommendations.

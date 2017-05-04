# HIPAA in the Cloud

[How Flatiron Health uses AWS to iterate and scale our healthcare data pipelines](https://www.meetup.com/AWS-NYC/events/239367206/)

Dan Eisenberg
Engineering Manager

AWS Big Data Week
May 3, 2017

Prototpe >> Scale >> Deploy
AWS helps manage cycle

Enables cancer researchers to learn from the experience of every patient

Because only 4% of cancer patients are enrolled in clinical trials, researchers don't understand what happens to many patients.

HIPAA makes things complicated
Storage, transmission, access is limited
Encryption required

For cancer, data is not nicely structured.  Faxed reports!

### Massive Variation

* Every patient is different
* No standard data models
* Realistic mock data is hard to generate

First lesson: develop against real data as fast as you cancer
Use S3 and EC2

Second lesson:
Doc types are not normalized
Design architecture which enables rapid iteration

Third lesson:
Anticipate scaling by keeping transformations small and idempotent (can run more than once without worry)

i.e. separate doc categorization and OCR tasks >> throw it to Python Celery

PostgreSQL is HIPAA compliant

Last lesson:
Use services to isloate systems and control access
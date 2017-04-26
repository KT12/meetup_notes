## LAB: My First Cluster with MongoDB Atlas  
### Jay Gordon
Development Advocate - NYC
[@jaydestro](https://github.com/jaydestro) - jay.gordon@mongodb.com
4/25/2017  
[Slides here](https://www.slideshare.net/JayGordon9/my-first-cluster-with-mongodb-atlas)
[Photo recap](https://goo.gl/photos/qn4JbDD5i8atCf4c8)

MongoDB Atlas is fully managed cloud
* 3 EC2 nodes in AWS cloud
* Atlas self-heals
* Redundant

Benefits
* Robust backups
* Group is isolated group of nodes

### MongoDB Atlas Lab

Download [here](https://www.mongodb.com/download-center#community)
Instructions to load on Ubuntu [here](https://docs.mongodb.com/master/tutorial/install-mongodb-on-ubuntu/)
Ubuntu troubleshooting [here](https://docs.mongodb.com/manual/tutorial/install-mongodb-on-ubuntu/)


### Login script:  
Automatically generated from Atlas website:  

mongo "mongodb://mongodbdemo-shard-00-00-ozq7j.mongodb.net:27017,mongodbdemo-shard-00-01-ozq7j.mongodb.net:27017,mongodbdemo-shard-00-02-ozq7j.mongodb.net:27017/test?replicaSet=MongoDBDemo-shard-0" --authenticationDatabase admin --ssl --username <USERNAME> --password <PASSWORD>

Once in the shell:

use mongodblab

db.firstdoc.insert{{"Database Name" : "MongoDB"}}

### Hierarchy of document organization
Database >> Collection >> Document

show databases
show collections

db.firstdoc.find().pretty()

### Command to load json file into primary node
Use the primary node, look up thru Atlas website
mongoimport --host mongodbdemo-shard-00-00-ozq7j.mongodb.net:27017 --db zips --type json --file ~/Downloads/zips.json --authenticationDatabase admin --ssl --username <USERNAME> --password <PASSWORD>

Can now [query](https://docs.mongodb.com/manual/tutorial/query-documents/) using JSON:

* Look for counties with population == 5526
db.zips.find({"pop" : 5526}).pretty()

### Checkout other resources
https://mongodb.influitive.com/users/sign_in

https://university.mongodb.com/

Compass - viz tool for MongoDB

Can query the back up data of a database-  ie restoring 2TB of data is very expensive.  No need to restore - can just directly query the backup.
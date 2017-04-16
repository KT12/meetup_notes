## NYC NoSQL Meetup

Peloton CTO and co founder Yoni (sp?)
Peloton makes tablet and bike
Most popular time is Sunday morning

### Couchbase and N1QL
Ravi Mayuram
[Slides here](https://www.slideshare.net/EricDavidBenariPMP/svp-of-couchbase-the-exciting-world-of-nosql-scaling-nosql-data-n1ql-vs-sql-mobile-databases)
Data is the new oil
NoSQL came out of the pain of Google and FB - horizontal scaling instead of vertical scaling.

Brings more logic to the data.

Use vector clock to determine causality

XDCR can be used as backup or disaster recovery.

PokemonGo used couchbase, but had a problem b/c the were using mysql.  Only running 8 nodes >> optimized queries and added secondary indices.  Ran smoothly afterwards.  8 nodes >> 72 nodes, but data has never left the original 8 nodes.

Data doesn't have to move.

#### Programming
JSON  +  SQL =  N1QL
JSON is lingua franca of internet + power of SQL
N1QL maniuplates schema on the fly, not just data.

Ad hoc querying and no need for another application.
Heavy lifting is done at the data level.

Can do array indexing as well.
Also includes stemming and lexical analyzer.

United built a crew management system over couchbase.

Clutser size = how is it determined?  Depends on how much you want to do in memory.  NOt necessarily based on size or speed.

System of engagement. System of record is old infa.
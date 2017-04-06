## Data Science + You
New York Python Meetup Group
@ SimulMedia
[Event Info here](https://www.meetup.com/nycpython/events/237182654/)

### Frédéric Bastien
### Theano
Theano is:
* Language
* Compiler
* Python module

Features
* Lazy eval
* GPU support
* Symbollic differentiation

Theano has `NanGuardMode` which is useful for debugging.

Fast to develop, fast to run


### Jeff Reback
### pandas
[Presentation slides](https://github.com/jreback/PandasTalks/blob/master/whatsnew/april_2017/Whatsnew%20in%20Pandas.pdf)

Arrow is in memory format
Spark + Parquet + Pandas

#### New Features
`.ix` deprecation > use `.loc` or `.iloc`
Panel deprecation > multi index frame
Can choose compression in pickle
Will support feather
Interval index is actually an index and not strings
`df.agg` has more fuctionality, can customize

LT what's coming
Less copying and memory use
CSV reader will be redone
Unified data types
A lot of unnecessary copying will be removed
Throwing plots to other engines

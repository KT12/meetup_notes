# Scale Agnostic Computing  
## Sean T. Allen
[Sendence](http://www.sendence.com/)
New York Python Meetup Group
Hosted by Peloton
August 17, 2017

#### Scaling from little data to big data is hard  
* Could re-write to scale across multiple processes
* Could run a few versions of it in parallel - smart loader like Celery  
* Scale agnostic >> write app scale agnostic API which runs on scale aware platform

Solution: Sendence Wallaroo
* Managed in memory state
* Guaranteed message processing

Written in Pony
Using Wallaroo, Python will be the performance inhibitor, not Wallaroo

Read:
* [Pat Helland's "Life Beyond Distributed Transaction"](http://adrianmarriott.net/logosroot/papers/LifeBeyondTxns.pdf)

# Manticore: Symbolic Execution for Humans
## Mark Mossberg
Trail of Bits

Program analyzer written in Python
Analyzes binary programs (ie C++ after compilation)

### Part 1: Symbolic Execution 101

Symbolic variables are more akin to algebraic variables

* Important for program analysis
* Useful for testing and security

### Part 2: Manticore

Tips for designing API
Look at other mature projects, standard library
Re-use familiar interfaces
More diverse the background, the better

* Josh Bloch - How to Design a Good API and Why it Matters*
Lower costs of using API

Keep it minimal
No. 1 Rule: If in doubt, leave it out
Cannot remove functionality once it's there
Be intentional about features

Python features which allow you to grow without breaking API
* Default params
* Properties
* Dynamic typing

Be critical (even pedantic) with yourself
Be iterative
Naming is important
Think like new user

### Manticore Testing
Actually implements CPU emulators
Software implementation of hardware

Unit tests
Use decorators to implement unit tests

Can autogenerate unit tests
CI testing for example code

### Open Source

Python infrastructure is easy, free
* Documentation: Sphinx, readthedocs, github
* Package mgmt: pypi + pip
* Testing: Travis CI

Manticore office hours via Slack
"Easy" issue tracker means people might come by and fix your code for you

`pip install manticore`
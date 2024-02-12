There is a fundamental problem in concurrency and that is change of data from multiple sources :
- Two or more pointers try to access the same data
- At least one is writing to the data
- There's is no mechanism to sync them
This may lead to those accessing reading data that is changing etc.
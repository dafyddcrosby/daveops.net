# MongoDB
@databases

Queries
-------
	// Show current operations
	db.currentOp()
	// Show long running queries 
	db.currentOp()['inprog'].filter(function(x) {return x.secs_running > 10})
	// Kill a query
	db.killOp(12345)

Administration
--------------
	// Drop database
	db.dropDatabase();
Rotate logs
-----------


 kill -SIGUSR1 <mongod pid>

Documentation
-------------



* <http://docs.mongodb.org/manual/administration/production-notes/>



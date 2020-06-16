# Final: Question 3


Suppose an instance of MongoClient is created with the following URI string:

```
from pymongo import MongoClient

uri = "mongodb+srv://m220-user:m220-pass@m220-test.mongodb.net/test"
mc = MongoClient(uri, authSource="admin", retryWrites=True, connectTimeoutMS=50)
```

The variable representing our client, mc, will:



- [x] **automatically retry writes that fail.**
- [ ] allow a maximum of 50 connections in the connection pool.
- [x] **use SSL when connecting to MongoDB.**
- [ ] authenticate against the test database.
- [x] **wait at most 50 milliseconds for timing out a connection.**

# Final: Question 3

**Problem:**

Suppose an instance of MongoClient is created with the following settings:
```
WriteConcern wc = WriteConcern.MAJORITY.withWTimeout(
    2500,
    TimeUnit.MILLISECONDS
);

MongoClientSettings settings =
    MongoClientSettings.builder()
        .applyConnectionString(
          "mongodb+srv://m220-user:m220-pass@m220-test.mongodb.net/test"
        )
        .writeConcern(wc)
        .retryWrites(true)
        .build();

MongoClient mongoClient = MongoClients.create(settings);
```
- [x] automatically retry writes that fail.
- [x] use Write Concern { w: majority } by default.
- [ ] allow a maximum of 50 connections in the connection pool.
- [ ] use Read Concern { r: majority } by default.




Let's take the following code, where URI is a connection to your Atlas cluster using an SRV record.

```
MongoClientSettings settings = MongoClientSettings.builder() \
    .applyConnectionString(new ConnectionString(URI)).build();
MongoClient mongoClient = MongoClients.create(settings);

// TODO do a read on the cluster to ensure you are connected

SslSettings sslSettings = settings.getSslSettings();
ReadPreference readPreference = settings.getReadPreference();
ReadConcern readConcern = settings.getReadConcern();
WriteConcern writeConcern = settings.getWriteConcern();
```

Which of the following variables contained the associated value?



- [ ] readPreference.toString() = "primary"
- [x] **writeConcern.asDocument().toString() = "{ w : 1 }"**
- [ ] readConcern.asDocument().toString() = "{ }"
- [x] **sslSettings.isInvalidHostNameAllowed() = true**
- [ ] sslSettings.isEnabled() = false

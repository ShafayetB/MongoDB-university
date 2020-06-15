# Lab 4.2: Aggregation Performance

**Problem:**

For this lab, you're going to create an index so that the following aggregation query can be executed successfully.

Before you work on your solution, delete all indexes for the restaurants dataset:

```
db.restaurants.dropIndexes()
```

Then, run the following query and you will receive an error.
```
db.restaurants.aggregate([
  { $match: { stars: { $gt: 2 } } },
  { $sort: { stars: 1 } },
  { $group: { _id: "$cuisine", count: { $sum: 1 } } }
])
```

```
{
  "ok": 0,
  "errmsg": "Sort exceeded memory limit of 104857600 bytes, but did not opt in to external sorting. Aborting operation. Pass allowDiskUse:true to opt in.",
  "code": 16819,
  "codeName": "Location16819"
}
```

Identify why this error is occuring, and build an index to resolve the issue.

Keep in mind that there might be several indexes that resolve this error, but we're looking for an index as small as possible that services this command.

In the text box below, submit the index that resolves the issue.

For example, if you ran:

```
db.restaurants.createIndex( { foobar: 1 } )
```
to create the index that fixes the error, then you would enter the following document which lists the fields indexed into the text box:

```
{ foobar: 1 }
```

<details>
  <summary>Click here for the solution</summary>
    Answer: {stars:1}
</details>


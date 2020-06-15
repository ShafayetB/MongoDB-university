# Quiz

## Introduction to Indexes

**Problem:**

Which of the following statements regarding indexes are true?

- [x] **Indexes are used to increase the speed of our queries.**
- [x] **The _id field is automatically indexed on all collections.**
- [x] **mIndexes reduce the number of documents MongoDB needs to examine to satisfy a query.**
- [x] **Indexes can decrease write, update, and delete performance.**

## Single Field Indexes Part 2

**Problem:**

Which of the following queries can use an index on the zip field?

- [x] **db.addresses.find( { zip : 55555 } )**
- [ ] db.addresses.find( { city : "Newark", state : "NJ" } )
- [ ] db.addresses.find()

## Understanding Explain

**Problem:**

If you observe the following lines in the output of explain('executionStats'), what can you deduce?

```

"executionStats" : {
  "executionSuccess" : true,
  "nReturned" : 23217,
  "executionTimeMillis" : 91,
  "totalKeysExamined" : 23217,
  "totalDocsExamined" : 23217,
  "executionStages" : {
    "stage" : "SORT",
    "nReturned" : 23217,
    "executionTimeMillisEstimate" : 26,
    "works" : 46437,
    "advanced" : 23217,
    "needTime" : 23219,
    "needYield" : 0,
    "saveState" : 363,
    "restoreState" : 363,
    "isEOF" : 1,
    "sortPattern" : {
      "stars" : 1
    },
    "memUsage" : 32522511,
    "memLimit" : 33554432,```

- [x] **The index selected for the query was not useful for the sort part of the query**
- [x] **An in-memory sort was performed**
- [x] **The system came very close to throwing an exception instead of returning results**


## Understanding Explain for Sharded Clusters

**Problem:**

With the output of an explain command, what can you deduce?

- [x] **The index used by the chosen plan**
- [x] **If a sort was performed by walking the index or done in memory**
- [ ] All the available indexes for this collection
- [x] **All the different stages the query needs to go through with details about the time it takes, the number of documents processed and returned to the next stage in the pipeline**
- [ ] The estimation of the cardinalities of the distribution of the values

## Sorting with Indexes

**Problem:**

Given the following schema for the products collection:

```
{
  "_id": ObjectId,
  "product_name": String,
  "product_id": String
}
```

And the following index on the products collection:

```
{ product_id: 1 }
```

Which of the following queries will use the given index to perform the sorting of the returned documents?

- [x] **db.products.find({}).sort({ product_id: 1 })**
- [x] **db.products.find({}).sort({ product_id: -1 })**
- [x] **db.products.find({ product_name: 'Soap' }).sort({ product_id: 1 })**
- [ ] db.products.find({ product_name: 'Wax' }).sort({ product_name: 1 })
- [x] **db.products.find({ product_id: '57d7a1' }).sort({ product_id: -1 })**


## When you can sort with Indexes


**Problem:**

Which of the following statements are true?

- [x] Index prefixes can be used in query predicates to increase index utilization.
- [x] Index prefixes can be used in sort predicates to prevent in-memory sorts.
- [x] We can invert the keys of an index in our sort predicate to utilize an index by walking it backwards.
- [ ] It's impossible to have a sorted query use an index for both sorting and filtering.


## Multikey Indexes

**Problem:**

Given the following index:

```
{ name: 1, emails: 1 }
```
When the following document is inserted, how many index entries will be created?

```
{
  "name": "Beatrice McBride",
  "age": 26,
  "emails": [
      "puovvid@wamaw.kp",
      "todujufo@zoehed.mh",
      "fakmir@cebfirvot.pm"
  ]
}
```

- [ ] 1
- [ ] 2
- [x] **3**
- [ ] 4

## Partial Indexes

**Problem:**

Which of the following is true regarding partial indexes?

- [x] **Partial indexes represent a superset of the functionality of sparse indexes.**
- [x] **Partial indexes can be used to reduce the number of keys in an index.**
- [ ] Partial indexes don't support a uniqueness constraint.
- [x] **Partial indexes support compound indexes.**

## Text Indexes

**Problem:**

Which other type of index is mostly closely related to text indexes?

- [ ] Single-key indexes
- [ ] Compound indexes
- [x] **Multi-key indexes**
- [ ] Partial indexes

## Collations

**Problem:**

Which of the following statements are true regarding collations on indexes?

- [ ] MongoDB only allows collations to be defined at collection level
- [x] **Collations allow the creation of case insensitive indexes**
- [ ] Creating an index with a different collation from the base collection implies overriding the base collection collation.
- [x] **We can define specific collations in an index**

## Wildcard Index Type: Part 2

**Problem:**

Using the wildcardProjection flag with Wildcard Indexes, we can:

- [ ] specify a set of fields in the Wildcard Index to project with $project.
- [x] **exclude a set of fields from the Wildcard Index.**
- [x] **include a set of fields in the Wildcard Index.**


## Wildcard Index Use Cases

**Problem:**

Which of the following are good reasons to use a Wildcard Index?

- [x] **The query pattern on documents of a collection is unpredictable.**
- [ ] A collection has documents with many different fields.
- [x] **An application consistently queries against document fields that use the Attribute Pattern.**



# Quiz

## Complex Aggregations

Which of the following classes can be used to compose aggregation pipeline stages and expressions ?



- [x] **com.mongodb.client.model.Aggregates**
- [x] **com.mongodb.client.model.Accumulators**
- [x] **com.mongodb.client.model.Filters**

## BBasic Writes - Updates

What is true about the Document Object inserted into a collection using the insertOne method?



- [x] **It contains the _id of an inserted document even if the Document did not have an _id value prior to insertion.**
- [ ] It can tell us whether the operation was acknowledged by the server.
- [ ] It is a cursor.

## Write Concerns

Which of the following Write Concerns are valid in a 3-node replica set?



- [x] **w: 0**
- [x] **w: 1**
- [ ] w: 4
- [ ] w: 5
- [x] **w: majority**

## Update Operators

When changing a field value in a single document it is best to use



- replaceOne
- **updateOne**
- updateMany
- deleteOne

## Basic Joins

Why did we use a let expression with expressive $lookup, when joining the comments and the movies collection?



- To store the output of the pipeline in the movie_comments field.
- **To use fields from the movies documents in the pipeline.**
- To use fields from the comments documents in the pipeline.
- To count the number of comments documents.

## Basic Deletes

Which of the following is true about deleting documents using the MongoDB Java Driver?



- [x] **deleteMany can delete any number of documents.**
- [ ] MongoDB Java Driver can only delete one document at a time.
- [x] **DeleteResult objects contain the number of deleted documents.**
- [ ] deleteOne will not return a DeleteResult object.
- [x] **deleteOne can only delete one document.**


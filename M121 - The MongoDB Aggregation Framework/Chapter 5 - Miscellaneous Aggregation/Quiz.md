# Quiz

## The $out Stage

Which of the following statements is true regarding the $out stage?

- If a pipeline with $out errors, you must delete the collection specified to the $out stage.
- **$out will overwrite an existing collection if specified.**
- $out removes all indexes when it overwrites a collection.
- Using $out within many sub-piplines of a $facet stage is a quick way to generate many differently shaped collections.

## $merge Overview

In MongoDB 4.2, the $merge Aggregation stage:

- [x] can output to a sharded collection.
- [x] can output to a collection in the same or different database.
- [x] can merge documents from an Aggregation and a target collection.

## $merge Syntax

**Problem:**

Consider an Aggregation Pipeline using the new $merge stage that outputs to the employee_data collection.

If we are not expecting to find any matching documents in the employee_data collection, which of the following stages should we use?

```
{
  $merge: {
    into: "employee_data",
    whenNotMatched: "insert",
    whenMatched: "merge"
  }
}
```
```
{
  $merge: {
    into: "employee_data",
    whenNotMatched: "fail",
    whenMatched: "replace"
  }
}
```
```
{
  $merge: {
    into: "employee_data",
    whenNotMatched: "discard",
    whenMatched: "replace"
  }
}
```
```
{
  $merge: {
    into: "employee_data",
    whenNotMatched: "insert",
    whenMatched: "fail"
  }
}
```
```
{
  $merge: {
    into: "employee_data",
    whenNotMatched: "fail",
    whenMatched: "merge"
  }
}
```
<details>
  <summary>Click here for the solution</summary>
    <ul>
      <li>{
  $merge: {
    into: "employee_data",
    whenNotMatched: "insert",
    whenMatched: "fail"
  }
}
</li>
    </ul>
</details>

## Views

Which of the following statements are true regarding MongoDB Views?

- Inserting data into a view is slow because MongoDB must perform the pipeline in reverse.
- A view cannot be created that contains both horizontal and vertical slices.
- Views should be used cautiously because the documents they contain can grow incredibly large.
- **View performance can be increased by creating the appropriate indexes on the source collection.**

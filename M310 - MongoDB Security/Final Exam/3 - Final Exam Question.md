# Final: Question 3

Given the following audit filter:

```
{
  "$or": [
    {
      "atype": "authCheck",
      "param.command": {
        "$in": [
          "find",
          "insert",
          "delete",
          "update",
          "findandmodify"
        ]
      }
    },
    {
      "atype": {
        "$in": [
          "createCollection",
          "dropCollection"
        ]
      }
    }
  ]
}
```

Which of the following commands would be logged by this audit filter?

Note: You can assume that auditAuthorizationSuccess is set to true.

- [x] **db.products.findOne({product: 'Door Hinge'})**
- [x] **db.products.insert({product: 'Amplifier'})**
- [x] **db.products.find({product: 'Candle'})**
- [ ] show dbs
- [x] **db.products.insertOne({product: 'Basket'})**

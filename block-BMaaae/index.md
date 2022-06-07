writeCode

Write code to:-

- create a database named `sports`.

```
use sports
```

- list all databases present in local mongod server.

```
show dbs
```

- create 3 collections named `cricket`, `football`, `TT` in sports databse.

```
db.createCollection('cricket')
db.createCollection('football')
db.createCollection('TT')
```

- add multiple players in those collections which should have fields like `name`, `age` and `email` and `bid_price`.

```
db.cricket.insertMany([{"name": "Sachin", "age": 50, "email": "sachin@gmail.com", "bid_price": "15 Lakh"}, {"name": "Dohni", "age": 40, "email": "dohni@gmail.com", "bid_price": "17 Lakh"}, {"name": "Virat", "age": 30, "email": "virat@gmail.com", "bid_price": "18 Lakh"}])

db.football.insertMany([{name: Messi, age: 45, email: messi@gmail.com, bid_price: 15 Lakh}, {name: Ronaldo, age: 40, email: ronaldo@gmail.com, bid_price: 20 Lakh}, {name: Neymar, age: 30, email: neymar@gmail.com, bid_price: 22 Lakh}])

db.TT.insertMany([{name: Sachin, age: 50, email: sachin@gmail.com, bid_price: 15 Lakh}, {name: Mohan, age: 40, email: mohan@gmail.com, bid_price: 20 Lakh}, {name: Vikram, age: 30, email: vikram@gmail.com, bid_price: 22 Lakh}])
```

- list all collections in sports database.

```
show collections
```

- rename `TT` collection to `tennis`.

```
db.TT.renameCollection('tennis')
```

- create a capped collection called `khokho` which should have max 3 documents.

```
db.createCollection('khokho', {capped: true, size: 1024, max: 3})
```

Try inserting more than 3 and see what happens?

```
db.khokho.insertMany([{"name": "Salman","age": 50,"email": "salman@gmail.com","bid_price": "15 Lakh"}, {"name": "Amir","age": 40,"email": "amir@gmail.com","bid_price": "17 Lakh"}, {"name": "Ranbir","age": 30,"email": "ranbir@gmail.com","bid_price": "18 Lakh"}])

db.khokho.insert({"name": "Sachin","age": 50,"email": "sachin@gmail.com","bid_price": "20 Lakh"})
```

- check whether a collection is capped or not?

```
db.cricket.isCapped()
db.football.isCapped()
db.tennis.isCapped()
db.khokho.isCapped()
```

- drop all documents from `football` collection.

```
db.football.remove({})
```

- delete cricket collection completely.

```
db.cricket.drop()
```

- delete sports database.

```
db.dropDatabase()
```

- check which database you are connected to ?
  sports
- connect to test database

```
use test
```

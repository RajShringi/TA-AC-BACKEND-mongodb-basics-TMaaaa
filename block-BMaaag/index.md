writeCode

Write code to:-

- create a database named `mountains`

```
use mountains
```

- a collection inside that database named `himalayas`

```
db.createCollection('himalayas')
```

- insert 1 document into that collection `{name: 'Dhauldhar range', height: '4000 mtrs'}`

```
db.himalayas.insert({name: 'Dhauldhar range', height: '4000 mtrs'})
```

- insert multiple document using insertMany command

```
db.himalayas.insertMany([
  { name: "Entry 1", height: "5000 mtrs" },
  { name: "Entry2", height: "6000 mtrs" },
  { name: "Entry3", height: "7000 mtrs" },
])
```

- find all documents from mountains

```
db.himalayas.find()
```

- find a single document using name

```
db.himalayas.find({name: 'Dhauldhar range'})
```

```
db.himalayas.update({name: 'Entry3'}, {$set: {height: '8000 mtrs'}})
```

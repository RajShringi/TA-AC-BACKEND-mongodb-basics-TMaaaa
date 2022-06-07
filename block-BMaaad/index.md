writeCode

Write command to

- List collections from a database.

```
show dbs
```

- create a new collection in your country database which you created recently.

```
db.createCollection('states')
```

Write code to:-

- crate a database named `weather`

```
use weather
```

- create a capped collection named `temperature` with maximum of 3 documents and try inserting more than 3 to see the result.

```
db.createCollection('temperature')
db.temperature.insert({'temp': '32C', 'city': 'Delhi'})
db.temperature.insert({'temp': '33C', 'city': 'Goa'})
db.temperature.insert({'temp': '40C', 'city': 'Kota'})
db.temperature.insert({'temp': '40C', 'city': 'Jaipur'})
```

- create a simple collection named `humidity`

```
db.createCollection('humidity')
```

- check whether `temperature` collection is capped or not ?
  no
- Delete `humidity` collection and then the entire database(weather).

```js
db.humidity.drop();
db.dropDatabase();
```

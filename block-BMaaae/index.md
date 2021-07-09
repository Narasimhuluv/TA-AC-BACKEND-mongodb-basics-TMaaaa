writeCode

Write code to:-

- create a database named `sports`.

  -> use sports

- list all databases present in local mongod server.
  -> db

- create 3 collections named `cricket`, `football`, `TT` in sports databse.

  -> db.createCollection('cricket')
  -> db.createCollection('football')
  -> db.createCollection('TT')

  

- add multiple players in those collections which should have fields like `name`, `age` and `email` and `bid_price`.

  -> db.cricket.insertMany([{name : "vasam Narasimhulu"}, {age : 23}, {email : "narasimhuluvasam2@gmail.com"}, {bidPrice : 3000000}]);
  -> db.football.insertMany([{name : "vasamNarasimhulu"}, {age : 23}, {email : "narasimhuluvasam2@gmail.com"}, {bidPrice : 3000000}]);
  -> db.TT.insertMany([{name : "vasam"}, {age : 23}, {email : "narasimhuluvasam@gmail.com"}, {bidPrice : 4000000}])

- list all collections in sports database.
  
  -> show dbs

- rename `TT` collection to `tennis`.

  -> db.TT.renameCollection("tennis")

- create a capped collection called `khokho` which should have max 3 documents.

  -> db.createCollection('khokho',{capped : true , size : 1024, max : 3})

  Try inserting more than 3 and see what happens?

     -> db.khokho.insertMany([{Andhrapradesh : 'Narasimhulu'}, {Kadapa : "vasam"}, {khajipet : "chinna"}])

- check whether a collection is capped or not?

  -> db.khokho.isCapped()

- drop all documents from `football` collection.

  -> db.football.drop()

- delete cricket collection completely.

  -> db.cricket.remove({})
  -> db.cricket.drop()

- delete sports database.

  -> db.dropDatabase()

- check which database you are connected to ?

  -> db

- connect to test database

  -> use test

This guide shows the frequently used command for MongoDB Shell. For full documentation, please consult [official mongoDB Shell guide](https://docs.mongodb.com/manual/mongo/).  

This guide assumes user already logged in to MongoDB Shell. If not, please consult the [installation and setup guide](README.md).

# Database

Show all databases: `show dbs`  

Show currently used databse: `db`  

Use and move to a database: `use <database>`  

# Collection

Collection in NoSQL DB is equivalent to table in RDBMS.  

Document in NoSQL DB is equivalent to row or record in RDBMS.

Show all collections: `show collections`  

Display up to 20 documents of a collection: `db.myCollection.find()` where `myCollection` is the chosen collection.  

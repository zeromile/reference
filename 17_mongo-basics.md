## 17 - Mongo basics ##

left off here: http://codepen.io/jasonleecooksey/pen/RoWdwJ

ngRoute, ng-view to control clicks and dynamically pull pages in from external files OR make already on page content hidden and then active

https://tests4geeks.com/single-page-application-using-angularjs-tutorial/


What is Mongo? 

Like other NoSQL databases, MongoDB supports dynamic schema (http://searchsqlserver.techtarget.com/definition/schema) design, allowing the documents in a collection to have different fields and structures. The database uses a document storage and data interchange format called BSON, which provides a binary (http://whatis.techtarget.com/definition/binary) representation of JSON-like (http://searchwindevelopment.techtarget.com/definition/JSON-Javascript-Object-Notation) documents. Automatic sharding (http://searchcloudcomputing.techtarget.com/definition/sharding) enables data in a collection to be distributed across multiple systems for horizontal scalability (http://searchcio.techtarget.com/definition/horizontal-scalability) as data volumes (http://searchstorage.techtarget.com/definition/volume) increase.

The name of the database was derived from the word humongous to represent the idea of supporting large amounts of data.

Is there migration files in express?



What is MongoDB?
- NoSQL
- A “record” in Mongo is a document
- MongoDB documents are similar to JSON object (BSON -> Binary JSON)
- The values of fields may contain other documents, arrays, and arrays of documents
- The advantages of using documents are:
    - Documents (i.e. objects) correspond to native data types in many programming languages.
    - Embedded documents and arrays reduce need for expensive joins.
    - Dynamic schema supports fluent polymorphism.
- In MongoDB, databases hold collections of documents

1. install mongo from website
    1. https://www.mongodb.com/download-center?jmp=nav#community   - Download
    2. Install for OSX
        1. https://docs.mongodb.com/manual/tutorial/install-mongodb-on-os-x/ - instructions
            1. Unzip file
            2. rename folder to mongodb
            3. Move to user folder
            4. Add path to mongodb/bin in .bash_profile or windows
            5. Create /data/db
            6. Set permissions ** sudo chmod 0755 /data/db && sudo chown $USER /data/db **
            7. Run 
                1. ** ls -ld /data/db/ ** to verify permissions are correct 
                2. should show: ** drwxr-xr-x  X user  wheel  XXX Date Time /data/db/ **
    3. Install for Windows
        1. https://docs.mongodb.com/manual/tutorial/install-mongodb-on-windows/
            1. follow all the instructions
            2. create \data\db folder
2. Test with ** mongod -version **
3. If that works then run ** mongod **
    1. If no error is returned then you are good to go
4. demo ** mongo ** in command line…show some database-y things
    1. https://docs.mongodb.com/manual/mongo/
    2. db - shows which database is in use
    3. use <database>
    4. show dbs
    5. show collections
    6. insert into test
    7. find()

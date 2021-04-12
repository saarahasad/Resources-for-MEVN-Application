# Resources-for-MEVN-Application

_Design and development resources to build an end to end application using MongoDB, Express, Vue.js, and Node.js_

## Basic Information on MongoDB

It is an open-source document database and leading NoSQL database. MongoDB works on the concept of collection and document.

These are some important features of MongoDB:

- Support ad hoc queries: In MongoDB, you can search by field, range query and it also supports regular expression searches.
- Indexing: You can index any field in a document.
- Replication: MongoDB supports Master Slave replication. A master can perform Reads and Writes and a Slave copies data from the master and can only be used for reads or back up (not writes)
- Duplication of data: MongoDB can run over multiple servers. The data is duplicated to keep the system up and also keep its running condition in case of hardware failure.
- Load balancing: It has an automatic load balancing configuration because of data placed in shards.
- Supports map reduce and aggregation tools.
- Uses JavaScript instead of Procedures.
- It is a schema-less database written in C++.
- Provides high performance.
- Stores files of any size easily without complicating your stack.
- Easy to administer in the case of failures.
- It also supports:
- JSON data model with dynamic schemas
- Auto-sharding for horizontal scalability
- Built in replication for high availability

###### Database: 
Database is a physical container for collections. Each database gets its own set of files on the file system. A single MongoDB server typically has multiple databases.

###### Collection: 
Collection is a group of MongoDB documents. It is the equivalent of an RDBMS table. A collection exists within a single database. Collections do not enforce a schema. Documents within a collection can have different fields. Typically, all documents in a collection are of similar or related purpose.

###### Document: 
A document is a set of key-value pairs. Documents have a dynamic schema. Dynamic schema means that documents in the same collection do not need to have the same set of fields or structure, and common fields in a collection's documents may hold different types of data.

## Design Resources

- https://www.colorzilla.com/ 
- https://www.materialpalette.com/ 
- https://flatuicolors.com/ 
- https://colorhunt.co/ 
- https://www.amazon.co.uk/gp/product/0300179359/ref=as_li_tl?ie=UTF8&camp=1634&creative=6738&creativeASIN=0300179359&linkCode=as2&tag=healthyliv0b8-21 
- https://chrome.google.com/webstore/detail/whatfont/jabopobgcpjmedljpbcaablpmlmfcogm?hl=en 
- https://www.amazon.co.uk/gp/product/1568989695/ref=as_li_tl?ie=UTF8&camp=1634&creative=6738&creativeASIN=1568989695&linkCode=as2&tag=healthyliv0b8-21 
- https://www.amazon.co.uk/gp/product/0881792063/ref=as_li_tl?ie=UTF8&camp=1634&creative=6738&creativeASIN=0881792063&linkCode=as2&tag=healthyliv0b8-21 
- https://www.amazon.co.uk/gp/product/B007F7R41Y/ref=as_li_tl?ie=UTF8&camp=1634&creative=6738&creativeASIN=B007F7R41Y&linkCode=as2&tag=healthyliv0b8-21 
- https://medium.com/product-design-ux-ui/26-digital-typography-rules-for-beginners-a04c6a5aaff3#.10tgnccvf 
- https://medium.com/thinking-design/xd-essentials-typography-in-mobile-apps-7048abfb1cc5#.tu3y5hv6z 
- https://www.canva.com/learn/distinguished-typographers-share-their-favorite-fonts/ 
- https://www.fastcompany.com/3028971/whats-the-difference-between-a-font-and-a-typeface 
- https://jgthms.com/web-design-in-4-minutes/ 
- https://dribbble.com/colors/ee6d66 
- http://platowebdesign.com/articles/translating-client-speak-infographic/ 
- https://www.amazon.co.uk/gp/product/1118766571/ref=as_li_tl?ie=UTF8&camp=1634&creative=6738&creativeASIN=1118766571&linkCode=as2&tag=healthyliv0b8-21 
- https://www.amazon.co.uk/gp/product/1592535879/ref=as_li_tl?ie=UTF8&camp=1634&creative=6738&creativeASIN=1592535879&linkCode=as2&tag=healthyliv0b8-21 
- https://uxplanet.org/golden-rules-of-user-interface-design-19282aeb06b#.kfznrp77q 
- https://teehanlax.com/story/medium/ 
- https://medium.com/@TGines/designing-user-interfaces-for-your-mother-dd45ec50f7b0#.j4bcs8rto 
- https://material.io/design 
- https://developer.apple.com/design/human-interface-guidelines/ios/visual-design/adaptivity-and-layout/ 
- https://www.mobile-patterns.com/ 
- https://pttrns.com/ 
- https://www.amazon.co.uk/gp/product/0321965515/ref=as_li_tl?ie=UTF8&camp=1634&creative=6738&creativeASIN=0321965515&linkCode=as2&tag=healthyliv0b8-21 
- https://uxmyths.com/ 
- https://www.amazon.co.uk/gp/product/0465050654/ref=as_li_tl?ie=UTF8&camp=1634&creative=6738&creativeASIN=0465050654&linkCode=as2&tag=healthyliv0b8-21 
- https://www.amazon.co.uk/gp/product/0321767535/ref=as_li_tl?ie=UTF8&camp=1634&creative=6738&creativeASIN=0321767535&linkCode=as2&tag=healthyliv0b8-21 
- https://52weeksofux.com/tagged/week_1 
- https://medium.theuxblog.com/ux-design-in-14-simple-steps-b8a0f2780769#.8a8x7xvj4 
- https://www.uxbooth.com/articles/using-dark-patterns-for-good/ 
- https://medium.com/@InVisionApp/ux-design-tips-for-your-app-8203107c77eb#.sjnw03a9t


## MongoDB GridFS vs Amazon S3 Storage

The main points to compare are:

##### Storage Size :- 
As you already might have guessed it , in Mongo db GridFs Any file would take a larger amount of size to be stored into the database . So what is the reason for the same ? Well it is because of how Mongodb GridFs works . It basically divides a file into smaller chunks with a default size of 256KB and stores it into the fs.chunks and its metafile data into fs.files collection . So each chunk would need some extra memory to store metadata along with the whole file metadata with various chunks information in fs.files. On the other hand Amazon S3 works in a different way which brings the file size difference . As a result any file stored in MongoDb GridFs would consume more memory than that of Amazon S3.



##### Cost:- 
If we assume that we will use amazon for both i.e hosting our MongoDb server on AWS and using AWS S3 then definitely AWS s3 is a clear win here. AWS EBS can cost as much as double as that of Amazon S3 and bandwidth would be of the same price . However if you are hosting on dedicated servers or somewhere else, it can be a game changer as in that case using Mongodb GridFs can be quite cheap both with respect to hosting and bandwidth cost . However that is mainly due to the fact of HIGH AWS costs compared to dedicated servers (as much as 1000 times if we compare bandwidth ), if you know how to set up and manage those . If you want we can do the same for you . If you are thinking I am doing self promotion !! Yesss I am ha ha . Now move to the next point.

##### Scalability  :- 
AWS s3 is a managed service  which is built for scalability based on under the hood scalable infrastructure. But in case of mongodb as it would be a self hosted / managed solution then we would be responsible for scaling the same as it would be in the case of normally scaling a nosql database via load balancers , proper collections arrangement and partitioning .


##### Conclusion :- 
AWS S3 is built for file storage and performs better in almost all aspects but if you are worried about High AWS bandwidth costs MongoDb GridFS on self managed servers would be a way to go.


## References for best MongoDB practices :
- https://developer.mongodb.com/article/mongodb-schema-design-best-practices/
- https://www.datavail.com/blog/mongodb-best-practices/
- https://www.mongodb.com/blog/post/performance-best-practices-mongodb-data-modeling-and-memory-sizing
- Advanced Schema Design Patterns: https://www.mongodb.com/presentations/advanced-schema-design-patterns 
- https://docs.mongodb.com/manual/applications/data-models/ 
- https://www.mongodb.com/blog/post/building-with-patterns-a-summary

## Benefits of data modeling: 

NoSQL schema design is a best practice to ensure that applications evolve, scale, and perform well. A good data model helps reduce development time, increase application quality, and lower execution risks across the enterprise.

Further reading: https://hackolade.com/nosqldb/mongodb-data-modeling.html

##  Tools to model data which are free or have a free trial period we could use:
- https://hackolade.com/document.html#mongodb
- https://dbschema.com/
- https://www.datensen.com/mongodb-design-tool.html
- https://dbmstools.com/categories/database-design-tools/mongodb

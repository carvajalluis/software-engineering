[[_TOC_]]
# Relational design Ghosts

## Separating data accessed together
separating data accessed together is most of the time an anti-pattern. MongoDB allows embedding documents to represent one-to-one relationships and to embed arrays of documents for one-to-many relationships.
### In-code symptoms: 
Accessing data separated into two collections requires the use of the 🚨🚨 **$lookup** 🚨🚨 operator. 
### Discussion: 
In some cases, separating data in several collections can be justified in order to avoid embedding huge arrays in documents or exceeding the 16MB size limit of MongoDB Document. There also exist design patterns such as the subset pattern or the extended reference pattern that combines embedding and separating data.

## Use of relational collections
For the same performance reasons as the previous smell (Separating data accessed together ), the use of the relational collection to represent many-to-many relationships is considered a bad practice in MongoDB.
### In-code symptoms: 
The use of relational collections can be detected in code by looking for a 🚨🚨 **lookup between three collections** 🚨🚨.
Discussion: Implement many-to-many relationships. Two-way embedding consists in maintaining a list of references in both collections. 

## Storage of empty values
It goes against one fundamental principle of NoSQL databases. Furthermore, storing empty or null values in documents will take unnecessary disk space.
### In-code symptoms: 
This anti-pattern is detectable in the insertion of new documents in the database. For instance, if a null value or an empty string is assigned to a field.

## Relying on transactions
The need to use transactions frequently may indicate that one of the fundamental rules of MongoDB design – data that is accessed together should be stored together – is not respected. If data accessed together are stored together, there would be no need to use transactions.

# Human oriented decisions

### Too long attribute names
Due to the use of JSON-based documents to store data in MongoDB, the name of every attribute will be stored for each document. Using long attribute names can then consume a lot of storage.
### Discussion:
Having meaningful attribute names is important for maintainability and human understanding, but it is important to find a balance between human readability and conciseness. To suggest an ideal length, researchers examined the document fields used in 250 projects using MongoDB and choose the 95th percentile as a maximal value. Consequently, we suggest that a 🚨🚨 **field name longer than 20 characters is considered too long.** 🚨🚨

## Human-readable values
They will take more space, not only in the documents but also in the indexes if those values are indexed. Larger data also induce more network consumption when retrieving it.
### In-code symptoms: 
Is not easy to detect automatically because you have to understand the meaning of the data independently from its type. Some really basic cases might be possible to discover such as string values like “yes" or “no" used to represent a boolean value or a state stored in a string format. 

## Too long document keys
In MongoDB, document keys (ids) are automatically indexed. A common example is 🚨🚨 **usage of UUIDs** 🚨🚨. They will rapidly generate large indexes files as the collection will grow. Large index files will induce performance and space consumption problems.
### In-code symptom: 
The use of long document keys can be detected by looking for UUIDs. 

# Design oversights

## Inconsistent order of attributes inside a collection
Schema flexibility does not mean that there is no need to keep a certain coherence between the documents inside of a collection. It is important to keep the document fields in the same order because MongoDB accords importance to this order when searching for embedded documents.
### In-code symptoms: 
This code smell then consists in inserting documents in the same collection but with a different field order. 
### Discussion:
After MongoDB 2.6 updates will preserve field order, with the following exceptions:
* The _id field is always the first field in the document.
* Updates that include renaming of field names may result in the reordering of fields in the document.


## Database accesses spread across the system
If a change is made to one collection in a NoSQL database, all the accesses to this collection in the system will have to be changed as well. Also, if these accesses are separated in many files, then this can complicate maintenance and impact maintainability.

### Storage of easily calculated values
Storing easily calculated values is an anti-pattern. Such data will indeed take disk space in the database while they could be easily calculated in the query or the program.
### In-code symptoms: 
With a manual code review, we could detect fields that contain easily calculated values from their name.

## Abusive use of indexes
Indexes can take a lot of disk space, especially for the collections having a large number of documents. Indexes also consume RAM as indexes are loaded in memory by the MongoDB engine. Furthermore, as indexes need to be updated by the MongoDB engine, every time the indexed field is changed, they will also consume the CPU and increase the duration of field updates. Therefore, it is important to use indexes wisely and only when necessary. 
### Discussion: 
It may depend on the number of fields in the documents or on the size of the collection. The maximum number of indexes that one can create in MongoDB is 64. However,  we will stick to no more than 10 indexes per collection.

# references

1. [Bern2021a.pdf](/.attachments/Bern2021a-34723830-ab7f-43b9-b950-ab29dae35058.pdf)
1. https://docs.mongodb.com/upcoming/release-notes/2.6/#insert-and-update-improvements



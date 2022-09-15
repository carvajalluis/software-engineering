| bucket pattern | comparison and limit | Skip & Limit |
| ------------------------------------------------------------ | --------------------------------------------------- | ------------------------------------------- |
|<code>db.history.find({ "_id": /^7000000_/ }).sort({ _id: 1 }).limit(1)</code>|<code>db.history.find({ customerId: 7000000, date: { $gt: ISODate("2018-07-21T12:01:35")}).sort({ date: 1 }).limit(1000)</code>|<code>db.history.find({ customerId: 7000000 }).sort({ date: 1 }).skip(0).limit(1000)</code>|
| fixed page size                                              | dynamic page size                                   | dynamic page size                           |
| fastest                                                      | pretty fast                                         | slowest                                     |
| easy to program                                              | hardest to program                                  | easiest to program                          |
| data storage for paging as main usage                        | data main purpose is not pagination                 | data main purpose is not pagination         |
| can travel to any page                                       | cant travel to specific page                        | can travel to any page                      |
| page  is based  on bucket document (page 1 means  bucket 1 ) | page  selection is based on sorting criteria and id | page  is based on page size and page number |

## References:

* https://www.mongodb.com/blog/post/paging-with-the-bucket-pattern--part-1
* https://www.mongodb.com/blog/post/paging-with-the-bucket-pattern--part-2
* https://www.mongodb.com/blog/post/building-with-patterns-the-bucket-pattern
* https://medium.com/swlh/mongodb-pagination-fast-consistent-ece2a97070f3
* https://www.codementor.io/@arpitbhayani/fast-and-efficient-pagination-in-mongodb-9095flbqr


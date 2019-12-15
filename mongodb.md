# Mongo DB Notes

## Creating a Database

mongoimport --db clicks --collection log < home/data/data/click_log.json

## Count & Search
```Python
db.log.count()
```
>retrieves total entries (log b/c that's what you named the collection from clicks db)
```Python
db.find('*somekey*').distinct() 
```
> retrieves the distinct values for whatever key you're looking for.
add .count() to that and you can retrieve the number of distinct values.

## OR Feature
Two ways: 
```Python
db.log.find({'a':{$in:[/Mozi/,/Oper/]}}) read this as "find the value of a where in the value theres something like mozi or oper" 
```
```Python
db.log.find({$or: [{'a': /Mozilla/}, {'a': /Opera/}]}, {'a': 1}).count()
```

## LIKE Features
use /*somesearchstringparam*/

## Finding the Field Type
```Python
typeof db.log.findOne({'t': {$exists: true}}).t
```

## Updating/Converting/ForEach Loop for a field
```Python
db.log.find({'t': {$exists: true}}).forEach(function(entry) {
 db.log.update({_id: entry._id}, {
             $set: {'t': new Date(entry.t * 1000)}
 })
})
```
>read this as "if there's a 't' key (in this case t is for timestamp), then do a for each loop over the collection doing a function for each entry. 
>the function is defined here like in JS, it's update the log for the given id (of t) and the entry for that id
>for setting the new date, you set the 't' key in this case to new Date(of the entry.t times 1000

## Check type
```Python
typeof db.log.findOne({'t': {$exists: true}}).t
```
## Aggregating
Aggregate like this:
```Python
db.log.aggregate (
... [
... {$group: {_id: '$u',count: {$sum : 1}} },
... {$sort: {count: -1}},
... {$limit: 1}
... ])
{ "_id" : "http://www.nsa.gov/", "count" : 478 }
```


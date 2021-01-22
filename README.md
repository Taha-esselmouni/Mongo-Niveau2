1. mongoimport -d ifdb -c films --jsonArray --file C:\Users\Youcode\Desktop\movies.json
2. db.films.find({"year":{$eq:2010}}).pretty();  
3. db.films.find({"year":{$gt:2009}}).count(); => 229
4. db.films.find({year:2008},{_id:1,cast:1,genres:1})
5. db.films.find({title:/^A/}).pretty();
6. db.films.find({cast:"Timothy Gibbs",year:2011}).pretty()
7. db.films.find({genres:"Thriller",year:2011}).pretty()
8. db.films.find({genres:"Thriller",year:2016}).sort({title:-1}).pretty()
9. db.films.insert([{title: "belg ben","year":2020}, {title:"beng testa","year":2020}]);
10. db.films.deleteMany({year:{$lt:2000}})
11. db.films.updateMany({}, {$set: {"rating": []}})
12. db.films.updateMany({_id:ObjectId("60084a39dd80d2427818b6df"),_id:ObjectId("60084a39dd80d2427818b6dd")}, {$set: {rating:[ { by: "moi", rating: 4 }, {by:"collaborateur", rating: 5} ]}})
13. db.films.updateMany({}, {$set: {"ar":""}})
14. db.films.updateMany({},{$rename:{"ar":"averageRating"}})
15.db.films.find({views:123444}).pretty()
17.db.films.insert({totalViews : [{views : [123444, 66855,78966]}]});

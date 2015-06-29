# mongodb-rest-server

## Introduction
A rest service server that use mongodb as backend storage service
Reference URL: http://adrianmejia.com/blog/2014/10/01/creating-a-restful-api-tutorial-with-nodejs-and-mongodb/

## Installation

To run this example, you need to start a mongodb with

```
$ mongod
```

Then install all the dependencies

```
$ npm install
```

## Execution

```
$ DEBUG=mongodb-rest-server:* ./bin/www
```

## Test

To test GET, simply use browser to check, for POST, you can use curl

ex:
```
$ curl -X POST http://localhost:3000 -d "name=buy+a+milk&completed=true"
```

or use some software like POSTMAN

## MongoDB simple command line tutorial

To enter the mongodb command line

```
$ mongo
```

To list all the databases

```
$ show dbs
```

Before querying collections inside the database, you need to use it

```
$ use <database>
```
To query everything inside the collection

```
$ db.<collection>.find()
```
ex: db.products.find()

To insert a document into the collection

```
$ db.<collection>.insert(<JSON>)
```
ex: db.products.insert({name: 'iphone6', price: '25000TWD'})

To remove all documents matched in the collection

```
$ db.<collection>.remove(<query>, {justOnce: <boolean>, writeConcern: <document>})
```
ex: db.products.remove({name:'iphone6'})

To drop a database

```
$ use <database>
$ db.dropDatabase()
```

To drop a collection

```
$ db.<colleciton>.drop()
```

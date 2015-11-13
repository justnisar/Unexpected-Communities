# Unexpected-Communities
A project aimed at mining unexpected communities.

In order to mine twitter, you need to have the authorized keys.

These keys can be got from http://developer.twitter.com by registering yourself as a developer.

The keys are used to mine the content of twitter through the streaming API

We use a config.py file to store the keys to mine twitter. 

These codes when combined with MongoDB and JSON format will be easy to work on. The reason being that Mongo is compatible with JSON format

The keys which are recieved from twitter needs to be input here for the program to work.

1) Run the code code_to_download_tweets.py -q "query" -d data to download the tweets. You can use a '>' operator to save to JSON format

2) Export the JSON file to MongoDB by using the mongo import tool. Example : mongoimport --db database_name --collection collection_name --file file.json 
This command will import the JSON file as a database collection(table in RDS)

3) These collections can be used in any python code by just importing the collections.
	from pymongo import MongoClient
	client = MongoClient() // a reference of MongoDB
	db = client.test // connecting to a database




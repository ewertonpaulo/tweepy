# tweepy
## Environment:
```
$ pip install -r requirements.txt
```
## How to use:
Create a file named auth.py with your own twitter api and postgresSql keys. You also have to add a boolean variable named sentiment_boolean who will define if the script will filter from saving the neutral tweets or not.
### auth.py
```py
# Authentications
consumer_key = 'your consumer key here'
consumer_secret = 'your consumer secret here'
access_token = 'your access token here'
access_token_secret = 'your access token secret here'

# DataBase connection keys
dbname='your database name here'
user='your user here'
host='your host here' #by default postgres uses 'localhost'
password='your password here'
port='your port here' #by default postgres uses '5432'

#Define the value to filter or not neutral tweets
sentiment_boolean = True
```
### example.py
```py
from tweetcollector.collector import collect

collect(5)
```
The function collect will pick an adjective of a text file and start the search. As parameter of collect you put the number of minutes you expect to search. main.py is an example of script, you can run on your prompt by the following command in the directory of the application:
```
python main.py
```
A message as 'collecting tweets with key someadjective' will confirm the correct run.

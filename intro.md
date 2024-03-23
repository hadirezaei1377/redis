redis is a fast db which uses cache and ram instead on hard disk to persist data.

for example we save last 50 messages from a chat in a space, so whenever we want this set of messages no need to send a query to db and make pressure on that.

redis stores data in key value mode

define variable in redis:
set name value
set hello world : hello is the name of variable and world is its value

return variable
get variable
get hello
>>> world

we can use redis as a primary db but normally we use it as a middle db for sending or recieving data quickly.

redis is not a db but we can have back up from data when we want periodic, for example every 20 seconds store data in hard drive
we can set it 1 second and use redis as a db.


string is the simplest data type in redis
in redis.io website/commands/strings we can see commands related to this data type
the most important of those are get and set

based on redis standard:
set user:1:Sam
set user:2:Ayda
set user:3:Nilda

get user:3:name 
>>>> Nilda

mget and mset:

normal conditions:
post:1:title               -----> 10 ms
post:1:content             -----> 15 ms
post:1:author              -----> 20 ms

post:2:title               -----> 30 ms
post:2:content             -----> 40 ms
post:2:author              -----> 50 ms

mget post:1:title post:1:content post:1:author          -----> 10 ms    

set page:10:title "welcome!"
set page:10:content "<html> .. </html>"
set page:10:views 10

for sorting we can use hash by hset
hash command:
hset page:20 title "welcome!" content "<html> .. </html>"

SADD meat kebab pizza burger 
SADD veg salad corn 
SADD iranian kebab fesenjoon

SINTER meat iranian 
>>> kebab

SADD fastfood pizza burger
SADD healthy salad
SINTER iranian healthy 
>>>"empty"
SINTER fastfood meat 
>>> pizza
>>> burger

SUNION fastfood iranian
>>> pizza 
>>> burger
>>> kebab 
>>> fesenjoon

after opening redis cli:
set x 10
get x
output:10

set x 10
set y 12
keys *          // command for recieving stored variables
output: x and y

timed value,EX : expiration, for example 
set sms_code 13456 EX 20
keys * 
output: x and y and sms_code
after 20 second
output: x and y

set sms_code 13456 EX 20
ttl command
output: sms_code 15    // 15 seconds is reminded

ttl command
int -2
-2 shows us the varabile is expired

ttl command for x or y
output: -1
-1 means this variable has no expiration time and it is infinite

PX is about milisecond
PX 1000 = EX 1

del x  is used for deleation variables
1 means deleation is done

set also use for updating
set x 15
set x 17
get x
output: 17

its better to use this commands for updating
set x 200 NX ... create varibale if it not exists
set x 300 XX ... Update variable

set new_variable Hadi XX
output: nill        // becuase its not exists

exists // variable existaion
exists x
output: 1 // x exists
exists y  // y exists
output: 1 
exists z
output: 0 // z not exists
exists x y
output: 2 // x and y are exist
exists x y z 
output: 2 // just x and y are exist, two of three

type x
int

set name Hadi
append name _Rezaei
get name
output: Hadi_Rezaei
strlen name
11 variable length

set age 15
increse age
output: 16
increse age
output: 17
incrby age 10
output: 27

// also decrese and decrby

m = multiple
mget name age 
Hadi_Rezaei
27

mset name Ali age 31
keys *
output:
Ali 
31

hash is key-value array ... for example  {"name:Ali", "age:45"}

HSET is used for array definition
HSET person name Ali age 27
HGET 

h = hash

hlen person 
2    ---> name and age

L = from left
from left push data to our array
LPush score 10 15 16 20 19.5
5

print values in array by Lrange
lrange score 0 -1    from zero(0) to last(-1)










# phpbb-acm-redis
phpbb cache module in redis master-slave

litlle hack...


add second redis_ro instance for read only request

Example:

Site has two web servers - web1 and web2.


install on web1 redis, set is master
install on web2 redis, set is slave

apache on web1 send write request to redis on web1, read resquest to redis on localhost (redis-master on web1)

apache on web2 send write request to redis on web1, read resquest to redis on localhost (redis-slave on web2)


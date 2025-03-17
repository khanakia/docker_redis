
## Setup
```sh
docker compose up -d
```

## Verify the redis setup
If not password is setup then this comment you can use to test otherwise use the next comnad
```sh
sudo docker exec -it redis-stack redis-cli info |  grep maxmemory
```


## Test Connection with pass
if wrong password you will see the following error `AUTH failed: WRONGPASS invalid username-password pair or user is disabled.`
```
redis-cli -u redis://default:PASS@127.0.0.1:6380
```


## For Redis Insight Installation
https://redis.io/learn/howtos/quick-start
```
docker run -d --name redis-stack -p 6379:6379 -p 8001:8001 redis/redis-stack:latest
```
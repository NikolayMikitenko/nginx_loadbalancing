# Balancing and delivery by GeoIP in Nginx
## Goal
Set up load balancer on nginx with balancing and deleivery by GeoIP to one UK, two US and one server for rest countries. In case of failure send all traffic to backup server. Healtch check happen every 5 seconds.
 
## Run project
Change docker-compose file name for testing different balancing and delivery
```
docker-compose -f "docker-compose-US.yml" up
```
 
## Test balancing and delivery
Call application
```
curl balancer
curl localhost
```
 
And see results.
For US:
```
<!DOCTYPE html>
<html>
<body>
<h1>US</h1>
</body>
```
 
For other:
```
<!DOCTYPE html>
<html>
<body>
<h1>rest</h1>
</body>
```
 
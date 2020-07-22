# Eureka REST Operaions
- https://github.com/Netflix/eureka/wiki/Eureka-REST-operations
```
Take instance out of service
PUT /eureka/v2/apps/appID/instanceID/status?value=OUT_OF_SERVICE

Move instance back into service (remove override)	
DELETE /eureka/v2/apps/appID/instanceID/status?value=UP 
```

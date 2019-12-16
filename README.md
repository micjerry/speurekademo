验证Spring Service Discovery的方案

eureka-server-demo作为服务注册中心;

eureka-client-demo去注册服务，并同时提供一个查询rest接口，可以查询自己的服务注册状态
   
   
验证：
   
    (1) 执行eureka-server-demo
   
    (2) 执行eureka-client-demo
   
    (3) 执行curl http://localhost:8080/service-instances/eureka-client-demo
        [root@5gtest ~]# curl http://localhost:8080/service-instances/eureka-client-demo
[{"instanceId":"iZwz9baq8tdsfbfbaatpt0Z:eureka-client-demo:8080","metadata":{"management.port":"8080"},"secure":false,"uri":"http://172.18.16.219:8080","instanceInfo":{"instanceId":"iZwz9baq8tdsfbfbaatpt0Z:eureka-client-demo:8080","app":"EUREKA-CLIENT-DEMO","appGroupName":null,"ipAddr":"172.18.16.219","sid":"na","homePageUrl":"http://172.18.16.219:8080/","statusPageUrl":"http://172.18.16.219:8080/actuator/info","healthCheckUrl":"http://172.18.16.219:8080/actuator/health","secureHealthCheckUrl":null,"vipAddress":"eureka-client-demo","secureVipAddress":"eureka-client-demo","countryId":1,"dataCenterInfo":{"@class":"com.netflix.appinfo.InstanceInfo$DefaultDataCenterInfo","name":"MyOwn"},"hostName":"172.18.16.219","status":"UP","overriddenStatus":"UNKNOWN","leaseInfo":{"renewalIntervalInSecs":30,"durationInSecs":90,"registrationTimestamp":1576489013254,"lastRenewalTimestamp":1576489013254,"evictionTimestamp":0,"serviceUpTimestamp":1576489012742},"isCoordinatingDiscoveryServer":false,"metadata":{"management.port":"8080"},"lastUpdatedTimestamp":1576489013254,"lastDirtyTimestamp":1576489012673,"actionType":"ADDED","asgName":null},"serviceId":"EUREKA-CLIENT-DEMO","host":"172.18.16.219","port":8080,"scheme":null}]
   
 

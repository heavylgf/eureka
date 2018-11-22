Eureka 项目结构说明
=====
（1）eureka-client：这个就是指的eureka的客户端，注册到eureka上面去的一个服务，
     就是一个eureka client，无论是你要注册，还是要发现别的服务，无论是服务提供者
     还是服务消费者，都是一个eureka客户端。
（2）eureka-core：这个就是指的eureka的服务端，其实就是eureka的注册中心。
（3）eureka-resources：这个是基于jsp开发的eureka控制台，web页面，上面你可以看到各种注册服务。
（4）eureka-server：这是把eureka-client、eureka-core、eureka-resources打包成了一个war包，
    也就是说eureka-server自己本身也是一个eureka-client，同时也是注册中心，同时也提供eureka
    控制台。真正的使用的注册中心。
（5）eureka-examples：eureka使用的例子
（6）eureka-test-utils：eureka的单元测试工具类

Eureka
=====
[![Build Status](https://travis-ci.org/Netflix/eureka.svg?branch=master)](https://travis-ci.org/Netflix/eureka)

Eureka is a REST (Representational State Transfer) based service that is primarily used in the AWS cloud for locating services for the purpose of load balancing and failover of middle-tier servers.

At Netflix, Eureka is used for the following purposes apart from playing a critical part in mid-tier load balancing.

* For aiding Netflix Asgard - an open source service which makes cloud deployments easier, in  
    + Fast rollback of versions in case of problems avoiding the re-launch of 100's of instances which 
      could take a long time.
    + In rolling pushes, for avoiding propagation of a new version to all instances in case of problems.

* For our cassandra deployments to take instances out of traffic for maintenance.

* For our memcached caching services to identify the list of nodes in the ring.

* For carrying other additional application specific metadata about services for various other reasons.


Building
----------
The build requires java8 because of some required libraries that are java8 (servo), but the source and target compatibility are still set to 1.7.


Support
----------
[Eureka Google Group](https://groups.google.com/forum/?fromgroups#!forum/eureka_netflix)


Documentation
--------------
Please see [wiki](https://github.com/Netflix/eureka/wiki) for detailed documentation.

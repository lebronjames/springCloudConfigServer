SpringCloud分布式配置中心springCloudConfigServer
1) pom.xml增加Config Server(spring-cloud-config-server)/Eureka(spring-cloud-starter-eureka)的依赖
2) 在程序主类，并添加@EnableConfigServer注解，开启Config Server
@EnableDiscoveryClient注解，用来将config-server注册到服务注册中心上去
3) application.properties中配置服务信息以及git信息
spring.application.name=config-server
server.port=7001
# 配置服务注册中心
eureka.client.serviceUrl.defaultZone=http://localhost:1111/eureka/
# git管理配置
spring.cloud.config.server.git.uri=https://gitee.com/lebronjames_kobe
spring.cloud.config.server.git.searchPaths=config-server
spring.cloud.config.server.git.username=3162310162@qq.com
spring.cloud.config.server.git.password=zhipaiwu


访问地址：http://10.5.2.241:7001/
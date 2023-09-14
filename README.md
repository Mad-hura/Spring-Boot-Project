# Spring-Boot-Project
1.Run Eureka Server

2.On Zookeeper
zookeeper-server-start.bat ../../config/zookeeper.properties

3.On kafka
kafka-server-start.bat ../../config/server.properties

4.Run Course service and student client

5.Create and run topic

kafka-topics.bat --bootstrap-server localhost:9092 --create --topic courseTopic --partitions 1

If topic already exists then -

kafka-console-consumer.bat --bootstrap-server localhost:9092  --topic courseTopic --from-beginning

6.Postman
->POST---localhost:8081/student

{

    "studentName":"nami",
    
    "course":
    
    {
        "courseName":"Jquery",
        
        "category":"Library",
        
        "price":800
    }

}

--->GET----localhost:8081/student

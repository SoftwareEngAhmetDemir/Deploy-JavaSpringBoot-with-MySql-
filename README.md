# Deploy-JavaSpringBoot-with-MySql-



#download maven 	apache-maven-3.6.3-bin.zip from this url : https://maven.apache.org/download.cgi

After That :
  1) open console in the root folder and write : mvn install 
  2) add app.yaml in the root file 
  3) write these instructions inside the app.yaml :
 runtime: java
env: flex
runtime_config:
  jdk: openjdk8
handlers:
- url: /.*
  script: auto
  http_headers:
   Access-Control-Allow-Origin: /*
  
 4) application.propereties 
        server.port=${port:8081}			  
spring.datasource.url=jdbc:mysql://ip for sql /db name
spring.datasource.username= username
spring.datasource.password=password
spring.jpa.hibernate.ddl-auto=update

5)open console in the root folder and write : gcloud app deploy target/jar file.jar

6) in google cloud  choice and create instance  after that select connections in Authorised networks add 0.0.0.0/0 and save it 

##################################################################################################
                  

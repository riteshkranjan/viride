# Getting Started (env setup)   
1. checkout code   
2. run mvn clean install   
3. Go to target folder and test with java -jar <appname>.jar   
4. open http://localhost:8080 to access this app
5. Make sure couchbase server is up and running: as mentioned in src/main/resources/applicaiton.properties file   
6. Couchbase must have a bucket as mentioned in above properties file as well as a user by same name and password mentioned in properties file   

# deploy in docker   
1. make sure docker cli is installed   
2. run mvn install dockerfile:build -DskipTests   
OR   
2. docker build -t gcr.io/hackathoncouchbase/viride-acme-app .      
3. docker images    
4. docker tag 5196f78b68ec gcr.io/hackathoncouchbase/viride-acme-app    
5. docker push gcr.io/hackathoncouchbase/viride-acme-app     



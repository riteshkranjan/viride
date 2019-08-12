# Getting Started (env setup)   
1. checkout code   
2. run mvn clean install   
3. Go to target folder and test with `java -jar <appname>.jar`      
4. open `http://localhost:8080` to access this app
5. Make sure couchbase server is up and running: as mentioned in `src/main/resources/applicaiton.properties` file   
6. Couchbase must have a bucket as mentioned in above properties file as well as a user by same name and password mentioned in properties file   

# Create docker   
1. make sure docker cli is installed   
2. run `mvn install dockerfile:build -DskipTests`     
OR   
2. docker build -t gcr.io/hackathoncouchbase/viride-acme-app .         
3. run `docker images` and note down image id    
4. tag image id `docker tag <imageId> gcr.io/hackathoncouchbase/viride-acme-app`       
5. finally push this image `docker push gcr.io/hackathoncouchbase/viride-acme-app`     

# Gcloud setup 
after installaiton of google cloud sdk run below commands
1. gcloud auth login    
2. gcloud config set project hackathoncouchbase    
3. gcloud container clusters list    
4. gcloud container clusters get-credentials viride-cluster-1 --zone us-central1-a   
5. kubectl get pods   



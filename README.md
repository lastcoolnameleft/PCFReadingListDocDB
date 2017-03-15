## Local
Following are the instructions to run the app locally against a local MongoDB instance and against Azure DocumentDB for MongoDB protocol instance.
1. Install Java and Maven
2. Install and start MongoDB
3. Clone the repository
4. Make the project base as the current directory 
5. Run the application by executing the follwoing command from the project base directory
      >  mvn package && java  -jar target/PCFReadingListDocDB-0.0.1.jar 
6. Access the appliction from the following URL:
      > http://localhost:7070    
7. Create a DocumentDB account for MongoDB protocol
     > Detailed instructions can be found [HERE](https://docs.microsoft.com/en-us/azure/documentdb/documentdb-create-account).
8. Retrieve and update the connection string for DocumentDB
     > Detailed instructions can be found [HERE](https://docs.microsoft.com/en-us/azure/documentdb/documentdb-connect-mongodb-account).
9. The updated connection string will look like the following 
      > mongodb://<USERNAME>:<PASSWORD>@<HOST>:<PORT>/<DATABASE>?ssl=true
10. From the project base directory run the following command:
      > mvn package && java -Dspring.data.mongodb.uri= mongodb://<USERNAME>:<PASSWORD>@<HOST>:<PORT>/<DATABASE>?ssl=true -jar target/PCFReadingListDocDB-0.0.1.jar
11. Access the appliction from the following URL:
      > http://localhost:7070 

## Local Docker
## Pivotal Cloud Foundry 

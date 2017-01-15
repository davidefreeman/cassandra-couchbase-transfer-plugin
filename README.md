# cassandra-couchbase-transfer-plugin

This tool allows you to transfer data from Cassandra to Couchbase , just by doing some small configurations :) 
##Configurations:

All the configurations can be done by setting the **environment variables**
###Couchbase Configuration:


|   Configuration Name  |   Default Value   |   Description |
| :---------------------: | :-----------------: | :--------------: |
|   COUCHBASE_URL       |   "localhost"     | The URL for the Couchbase.|
|   COUCHBASE_BUCKETNAME|   "foobar"        | The bucket name to which data needs to be transferred.|

### Cassandra Configuration:

| Configuration Name | Default Value | Description |
| :-----------------: | :------------: | :----------: |
| CASSANDRA_URL | "localhost" | The URL for the Cassandra. |
| CASSANDRA_PORT | 9042 | The port for the Cassandra. |
| CASSANDRA_KEYSPACENAME | "foobar" | The keyspace name for the Cassandra |
| CASSANDRA_TABLENAME | "testcouchbase" | The table name that needs to be transferred. |
| CASSANDRA_ID_FEILD_NAME | "id" | The field name that should be used as Couchbase Document Id, if the field name does not matches any column it gives a random id to the document. |


##Code in Action:

###Cassandra Side:
So this is how data looks on Cassandra Side:


###Couchbase Side:

**Case 1:** When id exists and same can be used as Couchbase Document Id.


**Case 2:** When id name does not exist and we need to assign Random id to Documents.



##How to Run the Cassandra-Couchbase Transfer plugin:

Steps to run the code are :

1. Download the code from the repository.
2. Configure the environment Variables according to the configuration.
3. Run the project using sbt run
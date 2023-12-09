# the_PINPIP_project
the Pininterest Data Pipeline project (no 3)
# Abstract
The purpose of this project is to build two types of data engineering pipelines, for processing *batch* and *streaming* data from the Pinterest social media service. Distributed computing services (AWS Cloud) are employed, and the processed data sets are eventually stored in predisposed cloud S3 buckets. Heere below an outline of the basic components of the ETL pipelines:

*Batch data*
    a. Amazon API Gateway
    b. Virtual Private Cloud: EC2 Instance
        1. Confluent-kafka-connect-s3
        2. Confluent kafka REST proxy
        3. Kafka consumer
    c. Amazon S3
    d. Databricks lakehouse?

*Streaming data
    a. Amazon API Gateway
    b. Virtual Private Cloud: Amazon Kinesis
    c. Databricks Delta
    d. Databricks lakehouse?

# A glimpse into the data to crunch
Data sets are stored as json files, each readable with json_load(<string that point to name>) into a python dictionary. There are three types of data sets as follows:

1. pinterest_data
	*post* {'index': 7528,'unique_id': 'fe34b356 xxxx' , 'title': 'No title', (description,poster_name,follower_count, tag_list,is_image_or_video,image_src,downloaded,save_location,category)}
	
2. geolocation_data
    *geo* {'ind': 7528, 'timestamp': xxx ,'latitude': ,'longitude': , 'country': }
    
3. user_data
    *user* {'ind': 7528, 'first_name':'Abigail', 'last_name':'Ali','age':'25','date_joined: cxxc}
    
There are 12 keys in *post*, and ID is an index; 5 keys in *geo*, ID is akin to ind (index); 5 keys in *usr*, ID is too aking to ind (index).
The primary keys are index/ind, which seem the same just but with different name.


# Table of Content

# Description of the project

# Licence Information

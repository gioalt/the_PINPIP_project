# the_PINPIP_project

the Pininterest Data Pipeline project (no 3)

# Abstract

The purpose of this project is to build two types of data engineering pipelines, for processing *batch* and *streaming* data from the Pinterest social media service. Distributed computing services (AWS Cloud) are employed, and the processed data sets are eventually stored in predisposed cloud S3 buckets. 

Here below an outline of the basic components of the ETL pipelines:

*Batch data*  
1. Amazon API Gateway  
2. Virtual Private Cloud: EC2 Instance  
        2a. Confluent-kafka-connect-s3  
        2b. Confluent kafka REST proxy  
        2c. Kafka consumer  
3. Amazon S3  
4. Databricks Notebook 

*Streaming data*  
1. Amazon API Gateway  
2. Virtual Private Cloud: Amazon Kinesis  
3. Databricks Delta Lake 

Here below a glimpse of the data sets:

They are stored as json files, each readable with json_load(<string that point to name>) into a python dictionary. There are three types of data sets as follows:

1. pinterest_data
	*post* {'index': 7528,'unique_id': 'fe34b356 xxxx' , 'title': 'No title', (description,poster_name,follower_count, tag_list,is_image_or_video,image_src,downloaded,save_location,category)}
	
2. geolocation_data
    *geo* {'ind': 7528, 'timestamp': xxx ,'latitude': ,'longitude': , 'country': }
    
3. user_data
    *user* {'ind': 7528, 'first_name':'Abigail', 'last_name':'Ali','age':'25','date_joined: cxxc}
    
In summary, there are 12 key-value pairs in *post*; 5 key-value in *geo*; 5 key-value in *usr*. Their *primary keys* are index/ind, which seem the same variable but with different name.


# Table of Content

# Description of the project

# Usage Instructions

# Licence Information

This program suite is not covered by licence. It was built in partial fullfilment of the requirements for the AICore Data Engineering certification.

**What is CIDR IP range?**
* Classless Inter-Domain Routing (CIDR) is a range of IP addresses a network uses

**AWS Config**
* Execute rules on your resources for complaince monitoring.
* Provides a time series graph to show the changes and relationships over a period of time.
* You can only delete the rules from CLI only.
* Command is ```aws configservice delete-configuration-recorder --configuration-recorder-name default```


**OpsWorks -** 

* AWS OpsWorks Chef Automate
* Puppet Entrprise
* OpsWorks Stacks - AWS
    * manages applications on both AWS and on Prem
    * Design layers that perform different functions
    * Autoscaling and scheduled scaling
    * Implements Chef Solo


**AWS Inspector:** 
* To perform security checks on compute cloud, mostly on EC2.

**Secrets Manager:**
* Stores secrets, encrypted, securely.
* Rotation is possible
* API alls over https can be made to retrieve secrets
* SM reads the secret, decrypts it and returns to the caller over https
* Supports RDS DB, RedShift Clusters, other DBs and Document DB & any other types of passwords
* Default encryption key is free of charge, Custom encryption key is charged.
* A lambda function can be triggered when a secret is expiring to automate the rest of the proess. 
* For RDS, Redshift and DynamoDB the lambda function is provided by the AWS.

**Systems Manager Parameter Store:**
* Parameter Store stores key values pairs like plain text, encrypted text 
* Other services can read these parameters instead of hardcodign them in the code
* A good example is cloud formation templates can read these values in the templates.
* Supports String, String List and Secure String
* CF templates: 
    * ```AWS::SSM::Parameter::Name```
    * ```AWS::SSM::Parameter::Value<String>``` 
    * ```AWS::SSM::Parameter::Value<List<String>>``` 
    * ```AWS::SSM::Parameter::Value<Any AWS type>```



**EC2 User-Data/Meta-data**
* http://169.254.169.254/latest/meta-daa
* http://169.254.169.254/latest/user-data

**Auto Scaling:**
* Auto Scaling Group are configured using launch configurations.
* Launch Configurations uses Launch Templates
* Auto scaling can spread across multiple AZs.
* Scheduled Scaling 
* Dynamic Scaling
        * Simple Scaling  - Based on Metrics
        * Stepped Scaling
        * Target Tracking - 
* Cooling period helps to prevent rapid provisioning.
* Replaced failed instances
* Auto Scalaing groups can be configured with ELB
* Auto Scaling group can be configured with Target Groups





     
**Helm With EKS(AWS)**
* https://www.traveldiaries4u.com/authorsCollections/fullCollections/softwareCollections/awsCodeCommitHelmDeploy?fbclid=IwAR12Mi9BdVYtJ6O3lmsIAP-mulBnzky33zMKBlEmSujx9kW--zH3eW0Q5O0

**Kafka by Confluent**
* https://www.confluent.io/online-talks/microservices-and-apache-kafka/?utm_medium=paidsocial&utm_source=linkedin&utm_campaign=ch.paidsocial_tp.prs_tgt.past-arc-titles_rgn.namer_lgn.eng_con.microservices-3pt-series-webinar-on-demand&creative=mak-icd


# AWS Certified Cloud Practitioner training 

- what is cloud computing ?

- Benefits of cloud computing 

- Types of cloud computing

- cloud computing Deployment model 

- set budget and budget alert 

- set up Billing Alarm

-  IAM  (change IAM users sign-in link)
-  Activate MFA (multi factor Authentication ) on Root Access 

-  create individual IAM User 
      - create user as Admin


- Regions 
 - every region has availability zone  

- create AWS EC2 instance give it a IAM role

- Session manager
   - how to get accesses to the instance 
   - session manager ( how to get access to EC2)

- create Amazing Machine Image (AMI)
   - we create  AMI  from instance that u have it look like a snapshot for ur entire server 
   - the server/ instance must not be created 
   - when u launch a AMI it forward u to the steps to create instance from that 

-Aut0 scaling Groups
  -  autoscaling group deleting delete instance too with it 

- Elastic Load balancer (ELB)
   - we wil set that  load balancer in front of your instances when traffic flow to ur load balancer 
     it will be distributed against the servers 
   -    we have three types of load balancer  (application loadbalancer (http , https) , Network load balancer and  cluster load
        balancer )
   - define security group ,  protocol version    , target type   
   - more info >> https://data-flair.training/blogs/aws-elb/
   - we need ur load balance to be run into Two availability Zone
   - configure security (HTTP or HTTPS) and configure ur Routes
   - we need to take the DNS name for ur load balancer and click on listener  to define the target http protocol and the port
   
- Sample Storage Services (S3)
    - s3 doesn't require ur region Selection
    - Create a bucket just to contain ur files 

- CloudFront
 
 - it is used as a CDN (Content Delivery Distribution)
 - copy your files to multiple edge location a round the world and served from nearby edge location
 - origin Domain name will be ur S3 bucket url 

- Relational Database Service (RDS)

  - u have many engines types that u can select from (Amazon Aurora , Mysql , Maria Db , PostgreSQL ,Oracle , M Sql server)
  - for free (750 hr on rds )
  - u have Storage auto scaling 
  - define backup retention period 
  - u have ur endpoint port and database name password  that u need to connect to ur db
  -

- Lambda

 -  define runtime (Ruby , Go ,java ,python ,.net core 2.1) 
 -  if u create lambda function with new roles it will write it's log to cloudwatch 
 -  u will have a nice editor 
 -  u can test ur code
 -  cloud watch give u indication about invocation , Duration  Error Count throtties and others on chart 
 -  lambda can be trigger from different services  So u can add many many trigger from any event on some services
 -  and it has an integration with some third party engine


_____________________________________________________

-EC2 pricing Model 

   - on-demand 
   - reserved-instance
   - spot instances 
   - Dedicated host  


- free services and they are free
   - IAM , Auto-scaling 
   - CloudFormation  it is free but it may provision other service which could cost u a mony 
 

- AWS Support plans

- Basic  ,developer , business and enterprise

 - cerate a support case 

 -AWS marketplace u  aws.amazon.com/marketplace 
    u have market place were u keep all all things u get from market place 

- AWS trusted Advisor 
  
    - advise u for security ,performance , billing , Service limit and fault tolerance 
    - u have only 7 free trusted advisor checks
    - it a list for best practice on AWS 
    
- consolidate Billing     

 - one bill for all your account 
 - u have master account and other accounts 
 - that for organization that own many accounts
 - u can use Cost Explorer  

 - the Consolidated Billing account -volume discount (1:58:20)
   - the more u use the more u save (see image)
   
 -AWS Cost Exploerer 
   -  see  ur spending 
   -  u can find useful information about costs 
   -  Daily unbended costs
   -  u can filter by services how does it cost
   -  u can get many reports  about costs and usage  

- AWS Budget 
  - help u  plan service usage  services costs and instance reservation 
  - u think about it as a build alarm 

-TCO calculator
   - total cost ownership
   - it is a approximation tool only 

-AWS Landing Zone
  -  Helping u setup multi account , it provide u the baseline environment for that .
  -  It is good for enterprise that has different accounts .
  -  Automatically provision and configure new accounts via 'Service Dialog template ' Uses
     Single Sign On (SSO) for managing and access the account . 
  -


- AWS Resources group and tags
  -  they are strongly related
  -  Tags acts a metadata  and resource group are collection of resources that share same one or more tags
  -  let's say you had a database a server and maybe an s3 bucket and you wanted to group them all together you'd give them
     all the same tag and then you could put them in a resource group and so that .
  

- AWS QuickStart

  - that is prebuilt template by AWS and AWS partner help u deploy popular stack reduce many manual procedures into just few steps

  - it is composed of 3 parts 
     -  A reference architecture for the deployment
          ( so it's gonna be like an architectural diagram and description  ) 
     -  AWS CloudFormation that automate and configure the Deployment
          (are used for provisioning multiple AWS's resources so it's gonna automate that deployment for you)
          ( u can use a  cloudformation to create or update an existing template and template it self 
           could be a Json/YAML file that describe ur stack's resources and the properties ) 
     -  the Deployment guide explaining the architecture and implementation in detail      
    
 - AWS costs and usage
  -  generate a detailed Spreadsheet , enabling you to better analyze and understand your AWS costs 
  -  that can be placed to [S3]
  -  Use [Athena] to turn the report to queryable database 
  -  use [QuickSight] to visualize your billing Data
 

 _________________________Technology Overview

 - AWS organization and Accounts
   - u can promoted your account to organization amd underneath u can create multiple account 
   -  apply service policy to an service
     (if u are giving policy to Ec2 only and u trying to  create an lambada function u will prevented as ur account under 
       organization unit  )
   -  we aren't delete accounts we just suspend them  that is happened to AWS related to credit card and billing 
  

- AWS Networking  
   - region , AZ , internet gateway , Route Table , NACLs ,Security Groups and Subnets 


- Database Services  

 - Dynamic DB - nosql key/value database (cassandra)
    - very flat and sample and have million record and guarantee read and write  
 - DocumentDB NoSQL Document database that is MongoDb compatible 
 - RDS Relational database that support multiple engines (mysql , postgress ,mara db , oracle ,MSSQL ,Aurora)
     - Aurora mysql (5x faster) and PSQL(3x faster ) database fully managed [it has high availability and durability ]
     - Aurora serverless - only runs when u need it like AWS lambda
 - Neptune Managed graph database
 - Redshift columnar database petabyte warehouse
 - Elastic cache - Redis or memcache


- Provision

  - is to set up a bunch of resources and services for u 
    - Elastic Beanstalk :- 
        service for scaling and deployment web Apps and services built with [node ,java ,.net ,php Go or even Docker]  like  
          heroku .
        u just choose ur container for .Net and u Don't care about infrastructure

      -   

# AWS Solutions Architect Associate Labs

Laboratórios práticos para preparação para a prova de certificação para AWS Solutions Architect - Associate Level do treinamento da Solvimm: https://solv.im/33DdK9L


## Index

- [Lab 01 - IAM](https://github.com/solvimm/aws-solutions-architect-associate-labs/tree/master/lab%2001%20-%20IAM)
- [Lab 02 - Billing Alarm](https://github.com/solvimm/aws-solutions-architect-associate-labs/tree/master/lab%2002%20-%20Billing%20Alarm)
- [Lab 03 - S3](https://github.com/solvimm/aws-solutions-architect-associate-labs/tree/master/lab%2003%20-%20S3)
- [Lab 04 - S3 Versioning](https://github.com/solvimm/aws-solutions-architect-associate-labs/tree/master/lab%2004%20-%20S3%20Versioning)
- [Lab 05 - S3 Cross Region Replication](https://github.com/solvimm/aws-solutions-architect-associate-labs/tree/master/lab%2005%20-%20S3%20Cross%20Region%20Replication)
- [Lab 06 - CloudFront](https://github.com/solvimm/aws-solutions-architect-associate-labs/tree/master/lab%2006%20-%20CloudFront)
- [Lab 07 - EC2](https://github.com/solvimm/aws-solutions-architect-associate-labs/tree/master/lab%2007%20-%20EC2)
- [Lab 08 - EBS](https://github.com/solvimm/aws-solutions-architect-associate-labs/tree/master/lab%2008%20-%20EBS)
- [Lab 09 - AWS Command Line (CLI)](https://github.com/solvimm/aws-solutions-architect-associate-labs/tree/master/lab%2009%20-%20AWS%20Command%20Line%20(CLI))
- [Lab 10 - EC2 Bootstraping](https://github.com/solvimm/aws-solutions-architect-associate-labs/tree/master/lab%2010%20-%20EC2%20Bootstraping)
- [Lab 11 - CloudWatch](https://github.com/solvimm/aws-solutions-architect-associate-labs/tree/master/lab%2011%20-%20CloudWatch)
- [Lab 12 - RDS](https://github.com/solvimm/aws-solutions-architect-associate-labs/tree/master/lab%2012%20-%20RDS)
- [Lab 13 - RDS com Alta Disponibilidade](https://github.com/solvimm/aws-solutions-architect-associate-labs/tree/master/lab%2013%20-%20RDS%20com%20Alta%20Disponibilidade)
- [Lab 14 - Route 53](https://github.com/solvimm/aws-solutions-architect-associate-labs/tree/master/lab%2014%20-%20Route%2053)
- [Lab 15 - Route 53 Routing Policy]()
- [Lab 16 - VPC](https://github.com/solvimm/aws-solutions-architect-associate-labs/tree/master/lab%2016%20-%20VPC)
- [Lab 17 - Load Balancer e Health Checks](https://github.com/solvimm/aws-solutions-architect-associate-labs/tree/master/lab%2017%20-%20Load%20Balancer%20e%20Health%20Checks)
- [Lab 18 - Autoscaling Groups]()


# AWS Samples
Sample codes using AWS services and serverless framework.

## Index

1. [Lambda Image Processing](#lambda-image-processing) 
2. [Translate Text from Image](#translate-text-from-image)


## Sample Applications

<a name="lambda-image-processing"/>

### Lambda Image Processing

#### About
From an uploaded image to Amazon S3, invokes AWS Lambda functions running in parallel to generate processed images such as:

- Applying watermark
- Thumbnail
- Black and White

And also has a structure to include new types of image processing in new AWS Lambda functions with configured serverless.yml

#### AWS Services Used
This sample application uses:

- Amazon S3
- Amazon SNS
- AWS Lambda

#### Architecture

![Lambda Image Processing Architecture](https://github.com/filipebarretto/aws-samples/blob/master/architecture-diagrams/lambda-image-processing-achitecture.png?raw=true)


<a name="translate-text-from-image"/>

### Translate Text from Image

#### About
From an uploaded image to Amazon S3, invokes a AWS Lambda function that uses Amazon Recognition to detect text and Amazon Translate to translate the detected text to Portuguese. After the text is processed, emails user using SNS with the translated text.


#### AWS Services Used
This sample application uses:

- Amazon S3
- Amazon SNS
- AWS Lambda
- Amazon Rekognition
- Amazon Translate

#### Architecture

![Lambda Image Processing Architecture](https://github.com/filipebarretto/aws-samples/blob/master/architecture-diagrams/translate-text-from-image-architecture.png?raw=true)
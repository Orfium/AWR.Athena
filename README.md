# AWS.Athena

This an R client to interact with the [AWS Athena](https://aws.amazon.com/athena), including wrapper functions 
around the [Athena JDBC package](http://docs.aws.amazon.com/athena/latest/ug/connect-with-jdbc.html) to 
to query data stored in S3.

## Installation

![CRAN version](http://www.r-pkg.org/badges/version-ago/AWR.KMS)

The package is not yet hosted on CRAN. 

But you can easily install the most recent development version of the R package as well:

```r
devtools::install_github('nfultz/AWR.Athena')
```

## What is it good for?



## What if I want to do other cool things with Athena and R?

Most functionality is provided via JDBC is mostly provided upstream, but if you have Athena-specific
features in mind, please open a ticket on the feature request, or even better, submit a pull request :)

## It doesn't work here!

To be able to use this package, you need to have an [AWS account](https://aws.amazon.com/free). If you do not have one already, you can register for free at Amazon and do 20K free requests per month, although usage is currently $5 / terabyte scanned.

Once you have an AWS account, make sure your default AWS Credentials are available via the [DefaultAWSCredentialsProviderChain ](http://docs.aws.amazon.com/sdk-for-java/v1/developer-guide/credentials.html). 
In short, you either provide a default credential profiles file at `~/.aws/credentials`, use the `AWS_ACCESS_KEY_ID` and `AWS_SECRET_ACCESS_KEY` environment variables or if using `AWR.Athena` on AWS, you can also rely on the EC2 instance profile credentials 
or ECS Task Role as well.
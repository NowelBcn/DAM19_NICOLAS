# Assignment: Decision making

##Quick acces to files:

The source logs and the data analyzed can be check at:

<https://docs.google.com/spreadsheets/d/1UY9qVkAuSgCIFZ272S1NWGm9c1UQ2XLmNbTE8XC9utM/edit?usp=sharing>


##Assignment description:

###Task:
* Clients complain that the searches for a destinations sometimes fail. Head of product decided to address the issue, and ask development team to work on fix.

* The team committed to work out the solution during August. It was agreed that the team’s bonus payout would depend on effectiveness of the solution.

* **The Head of Product ask you to analyze the data and help him to decide whether the team deserve the bonus?**

* Your answer should be documented and submitted to the GitHub so that any changes can be easily tracked.

###Useful context:

* Data for Barcelona destination **(18452212)** is representative **so that any conclusions can be extrapolated for other destinations.**
 
 
##Process of solving
 
### Gathering data from AWS S3


**Homebrew on Mac OS X**

Install and configure AWS CLI in the computer via Terminal using Brew.

Install AWS with the code:

```
brew install awscli

```

After installation brew will provide instructions for installing completion and where to find the examples on how to use aws-cli.


**Configuring AWS CLI**

```$ aws configureAWS Access Key ID [None]: AKIAIOSFODNN7EXAMPLEAWS Secret Access Key [None]: wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEYDefault region name [None]: eu-west-1Default output format [None]: ENTER
```

**Exploring the AWS S3 Bucket provided with the data**

Explore through the buckets with command:

```
$ aws s3 ls s3://data.public.bdatainstitute.com

```

You can use commands like:

```
--recursive |  To explore the whole Key with it's subdomains
--human-readable  |  
```
Once the key you are interested in, you can download it with:
```
--recursive |  To explore the whole Key with it's subdomains
--human-readable  |  Turns the data provided in the CLI Pretty Print.
```

In our case it goes as follow:

```
iMac-de-Hugo:~ nicolascapo$ aws s3 cp s3://data.public.bdatainstitute.com/dam/query_logs/ awsfiles.zip --recursive
download: s3://data.public.bdatainstitute.com/dam/query_logs/2018/08/2018_08_18452212_summary.json to awsfiles.zip/2018/08/2018_08_18452212_summary.json
download: s3://data.public.bdatainstitute.com/dam/query_logs/2018/09/2018_09_18452212_summary.json to awsfiles.zip/2018/09/2018_09_18452212_summary.json
download: s3://data.public.bdatainstitute.com/dam/query_logs/2018/08/2018_08_18452212_log.json to awsfiles.zip/2018/08/2018_08_18452212_log.json
download: s3://data.public.bdatainstitute.com/dam/query_logs/2018/09/2018_09_18452212_log.json to awsfiles.zip/2018/09/2018_09_18452212_log.json
iMac-de-Hugo:~ nicolascapo$ 
```
### Manipulating with JSON files

####Pre-viewing the JSON files with online viewer

 https://jsoneditoronline.org/
 
####JSON Path tester
 [I need to understand what is this used for]
 
```
JSON Path Example

$.logs[*].timestamp
```

####JSON → CSV ?

<http://www.convertcsv.com/json-to-csv.html>
 
###Documment the process with a .md report and upload it to Github
####Download and install git
Install git on your computer

<https://git-scm.com/download/>

##Conclusions of Analysis


[To be finished]






 

  




# Cymptom Python Candidate Task

## Pulling EC2 data using Python
Your goal in this assignment is to pull EC2 instances data from AWS cloud and structure it in a human-readable way.
You will receive a token in a separate mail for interacting with our testing AWS environment.
You will probably need to use [boto3 describe_instances](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ec2.html#EC2.Client.describe_instances)
method to pull the container data from our environment.

### What data to pull?
EC2 instances have a lot of metadata related to them, your task is to pull all instances in our environment.
For each instance, we want to collect all data that seems relevant for further cyber exploitation of these instances.
This can include:
* Id's
  * ImageId
  * InstanceId
  * ...
* OS / PlatformDetails
* network settings:
  * IP addresses
  * dns settings
  * subnet
  * interfaces
  * ...
* Status (stopped / running ...)
* description
* LaunchTime
* tags
* specs
  * cpu
  * ram
  * InstanceType
* Security Groups
* Tokens

and any other info you find relevant!

### Guidelines:
* Your code should be production code not POC, this means that you should consider things like how to structure your 
code in a modular way so:
  * It's clear enough so updates or changes will be simple.
  * It's stretchered in a way that parts are not dependent on each other.
  * And in general, uses the best OOP principles and design patterns.
* Use pythons [dataclasses](https://docs.python.org/3/library/dataclasses.html) to structure the returned data from your code
* Use python version 3.7+
* Use [typing](https://docs.python.org/3/library/typing.html) to make methods as clear as possible.
* Please try to keep pep8 linting guidelines.
* **Don't clone this repo!**
* AWS has different regions that each may contain EC2 instances, you should pull all instances, take that into account!
* The credentials you received might have limited access to ec2 and to AWS regions, try first pulling from “us-east-2” to make sure it works.


## Bonus

If you'll use pytest and write a basic test-suit in order to validate that your assignment is working as 
expected that will definitely give you an edge over other submissions!

## Assignment submission
You should send us back a repository containing the code you have written.
Please don't clone the repo!

**Good luck!**

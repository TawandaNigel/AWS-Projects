<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Build a Virtual Private Cloud

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-networks-vpc)

**Author:** Tawanda Nigel Chitapi  
**Email:** nigel.chitapi@gmail.com

---

## Build a Virtual Private Cloud (VPC)

![Image](http://learn.nextwork.org/heartfelt_cyan_glamorous_medlar/uploads/aws-networks-vpc_2facf927)

---

## Introducing Today's Project!

In this project, I will demonstrate how to create VPC, create Subnets and attach an Internet Gateway to my VPC.

I'm doing this project to learn to learn about AWS networking and traffic rules, and security measures to control how resources, like EC2 instances and databases, connect and work together

### What is Amazon VPC?

Amazon VPCs are isolated sections of the AWS Cloud that help to keep my AWS resources private and secure

In today's project, I used Amazon VPC to host a Public Subnet that contain my AWS Resources

### Personal reflection

This project took me 30 minutes

One thing I didn't expect in this project was the ability to automatically assign public IPV4 adresses to instances. I though i would have to manually create on for each and every instance i wish to be public.

---

## Virtual Private Clouds (VPCs)

### What I did in this step

In this step, I will create a VPC because it is important to isolate my AWS resources from being accessible to the whole of AWS. My resources need to be private and secure and live within a specific network that is unique to me or my organization only.

### How VPCs work

VPCs are isolated sections of the AWS Cloud that help to keep my AWS resources private and secure

### Why there is a default VPC in AWS accounts

There was already a default VPC in my account ever since my AWS account was created. This is because AWS has setup a default VPC to allow me to create and deploy EC2 instances or RDS databases right away without having to create my own VPC from scratch.

![Image](http://learn.nextwork.org/heartfelt_cyan_glamorous_medlar/uploads/aws-networks-vpc_2facf927)

### Defining IPv4 CIDR blocks

To set up my VPC, I had to define an IPv4 CIDR block, which is a way to assign a whole block/range of IP addresses, kind of like creating a zone/area in a city that my VPC can allocate IP addresses to the resources within my VPC.

---

## Subnets

### What I did in this step

In this step, I will create a public subnet withing my VPC because i need to seperate resources that can and need to be accessed publicly from those that need to remain private for internal access only.

### Creating and configuring subnets

Subnets are sub-sections on my VPC akin to neighborhoods in a City. There are already subnets existing in my account, one for every Availability Zone in the Region that my VPC is set up in. 

### Public vs private subnets

The difference between public and private subnets are their accessibily to the public or the internet. Resources withing a private subnet are meant to be private and for internal use and access only. Public subnets contain resources that are designed to be accessible to the public. 

For example, if you're running a web app, the public-facing website needs to be accessible from the internet - so an EC2 instance hosting the website should be launched in the public subnet.

On the other hand, the web app's database that's storing sensitive data shouldn't be directly accessible from the internet. It only needs to communicate with the EC2 instance, so it can sit in the private subnet.

For a subnet to be considered public, it has to be routed to an Internet Gateway

![Image](http://learn.nextwork.org/heartfelt_cyan_glamorous_medlar/uploads/aws-networks-vpc_157c4219)

### Auto-assigning public IPv4 addresses

Once I created my subnet, I enabled auto-assign public IPv4 addresses. This setting makes sure each EC2 intance that I launch in that particular subnet will be automatically assigned a Public IP Address so that resources being hosted by the instance can be accessed publicly. 

---

## Internet gateways

### What I did in this step

In this step, I will create an Internet Gateway and attach the Internet Gateway to my VPC because i would like to enable resources within my VPC to be able to connect to the internet.

### Setting up internet gateways

Internet gateways are a key VPC component that allows or enables internet access to the resources within my VPC. 

Attaching an internet gateway to a VPC means resources within the VPC are able to access the internet. EC2 instances with a Public IPV4 address would still not be able to connect to the internet, even though their IP Address is public.

If I missed this step, resources within the VPC would not be able to connect to the internet as well as users on the internet, they would not be able to connect to the internet. 

While I have setup an internet gateway and attached it to my VPC, I still need to setup route tables. Route Tables will help EC2 instances resources within my VPC to find their way to the internet gateway attached to my VPC.


![Image](http://learn.nextwork.org/heartfelt_cyan_glamorous_medlar/uploads/aws-networks-vpc_4ae90410)

---

## Using the AWS CLI

### What I'm doing in this extension

### Exploring CloudShell and CLI

### Debugging my setup

### Comparing CloudShell vs AWS Console

---

---

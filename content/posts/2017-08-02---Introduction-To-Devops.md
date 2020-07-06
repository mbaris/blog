---
title: Introduction to DevOps
date: "2017-08-02T00:00:00+03:00"
template: post
draft: false
slug: "introduction-to-devops"
category: "DevOps"
tags:
  - "Devops"

description: "Devops is the combination of practices, philosophies and tools that focuses on improving the delivery process of a product. It emphasizes communication between product management, development and operations teams. "

---

## Culture

In a traditional company, product team comes up with feature requests, development team implements these requests and operations team deploys and maintains the application. 
With this model:

* Teams are mostly decoupled from each other
* Deployment cycle takes a lot of time
* Responsibility is not shared since a teams job is to hand their result to the next one before a deadline

DevOps is about breaking the walls and encouraging collaboration between these teams. Definition of done now is to deliver a product to the customer and see it succeed. With unit, integration and acceptance testing, monitoring and applying continuous integration/deployment paradigms, deployment becomes less risky and faster.

## Automation

Cloud and SaaS movements raised the bar on user expectations from an application. ten years ago, operations people could manually deploy, update and maintain their product manually since there were only one or two servers, and shutting them down for a few minutes while updating was not a big deal. But now our applications are divided into multiple programs so we need to automate our deployment, provisioning and failover processes. Thankfully, with the advent of services like Amazon Web Services(AWS), Microsoft Azure, Digitalocean and Google Cloud Platform, we can provision new servers and resources for our applications in mere seconds. Then we can use configuration management tools like ansible, puppet, or chef to configure these servers. 
Automation also prevents some of the errors in deployment and creates consistency. Automating the deployment and provisioning process also helps removing differences in development, test, staging and production environments. We can use the same process with some config changes for all of environments. 

At OpsGenie, we try to do minimal updates most of the time but we provision over 40 ec2 boxes from aws for a full redeploy. Without a lot of automation, 3 updates every day wouldn't be possible. 

## Measure

There are a lot of metrics to be measured in this environment. A pipeline is as fast as its slowest part. Detecting wrong parts about the application and acting fast is crucial.

For product decisions:

* Number of visits(per page, per user etc) and amount of time spent on pages
* Customer growth rate(We even have a company wide bet tradition on this)
* A/B test results
* Churn rate of customers
* MTTA and MTTR(Mean Time To Acknowledge/Mean Time to Resolve) for problems

For development teams:

* Response time of different functions
* Length of database, cache transactions
* Memory and cpu utilization
* Errors in the app
* Duration of tests
* Duration of deployment
* Performance changes with new features

## Share

For shared responsibility model to work, we need shared input from all stakeholders. They need to be aligned on what the current situation is and communication between them should be easy and as transparent as possible.

DevOps is not something we can apply to our workplace by ust using some tools. It is a lot of work and requires a mentality shift for everyone who is involved. Creating a "DevOps Team" or job listings with "DevOps Engineers" is a common thing but DevOps is not a title, it is a methodology.
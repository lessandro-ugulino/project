---
layout: post
title: AWS Dashboard
date: 2020-08-26 01:00 +0700
modified: 2020-03-07 16:49:47 +07:00
description: AWS Dashboard dfsf
tag:
  - aws
  - projects
image1: /aws-dashboard/aws-dashboard.png

images:
  csv: /assets/img/ec2-snapshots.png
  dashboard: /assets/img/aws-dashboard.png

---

As the requirement for tracking down all information and also act as soon as an incident happens, this dashboard can be a great way to view and share the status across your team of all current AWS resources.

<div style="text-align:center">
<img src="{{ page.images.dashboard }}" alt="{{ page.images.dashboard }}"/>
<figcaption>Fig 1. Example AWS dashboard</figcaption>
</div>

The screenshot above represents the data from an AWS account in Europe, measuring how many EC2 are running and on the right side, how many snapshots are older than 60 days.

### Technologies Involved

- Python 3
- AWS cli
- Excel
- Jenkins
- Bash script

Basically, a Jenkins project was created to run the bash script to extract the data (quantity of EC2 and snapshots) from AWS account via aws cli and then saved it in a .csv file like below.

<div style="text-align:center">
<img src="{{ page.images.csv }}" alt="{{ page.images.csv }}"/>
<figcaption>Fig 2. Example .csv file</figcaption>
</div>

A python script then, read this .csv file and translate it into a dashboard.

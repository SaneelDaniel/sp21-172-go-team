
# CMPE 172 - Starbucks Project - Team Journal - Go Team


# Team Project (Go Team)


## Introduction

Problem Statement:

The team has been selected to bid on work for the next version of Starbucks's Online Store and Back office Apps

REQUIREMENTS:

1. Cashier's App (Frontend & Backend)

2. Online Store & Backoffice Help Desk

3. REST API

4. Backoffice Help Desk & Integrations

Team Members: - Martin Vladimirov - Maurice Washington - Saneel Daniel - Taarush Vemulapalli


## Instructions:

* Deployed instance (using Makefile + containerized stack): http://starbucks-go-team.netlify.app 

* Locally:

First, create a mysql environment: 

`docker run -d --name mysql -td -p 3306:3306 -e MYSQL_ROOT_PASSWORD=cmpe172 mysql:8.0`

Inside MySQL shell

`mysql> create database starbucks;`
`mysql> create user 'springuser'@'%' identified by 'SecretPW123';`
`mysql> grant all on starbucks.* to 'springuser'@'%';` 

Next, run the backend:
`cd final-backend && ./gradlew bootRun`

![bootRun](Images/bootRun.png)


Finally, run the front-end:
`cd final-frontend && npm install`
`npm run start`


## { Cashiers App }

Once our user creates an order, they will be redirected to our cashiers page. This will display the Order ID number, different items, and the price.
<img width="1417" alt="cashier" src="https://user-images.githubusercontent.com/36089262/118932759-40e63f00-b8fd-11eb-81b1-6363a038eed8.png">


Front End managed by Martin Vladimirov, and backend managed by Taarush Vemulapalli

## { Online Store & Backoffice Help Desk }
In order to run the front end , first type `cd final-frontend`. 

Run `npm install` and then `npm run start`

Our online store displays a variety of different drink categories that users can browse.
<img width="1373" alt="menu" src="https://user-images.githubusercontent.com/36089262/118932038-7179a900-b8fc-11eb-8ab0-568e2390747d.png">

If a user makes a report, we can view them from our backoffice help desk and resolve issues that our users may have.
<img width="1440" alt="adminreports" src="https://user-images.githubusercontent.com/36089262/118932044-73dc0300-b8fc-11eb-9877-587e6176b255.png">

Front End managed by Martin Vladimirov, and backend managed by Saneel Daniel

## { REST API }

Design and Development to be done by Taarush Vemulapalli and Saneel Daniel

* Handles user auth, payments, orders, and help tickets

## { Cloud deployment }

Design and Development to be done by Taarush Vemulapalli and Saneel Daniel

* Front-end CI/CD - Netlify:

`netlify.toml` defines the config (pointing to main repo)

On commits, we see a build/deploy trigger:

![netlify](Images/netlify.png)

For our backend, see Makefile for our docker network/push commands, under `final-backend/Makefile`


# Team Journal

## Week 1 (Project Kickoff) - (4/16/21 - 4/21/21)

- The team had meetings to discuss the requirements and setup the initial layout.
- We had discussion over responsibility division and task allocations.
- We had brainstorming session on how to start the bare-bones templates and move further from there.
- We concluded the week with task allocations and reviewing the necessary starter codes and will be laying out a boilerplate up within the next couple of days.

![week1-taskboard](Images/week1-taskboard.png)

## Week 2 

- Divided the tasks and made our own branches to make progress
- Scheduled weekly calls and deadlines for our internal goals

![week2-taskboard](Images/week2-taskboard.png)

## Week 3 

- The team had meetings to discuss the requirements 
- Completed REST endpoint (with postman tests)
- Completed cashiers/help desk screens
- Configured docker instances


![week3-taskboard](Images/week3-taskboard.png)

## Week 4

-  Final front-end and back-end integration
-  Cloud deployement and 

![week4-taskboard](Images/week4-taskboard.png)

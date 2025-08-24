# Day 1 - Docker Fundamentals

# Why Docker Need?
<img width="1284" height="613" alt="image" src="https://github.com/user-attachments/assets/db476500-ac1c-47bc-a9bb-41edd23d2c0f" />



## What is Docker

![image](https://github.com/piyushsachdeva/CKA-2024/assets/40286378/2f8eb0eb-8c2d-4460-8dbc-c43e1f3fce3e)

Before dive into Docker , Let's understand about containers.

## What is containers exactly?

It provides you an isolated environment with all the libraries , all the application code and runtime operating system dependency and everything that an application needs to run irrespective of the operating system, host operating system where it is running.

**Guest Operating system will be packaged inside the container itself.**

**Main goal of the container is to build and ship and run your application code.**

**Build ---> Ship ----> Run**

Docker is nothing but platform that helps you execute these tasks. It provides a medium for you to execute all these tasks.

Alternative tool for Docker is Podman. But Docker is most of the organisation using.


## Understanding Containers V/S Virtual Machines

![image](https://github.com/piyushsachdeva/CKA-2024/assets/40286378/b1bfe6ae-a1e6-4b04-8486-272d3ed380bc)


## Containers V/S Virtual machines with the help of a Building and House analogy


![image](https://github.com/piyushsachdeva/CKA-2024/assets/40286378/48061343-195d-4299-8815-0856e9b5af71)



## Challenges with the non-containerized applications

![image](https://github.com/piyushsachdeva/CKA-2024/assets/40286378/58b4c2dd-6abe-4acd-9318-c718e4133a91)

The Code is works in Dev Environment, Test Environment. But it is not works on prod environment. 

There Could be multiple reason for failed the Build Promotion. 

Such as, 

  1.**Environment misconfig**
  
  2.**Missing dependancy**
  
  3.**Missing libraries in the prod environment**
  
  4.**Issue with environment**
  
  5.**Issue with Infrastructure**
  
There was no easy way to package all the dependancy , libraries, Configuration along with application inside the build and ship it to all the environment including Prod Environment.

That's Why **Docker** came into the picture.

## How Docker solves the challenges

![image](https://github.com/piyushsachdeva/CKA-2024/assets/40286378/a8f134d8-b70e-4c99-857e-5da26e68674b)


## That's how docker was born(Just kidding!)

![image](https://github.com/piyushsachdeva/CKA-2024/assets/40286378/c781a038-3420-4980-a3d8-ab123fc33d95)



## A Simple Docker WorkFlow

![image](https://github.com/piyushsachdeva/CKA-2024/assets/40286378/444db8f4-1cbb-47b0-986f-489292f05b7c)



## Docker Architecture

![image](https://github.com/piyushsachdeva/CKA-2024/assets/40286378/79099c53-7f63-4bb6-885c-28cdd0850d93)

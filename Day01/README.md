# Day 1 - Docker Fundamentals

## Challenges with the non-containerized applications

![image](https://github.com/piyushsachdeva/CKA-2024/assets/40286378/58b4c2dd-6abe-4acd-9318-c718e4133a91)

The code works in the Dev environment, also works in the Test environment, but fails in the Prod environment.

There could be multiple reasons for the failure of build promotion, such as:

**Environment misconfig**

**Missing dependency**

**Missing libraries in the Prod environment**

**Issues with the environment setup**

**Issues with Infrastructure**

There was no easy way to package all the dependencies, libraries, configurations along with the application inside the build and then ship it consistently to all environments including Production.

👉 That’s why **Docker** came into the picture.


## What is Docker?

![image](https://github.com/piyushsachdeva/CKA-2024/assets/40286378/2f8eb0eb-8c2d-4460-8dbc-c43e1f3fce3e)

Before dive into Docker, Let's understand about containers.

## What is a Container Exactly?

A container provides you an isolated environment with:

All required libraries

Application code

Runtime operating system dependencies

Basically, everything that an application needs to run irrespective of the host operating system.

✅ Guest operating system dependencies are packaged inside the container itself.

✅ Main goal of a container → Build → Ship → Run your application code.

Docker is a platform that helps you execute these tasks. It provides a medium for you to build, package, and run your applications.

👉 An alternative to Docker is Podman, but Docker is still the most widely used across organizations.

## How Docker solves the challenges

![image](https://github.com/piyushsachdeva/CKA-2024/assets/40286378/a8f134d8-b70e-4c99-857e-5da26e68674b)

  Now, instead of just shipping code, we ship everything together – dependencies, libraries, application code, and even the OS image required.

This way, the application runs consistently in Production, just like it runs in Dev and Test.


## That's how docker was born(Just kidding!)

![image](https://github.com/piyushsachdeva/CKA-2024/assets/40286378/c781a038-3420-4980-a3d8-ab123fc33d95)


## Understanding Containers V/S Virtual Machines

![image](https://github.com/piyushsachdeva/CKA-2024/assets/40286378/b1bfe6ae-a1e6-4b04-8486-272d3ed380bc)


**Virtual Machine**

A Virtual Machine (VM) is nothing but a virtual computer that has:

Computing power (CPU, RAM)

Storage

Networking

An operating system installed

Everything that a physical computer needs is provided inside a VM.

👉 Typically, one VM is used to run a single application.

**Hypervisor**

A Hypervisor is the software (or hardware) that makes virtualization possible.

It allows you to create and manage multiple virtual machines on a single physical computer.

**What is Virtualization?**

Virtualization allows you to run multiple operating system instances concurrently on a single physical machine.

For example:

You can run Ubuntu, Fedora, and CentOS all at the same time on top of your Windows machine with the help of virtualization.




## Containers V/S Virtual machines with the help of a Building and House analogy


![image](https://github.com/piyushsachdeva/CKA-2024/assets/40286378/48061343-195d-4299-8815-0856e9b5af71)






## A Simple Docker WorkFlow

![image](https://github.com/piyushsachdeva/CKA-2024/assets/40286378/444db8f4-1cbb-47b0-986f-489292f05b7c)

## What is a Docker Image?

All dependencies, libraries, application code, and the OS are packaged into an image.

This image is shippable from one environment to another.

⚠️ You cannot ship containers directly across environments. Instead, you ship the image, and then run containers from it.

💡 Usually, you should have one Dockerfile per application.


## Docker Architecture

![image](https://github.com/piyushsachdeva/CKA-2024/assets/40286378/79099c53-7f63-4bb6-885c-28cdd0850d93)

**1. Run the docker build command on the CLI**
This is the first step — we ask Docker to build an image.

**2. Dockerd reads the Dockerfile (source code + instructions)**
The Docker daemon (dockerd) takes the Dockerfile we provided.

**3. Docker creates an image and stores it in the host (local image store)**
Now the image is packaged and saved locally on the container host.

**4. Run the docker push command**
If we want to share the image, we push it to a registry.

**5. Dockerd takes the local image and pushes it to the Registry**
The daemon uploads the image from host storage to Docker Hub or a private registry.

**6. Run the docker pull command**
If we want an image that is not on the host, we pull it from the registry.

**7. Dockerd pulls the image from the Registry into local host storage**
Now the image is available locally to use for containers.

**8. Run the docker run command**
We use this to start a container from the image.

**9. Container starts running on the Container Host**
Finally, the container is created and executed with all dependencies, libraries, and code.


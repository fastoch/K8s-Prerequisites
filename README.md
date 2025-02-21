# K8s-Prerequisites

 Do NOT Learn Kubernetes Without Knowing These Concepts... - https://www.youtube.com/watch?v=wXuSqFJVNQA  

# Understand Containerization

As a developer, or as a DevOps engineer, you will deploy containerized apps & services to K8s.  

## Docker definition

Docker is a containerization engine created by a french guy named Solomon Hykes. First release was in 2013.  

Docker defines a container as a standard unit of software that packages up code and all its dependencies so the application runs quickly and reliably from one computing environment to another.  

A Docker container image is a lightweight, standalone, executable package of software that includes everything needed to run an application: 
- code
- runtime
- system tools
- libraries
- and settings

---

## Dockerfile

To containerize your app, you first create a dockerfile that has all the instructions for building an image of your app.  

So, if you're containerizing a **React** app, you might start off with: 
- pulling a **Node** runtime (from the Docker Hub registry),
- then you'll add your **package.json**,
- then you'll install dependencies,
- then you'll add your code
- then you'll add the `npm run start` command to start your app

![image](https://github.com/user-attachments/assets/1ac6ec1a-fee1-4800-abbc-5f27216fd387)

`CMD ['npm', 'start']` is a Dockerfile instruction used to specify the default command that should be executed when a container is run from an image.  
When this command is executed, it typically runs a predefined **script** specified in the "start" property of a package's "scripts" object in the **package.json** file.  

Using `CMD ['npm', 'start']` in a Dockerfile is a common practice for Node.js applications, as it provides a standardized way to start the application regardless of its specific entry point.  

---

## Build an image and run a container

Once you have this dockerfile assembled, you can use Docker to build an image. This image will be the blueprint for running your app.   
This image becomes a container at runtime. When you run the image, Docker is going to follow the steps, the instructions provided in your dockerfile.  
If you go to an image repository like Docker Hub, you can find thousands of images that you can pull down to your computer and run in a container. There's images for pretty much anything...  

## The benefits of containerization

Containers are isolated environments which offer portability and ease of use, you can spin them up or down very easily.  
You can run multiple copies of a container for ensuring high availability, and couple that with load balancing.  
And they can run on any computer, regardless of the host OS, no need to worry about hardware or software compatibility.  

---

## What is K8s

K8s, short for Kubernetes, is an environment for you to orchestrate and automate: 
- the deployment,
- the management,
- the scaling,
- and the networking
of your containers.

---

# Cloud Basics

That is the second prerequisite you need prior to learning K8s.  






@5/13
---
EOF

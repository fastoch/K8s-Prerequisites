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

That is the second prerequisite you need to cover prior to learning K8s.  

Companies often choose to deploy K8s in the Cloud, as a managed solution.  
So, understanding the basics of Cloud computing is essential before learning K8s.

The Cloud providers manage the K8s clusters on their own Virtual Machines or servers.  
And from there, it can tie into all the other services that a Cloud provider offers, such as:
- identity and access 
- logging
- networking
- ...

However, when you deploy K8s in the Cloud, it can get expensive pretty quick.

---

# YAML and Declarative configurations

The third prerequisite to learning K8s.  
YAML = YAML ain't markup language (a recursive acronym like GNU is not Unix).  

YAML is a data serialization language for writing configuration files.  
It's a superset of JSON. Every JSON file is also a valid YAML file.  

The resources in K8s are created in a declarative way.  
You declare how you want things to be, and K8s will make sure that it meets that declaration.  

That declarative configuration is provided in a .yaml config file called a **manifest** file.  
This manifest file describes the desired state of a K8s object.  

In other terms, YAML files are configuration files that house the declaration of your K8s objects.  

---

# Networking basics

The fourth prerequisite before learning K8s, specifically Linux networking.  
In K8s there's communication between the pods and the containers within them, and there's networking out to external destinations.  

There are different networking service types:
- clusterIP
- LoadBalancer
- NodePort

You need to grasp networking concepts like:
- OSI Model
- Networking Protocols
- IP configuration
- DNS
- Routing

---

# Terminal proficiency

The fifth prerequisite to learning K8s.  
To interact with a K8s cluster, you'll use the `kubectl`, a CLI tool.  

https://kubernetes.io/docs/reference/kubectl/

---
EOF

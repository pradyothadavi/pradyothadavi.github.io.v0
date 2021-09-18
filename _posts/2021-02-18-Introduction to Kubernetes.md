---
name: Introduction to Kubernetes
layout: post
title: Introduction to Kubernetes
---

The way software applications have been deployed, has evolved over a period of time. Better hardware resource utilisation
has been one of the key objectives. Today, container based deployments are popular and one of the most preferred way of
deployment.

![Deployment Evolution](https://d33wubrfki0l68.cloudfront.net/26a177ede4d7b032362289c6fccd448fc4a91174/eb693/images/docs/container_evolution.svg)
*Reference: [what-is-kubernetes](https://kubernetes.io/docs/concepts/overview/what-is-kubernetes/)*

#### **What is a container?**

A container is the runtime instantiation of a _Container Image_. It is a standard Linux process typically
created through a clone() system call instead of fork() or exec().

There are two states of container
* rest
* running

When at rest, a container is a file( or set of files ) that is saved on disk. It is referred to as Container Image.

When you type the command to start a container, the Container Engine unpacks the required files and meta-data, then
hands them off to the Linux kernel. In running state, containers are just a Linux process.

 [Container Terminology](https://developers.redhat.com/blog/2018/02/22/container-terminology-practical-introduction/){:target="_blank"} is
 a good primer to understand a little more in depth.

 [Open Container Initiative](https://opencontainers.org/){:target="_blank"} under [The Linux Foundation](https://www.linuxfoundation.org/){:target="_blank"}
 is creating open industry standards around container formats and runtime.

Docker, Container Linux ( CoreOS Linux ), cri-o are few examples.

#### **What is Kubernetes?**

Containers provide mechanisms to bundle your applications and make them agnostics of the underlying hardware, however
managing and orchestrating different containers comes with its own challenges. [Borg](https://research.google/pubs/pub43438/){:target="_blank"}
is a cluster management system used within Google for managing and running containerized workload. This was open sourced
in the year 2015 as Kubernetes, also known as K8s.

Kubernetes is a portable, extensible, open-source platform for managing containerized workloads and services, that facilitates both declarative configuration and automation.

---
name: Workloads
layout: post
title: K8 workload cheatsheet
---

A workload is an application running on Kubernetes. The basic deployable unit on K8s is Pod. The workload runs inside a 
set of Pods.

Kubernetes provides different built-in workload resources for managing a set of pods. These workload resources are as
follows
* ReplicaSet
* Deployment
* StatefulSet
* DaemonSet
* Job
* CronJob

Using the custom resource definition, additional workload resources can be defined.
---
layout: page
title: Platform Dictionary
permalink: /guides/platform-dictionary/
hide: true
---

## Objective
Familiarize yourself with basic platform terminology. Some content may be duplicated across other guides but will contain more detail and context around the terms.

## High-Level

### Astronomer Platform
All of the __Astronomer core__ components and __deployment__ specific components which live on a Kubernetes cluster.

### Astronomer Core
The core applications that make up the __Astronomer Platform.__ There is only one instance of each component with a single Astronomer install.

### Deployment Components
The applications specific to a single Airflow __deployment__.

### Platform Install
A single installation of the __Astronomer Platform__. Will include the core components as well as __deployment components__ for each __deployment__ created on your cluster.

### Astronomer Project
An Airflow project directory containing dependency files. In most circumstances it is one to one with a production __deployment__. 

### Deployment
A named Airflow cluster. Mapped to only a single __Astronomer project__.

### Workspace
Workspaces contain a group of Airflow Cluster __Deployments__.

## Platform Components

### astro-cli
A command line tool giving the programmatic access to the __Astronomer Platform__

### houston-api
A GraphQL API responsible for handling request from the user or user-level platform components (astro-cli, orbit-ui).

### commander
Handles gRPC requests from the __houston-api__ in order to provision, update and delete Airflow __deployments__ on the __Astronomer Platform__.

### orbit-ui
A webUI built on React. Provides a clean visual experience for users who will be administrating and monitoring the platform.

## Airflow Components

### Executor
[Executors](https://airflow.incubator.apache.org/code.html?highlight=executor#executors) are the mechanism by which task instances get run.

### Webserver
The user interface for monitoring, administrating and developing Airflow.

### Scheduler
The [Airflow scheduler](https://airflow.incubator.apache.org/scheduler.html?highlight=scheduler#scheduling-triggers) monitors all tasks and all DAGs, and triggers the task instances whose dependencies have been met.

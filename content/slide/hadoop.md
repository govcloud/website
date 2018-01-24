+++
draft = false
title = "Statistics Canada Presentation"
description="Statistics Canada Presentation in Ottawa."
language = "en"
tags = [
    "drupal",
    "slide"
]
date = "2017-01-01T13:10:52-05:00"
type = "slide"
+++

<!-- .slide: id="hadoop" data-transition="concave" -->

# Hadoop

[govcloud/charts](http://github.com/govcloud/charts) <i class="fa fa-github"></i></li>

Note:

---

<!-- .slide: id="intro" data-transition="concave" -->

# Agenda

1. Containers
2. Kubernetes
3. Charts

Note:

---

<!-- .slide: id="containers" data-transition="concave" -->

# Containers

> Containers will yield the following benefits to Government:

<div class="col-xs-6 col-sm-6 col-md-6">
  <ul class="list-unstyled">
    <li>Platform independence</li>
    <li>Resource efficiency and density</li>
    <li>Effective isolation and resource sharing</li>
    <li>Speed</li>
  </ul>
</div>

<div class="col-xs-6 col-sm-6 col-md-6">
  <ul class="list-unstyled">
    <li>Immense and smooth scaling</li>
    <li>Operational simplicity</li>
    <li>Developer productivity</li>
    <li>Development pipeline</li>
  </ul>
</div>

Note:

**Platform independence: Build it once, run it anywhere**

A major benefit of containers is their portability. In particular containers help to facilitate a cloud native approach via a microservices architectural design pattern.

A container wraps up an application with everything it needs to run, like configuration files and dependencies. This enables you to easily and reliably run applications on different environments such as your local desktop, physical servers virtual servers, testing, staging, production environments and public or private clouds.

This portability grants organisations a great amount of flexibility, speeds up the development process and makes it easier to switch to another cloud environment or provider, if need be.

**Resource efficiency and density**

Since containers do not require a separate operating system, they use up less resources. While a VM often measures several gigabytes in size, a container usually measures only a few dozen megabytes, making it possible to run many more containers than VMs on a single server.

Since containers have a higher utilisation level with regard to the underlying hardware, you require less hardware, resulting in a reduction of bare metal costs as well as datacentre costs.

**Effective isolation and resource sharing**

Although containers run on the same server and use the same resources, they do not interact with each other. If one application crashes, other containers with the same application will keep running flawlessly and won’t experience any technical problems. This isolation also decreases security risks: If one application should be hacked or breached by malware, any resulting negative effects won’t spread to the other running containers.

**Speed: Start, create, replicate or destroy containers in seconds**

As mentioned before, containers are lightweight and start in less than a second since they do not require an operating system boot. Creating, replicating or destroying containers is also just a matter of seconds, thus greatly speeding up the development process, the time to market and the operational speed. Releasing new software or versions has never been so easy and quick. But the increased speed also offers great opportunities for improving customer experience, since it enables organisations and developers to act quickly, for example when it comes to fixing bugs or adding new features.

**Immense and smooth scaling**

A major benefit of containers is that they offer the possibility of horizontal scaling, meaning you add more identical containers within a cluster to scale out. With smart scaling, where you only run the containers needed in real time, you can reduce your resource costs drastically and accelerate your return on investment. Container technology and horizontal scaling has been used by major vendors like Google and Twitter for years now.

**Operational simplicity**

Contrary to traditional virtualisation, where each VM has its own OS, containers execute application processes in isolation from the underlying host OS. This means that your host OS doesn’t need specific software to run applications, which makes it simpler to manage your host system and quickly apply updates and security patches.

**Improved developer productivity and development pipeline**

A container-based infrastructure offers many advantages, promoting an effective development pipeline. Let’s start with one of the most well-known benefits. As mentioned before, containers ensure that applications run and work as designed locally. This elimination of environmental inconsistencies makes testing and debugging less complicated and less time-consuming since there are fewer differences between running your application on your workstation, test server or in production environment. The same goes for updating your applications: you simply modify the configuration file, create new containers and destroy the old ones, a process which can be executed in seconds. In addition to these well-known benefits, container tools like Docker offer many other advantages. One of these is version control, making it possible for you to roll-out or roll-back with zero downtime. The possibility to use a remote repository is also a major benefit when working in a project-team, since it enables you to share your container with others.

## Data Points

* 71% of Fortune 100 companies are running containers

---

<!-- .slide: id="kubernetes" data-transition="concave" -->

# Kubernetes

> Kubernetes will yield the following benefits to Government:

<div class="col-xs-6 col-sm-6 col-md-6">
  <ul class="list-unstyled">
    <li>Managed complexity</li>
    <li>Vendor lock-in</li>
    <li>Multi cloud</li>
    <li>Self-healing</li>
  </ul>
</div>

<div class="col-xs-6 col-sm-6 col-md-6">
  <ul class="list-unstyled">
    <li>Google backed</li>
    <li>Vibrant community</li>
    <li>Big name supporters</li>
    <li>Flexibility</li>
  </ul>
</div>

Note:

**Managed complexity**: Automation of the deployment, scaling, and operation of application containers in a clustered environment via primitives

**Vendor Lock-in**: Essentially every major cloud provider (public, private, hybrid) support Kubernetes

**Multi-Cloud**: Ideal for managing multi-cloud environments / workloads

**Self-healing**: Auto-placement, auto-restart, auto-replication, auto-scaling

**Google Backed**: Originally built by Google leveraging a decade of experience running containers at scale

**Vibrant Community**: One of the fastest moving projects in open source history

**Big Name Supporters**: Google, Microsoft, AWS, IBM, RedHat, Oracle, VMWare, Intel, Pivotal etc

**Flexibility**: Simplicity of a PaaS with the flexibility of IaaS

> Interesting data points

* 54% of Fortune 100 companies are running Kubernetes
* Housed within a large, neutral open source foundation, the Cloud Native Computing Foundation
* CNCF consists of enterprise companies such as Microsoft, Google, AWS, SAP, Oracle, Pivotal, etc
* Kubernetes has won the orchestration wars and is recognized as the de facto standard for container orchestration
* Gartner: By 2020, more than 50% of global enterprises will be running containerized applications in production.
* With that, Kubernetes has emerged as the leading orchestration method in the market with a 71% adoption rate.

---

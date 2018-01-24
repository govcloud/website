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

# Cloud Ops

[govcloud/charts](http://github.com/govcloud/charts) <i class="fa fa-github"></i></li>

Note:

This a presentation created by the new cloud operations team. Expect to see a lot more from us in the coming weeks. Additionally if want to follow our work more closely please consult either our website, slack
channel, or github organization.

---

<!-- .slide: id="intro" data-transition="concave" -->

# Agenda

1. Containers
2. Kubernetes
3. Toolchain
4. Helm (Charts)
5. Big Data
6. Azure (AKS/ACS)

Note:

The agenda for this presentation is fairly straightforward and while each of these sections could easily take hours to explain I will do my best to provide an accurate summation.

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

Everyone that learns about containers and their server immutability concept invariably loves them, because of the power they give, both on the development and in the deployment sides.

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
    <li>Open Service Broker</li>
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

As containers become more popular each day, more technology is being developed to help unleash all the power containers can offer. One of the most useful technologies created around containers in the deployment side is orchestrators.

A container orchestrator is a software that is able to orchestrate and organize containers across any number of physical or virtual nodes. The potential of this is enormous, as it greatly simplifies the deployment of the infrastructure (each node only has Docker installed) and its operation (as all servers are exactly equal). The container orchestrator takes in account things as failing nodes, adding more nodes to the cluster or removing nodes from the cluster by moving the containers from one node to another to keep them available at all times.

While containers + orchestrators technology not only resolves a lot of problems related with infrastructure management, it also resolves a lot of problems regarding deploying software in the infrastructure, as the software, its dependencies and runtime are always deployed at the same time, minimizing the errors commonly associated to deployments in non-immutable environments.

Kubernetes has won the orchestrator wars, hands down and as of 2018 now takes center stage. This is proved by every single cloud vendor integrating with it and providing their own managed service. Additionally by most PAAS's offering first class support for it. (Pivotal, OpenShift, Tectonic, ...)

**Managed complexity**: Automation of the deployment, scaling, and operation of application containers in a clustered environment via primitives

**Vendor Lock-in**: Essentially every major cloud provider (public, private, hybrid) support Kubernetes

**Multi-Cloud**: Ideal for managing multi-cloud environments / workloads

**Self-healing**: Auto-placement, auto-restart, auto-replication, auto-scaling

**Google Backed**: Originally built by Google leveraging a decade of experience running containers at scale

**Vibrant Community**: One of the fastest moving projects in open source history, 2nd largest. Additionally over 30,000 users on slack many google engineers.

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

<!-- .slide: id="tooling" data-transition="concave" -->

# Tooling

> The dev tooling on top of k8s namely Helm, Draft, Brigade and Kashti are the Bell Labs of the cloud era

Note:

This was a quote that I have heard more then a few times by some big name developers working on AKS @ Microsoft.

I'll only be demonstrating the Helm component but wanted to very quickly highlight applicable tooling.

---

<!-- .slide: id="charts" data-transition="concave" -->

# Helm (Charts)

> Helm is a tool for managing Kubernetes charts. Charts are packages of pre-configured Kubernetes resources.

* Kubernetes package manager
* Reproducible builds of your k8s applications
* Intelligently manage your k8s manifest files
* Manage releases of Helm packages

Note:

Helm makes doing reliable reproducible deployments ridiculously easy to Kubernetes, and is the standard way of working with Kubernetes.

Think of Helm as the package manager for Kubernetes similar to apt/yum/apk. If you deploy applications to Kubernetes, Helm makes it incredibly easy to version those deployments, package it, make a release of it, and deploy, delete, upgrade and even rollback those deployments as charts. Charts being the terminology that helm use for package of configured Kubernetes resources.

---

# Helm (Charts)

* CNCF
* Prometheus
* Grafana
* Portal

Note:

Now that we have a brief overview of what a Helm chart is I thought I would go over a couple before get into specific Big Data topics.

---

## Big Data

* Advantages of Containers + Orchestrators for distributed computing
* Spark on k8s
* HDFS on k8s

Note:

With the numerous advantages of containers and orchestrators being in the distributed computing domain, the BigData world, which extensively relies on enormous amounts of distributed computing power have taken notice over the past couple years.

Particular companies such as:

* Google
* Red Hat
* Comcast
* Intel
* Palantir
* Bloomberg
* PepperData
* TerraData

have solved many of the barriers that initially thwarted containers from thriving in the Big Data ecosystem.

## Spark on k8s

* Patching up Spark Driver and Executor Code
* Often times Spark stores data on HDFS
* Show different aspects of Spark ecosystem in k8s
* Spark cluster
* Spark on k8s
* Spark operator

## Comparison with Spark Standalone on Kubernetes

The proposed design is more flexible than the basic Kubernetes Spark example for several
reasons:

1. Spark executors can be elastic depending on job demands, since spark can speak

directly to kubernetes in order to provision executors as required.
2. The proposed solution allows leveraging of Kubernetes constructs like ResourceQuota,

namespaces, audit logging, etc. Contrasting with Spark standalone where Spark’s notion
of identity is disparate and unaware of Kubernetes constructs like service accounts.

3. The proposed solution allows for greater isolation between Spark Jobs than standalone

mode, as each of them runs in their own container, utilizing cgroups to enforce CPU and
memory requests and limits.

4. When submitting jobs against a standalone Spark cluster running on Kubernetes, one is

restricted to using the Docker image that the standalone Spark cluster was launched
with to run the executors. The proposed design allows the user to specify a custom
docker image​ for the driver and executors when the user submits the job.

5. The proposed design simplifies the process of running Spark jobs: while the current

solution requires two steps to first run the standalone Spark cluster and then to run the
Spark jobs against that cluster, the proposed design requires no prior k8s setup​ to run
the user's application.

6. The proposed solution adds a Resource Staging Server (RSS) component that simplifies

the deployment of user-specified jars and files which is still difficult with a Spark
Standalone cluster on Kubernetes.

7. In the existing solution, resource negotiation for spark jobs is tied to the configuration of

the standalone Spark cluster as well as the configuration of the Kubernetes cluster. If the
second layer of the standalone cluster manager is eliminated, then the user can unify all
resource administration and configuration​ into the Kubernetes framework alone.

8. Kubernetes is a popular container orchestration environment with wide adoption. Users

who are already deploying applications on Kubernetes, or who plan to, will benefit from
the ability to run Spark applications on Kubernetes as well, instead of running a separate
standalone Spark cluster or managing a separate orchestration environment.

## HDFS on k8s

* Data locality
* Rack locality
* Node preference
* Kerberos
* Namenode High Availability

## Why deploy Hadoop in Containers?

1) You are heavily over provisioned. You run Hadoop clusters in silos, and every time you need to bring up a silo, you create a new physical (cloud or on prem) hardware footprint to host this Hadoop cluster. Virtualization is not an option, since you want to get bare-metal performance. You have unused clusters that are consuming storage and compute resources. Since they are pinned to physical infrastructure, it is difficult to reuse resources.

2) You desire to host a common platform as a service for multiple Hadoop end users (internal customers). You also want to run other data services like Cassandra on this same infrastructure.

3) Your HDFS data lakes have inconsistencies. Since you create multiple silos for each Hadoop cluster, you are unable to audit or validate the correctness of the data in the data lakes. Since these data lakes are created separately from the deployment of your Hadoop cluster, you have no control over the governance of its data.

4) You are spending too much time with manual resources used to create silos. Your end users are unable to deploy Hadoop clusters without IT intervention and out of band compute and storage provisioning. You want to get to a mode where clusters can be deployed in a self-service, programmatic manner.

Traditionally, Hadoop has been deployed directly on bare metal servers in a siloed environment. As the number of Hadoop instances and deployments grow, managing multiple silos becomes problematic. The specific issues with managing multiple Hadoop silos on fixed physical infrastructure are:

* Under utilization of server and storage resources.
* Manual out of band storage and compute provisioning for each new deployment.
* Creation of multiple conflicting data lakes (data inconsistencies between silos).
* Zombie resources after the completion of a job.

Typically, some form of virtualization is needed to manage any large application deployment to solve these issues. Virtual machines however add a layer of overhead that is not conducive to big data deployments. This is where the advent of containers becomes useful. By deploying Hadoop inside of Linux containers, you can get the power of virtualization with bare metal performance. You also empower a DevOps model of deploying applications - one in which out-of-band IT is not involved as your application owners deploy and scale their Hadoop clusters.

The benefits of running Hadoop with containers are:

* Enable Hadoop to run on a cloud-native storage infrastructure that is managed the same way, whether you run on-premise or in any public cloud
* Faster recovery times during a failure for Data, Name and Journal nodes.
* Increased resource utilization because multiple Hadoop clusters can be safely run on the same hosts
* Improved Hadoop performance with data locality or hyperconvergence
* Dynamic resizing of HDFS volumes with no downtime
* Simplified installation and configuration of Hadoop

---

<!-- .slide: id="azure" data-transition="concave" -->
# Azure

* aks scale

Note:

---

<!-- .slide: id="pachyderm" data-transition="concave" -->
# Pachyderm

* Hadoop hard to find at Strata
* According to Gartner Hadoop is dead

Note:

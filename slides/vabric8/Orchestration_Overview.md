# Orchestration, an overview

In this chapter, we will:

* Explain what is orchestration and why we would need it.

* Present (from a high-level perspective) some orchestrators.

* Show one orchestrator (Openshift/Kubernetes) in action.

---

class: pic

## What's orchestration?

![Joana Carneiro (orchestra conductor)](images/conductor.jpg)

---

## What's orchestration?

According to Wikipedia:

*Orchestration describes the __automated__ arrangement,
coordination, and management of complex computer systems,
middleware, and services.*

--

*[...] orchestration is often discussed in the context of 
__service-oriented architecture__, __virtualization__, provisioning, 
Converged Infrastructure and __dynamic datacenter__ topics.*

---

## What is scheduling?

According to Wikipedia (again):

*In computing, scheduling is the method by which threads, 
processes or data flows are given access to system resources.*

The scheduler is concerned mainly with:

- throughput (total amount or work done per time unit);
- turnaround time (between submission and completion);
- response time (between submission and start);
- waiting time (between job readiness and execution);
- fairness (appropriate times according to priorities).

In practice, these goals often conflict.

**"Scheduling" = decide which resources to use.**

---

* Scheduling with multiple resources (dimensions) is hard.

* Don't expect to solve the problem with a Tiny Shell Script.

* There are literally tons of research papers written on this.

---

## But our orchestrator also needs to manage ...

* Network connectivity (or filtering) between containers.

* Load balancing (external and internal).

* Failure recovery (if a node or a whole datacenter fails).

* Rolling out new versions of our applications.

  (Canary deployments, blue/green deployments...)


---

## Some orchestrators

We are going to present briefly a few orchestrators.

There is no "absolute best" orchestrator.

It depends on:

- your applications,

- your requirements,

- your pre-existing skills...

---

## Nomad

- Open Source project by Hashicorp.

- Arbitrary scheduler (not just for containers).

- Great if you want to schedule mixed workloads.

  (VMs, containers, processes...)

- Less integration with the rest of the container ecosystem.

---

## Mesos

- Open Source project in the Apache Foundation.

- Arbitrary scheduler (not just for containers).

- Two-level scheduler.

- Top-level scheduler acts as a resource broker.

- Second-level schedulers (aka "frameworks") obtain resources from top-level.

- Frameworks implement various strategies.

  (Marathon = long running processes; Chronos = run at intervals; ...)

- Commercial offering through DC/OS my Mesosphere.

---

## Rancher

- Rancher 1 offered a simple interface for Docker hosts.

- Rancher 2 is a complete management platform for Docker and Kubernetes.

- Technically not an orchestrator, but it's a popular option.

---

## Swarm

- Tightly integrated with the Docker Engine.

- Extremely simple to deploy and setup, even in multi-manager (HA) mode.

- Secure by default.

- Strongly opinionated:

  - smaller set of features,

  - easier to operate.

---

## Kubernetes

- Open Source project initiated by Google.

- Contributions from many other actors.

- *De facto* standard for container orchestration.

- Many deployment options; some of them very complex.

- Reputation: steep learning curve.

- Reality:

  - true, if we try to understand *everything*;

  - false, if we focus on what matters.

---

## Openshift: Kubernetes / Docker in action

.center[![test environment](images/openshiftTestOmgeving.jpg)]

# Docker 30,000ft overview

In this intro, we will talk about:

* Why containers (non-technical elevator pitch)

* How Docker helps us to build, ship, and run

---

## OK... Why the buzz around containers?

* The software industry has changed

* Before:
  * monolithic applications
  * long development cycles
  * single environment
  * slowly scaling up

* Now:
  * decoupled services
  * fast, iterative improvements
  * multiple environments
  * quickly scaling out
  * cloud native applications
  * continuous integration, - delivery, - deployment

---

## Cloud Native Software

* Cloud is about WHERE we are computing; Cloud Native is about How.
* Cloud Native software is highly distributed, must operate in a constantly changing environment and is constantly changing
* Failure is the rule, not the exception
  * Zero downtime
  * short feedback time
  * Mobile and Multi-Device Support
  * Connected devices - (IOT)
  * Data driven 

---

class: pic

## Cloud Native

* Open Source, Standards, API driven.
* Agile: Continuous Integration / Continuous Delivery
* Flexible: elastic, scale;
* Microservices: resilient, composable

![cloudnative](images/cloudNativeImage.png)

---

class: pic

## Continuous

![cicd](images/cicdPipeline.png)


---

## Deployment becomes very complex

* Many different stacks:
  * languages
  * frameworks
  * databases

* Many different targets:
  * individual development environments
  * pre-production, QA, staging...
  * production: on prem, cloud, hybrid

---

class: pic

## The deployment problem

![problem](images/shipping-software-problem.png)

---

class: pic

## The matrix from hell

![matrix](images/shipping-matrix-from-hell.png)

---

class: pic

## The parallel with the shipping industry

![history](images/shipping-industry-problem.png)

---

class: pic

## Intermodal shipping containers

![shipping](images/shipping-industry-solution.png)

---

class: pic

## A new shipping ecosystem

![shipeco](images/shipping-indsutry-results.png)

---

class: pic

## A shipping container system for applications

![shipapp](images/shipping-software-solution.png)

---

class: pic

## Eliminate the matrix from hell

![elimatrix](images/shipping-matrix-solved.png)

---

## Results

* [Dev-to-prod reduced from 9 months to 15 minutes (ING)](
  https://www.docker.com/sites/default/files/CS_ING_01.25.2015_1.pdf)

* [Continuous integration job time reduced by more than 60% (BBC)](
  https://www.docker.com/sites/default/files/CS_BBCNews_01.25.2015_1.pdf)

* [Deploy 100 times a day instead of once a week (GILT)](
  https://www.docker.com/sites/default/files/CS_Gilt%20Groupe_03.18.2015_0.pdf)

* [70% infrastructure consolidation (MetLife)](
  https://www.docker.com/customers/metlife-transforms-customer-experience-legacy-and-microservices-mashup)

* [60% infrastructure consolidation (Intesa Sanpaolo)](
  https://blog.docker.com/2017/11/intesa-sanpaolo-builds-resilient-foundation-banking-docker-enterprise-edition/)

* [14x application density; 60% of legacy datacenter migrated in 4 months (GE Appliances)](
  https://www.docker.com/customers/ge-uses-docker-enable-self-service-their-developers)

* etc.

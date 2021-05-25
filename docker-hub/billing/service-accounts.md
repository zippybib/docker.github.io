---
description: Service Accounts
keywords: Docker, Docker Hub, subscription, service account
title: Service Accounts
---

A service account is a Docker ID used for automated management of container images or containerized applications. Service accounts are typically used in automated workflows, and do not share Docker IDs with the members in the Team plan. Common use cases for this include mirroring content on Docker Hub, or tying in image pulls from your CI/CD process.

> **Note:**
> 
> Service accounts included with the Team plan are limited to 15,000 pulls per day.  If you require a higher number of pulls, you may purchase an **Enhanced Service Account add-on.**
 
## Enhanced Service Account Add-On Pricing
| Tier | Pull Rates Per Day* | Annual Fee |
| ------ | ------ | ------ | 
| 1 | 15-50k | $9,950/yr |  
| 2 | 50-150k | $17,950/yr |
| 3 | 150k-500k | $60,000/yr |
| 4 | 500k+ | Tier 4+ $60k/yr/500k Pull increment | 

<sub>*Once the initial Tier is established, that is the minimum fee for the year.  Annual commitment required.  The service account may exceed Pulls by up to 25% for up to 20 days during the year without incurring additional fees.  Reports on consumption will be provided upon request.  At the end of the initial 1-year term, the appropriate Tier will be established for the following year.<sub>
 
## How a Pull is defined:

- A pull request is defined as up to two `GET` requests on registry manifest URLs (`/v2/*/manifests/*`).
- A normal image pull makes a single manifest request.
- A pull request for a multi-arch image makes two manifest requests.
- `HEAD` requests are not counted.
- Limits are applied based on the user doing the pull, and not based on the image being pulled or its owner.


Additional information can be found in our documentation pages:
- https://docs.docker.com/registry/recipes/mirror/
- https://docs.docker.com/docker-hub/repos/#service-accounts


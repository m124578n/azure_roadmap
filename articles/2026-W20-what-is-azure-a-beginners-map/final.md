# What is Azure? A Beginner's Map

**Week:** W20 (2026-05-11)
**Status:** published
**Dev.to URL:** [(fill after publish)](https://dev.to/shunchih/what-is-azure-a-beginners-map-424p)

---

## Introduction

![Microsoft Azure](FILL_IN_IMAGE_URL)

Azure is Microsoft's cloud platform. With Azure, you can build and tear down an entire environment without purchasing any physical hardware.

I've been using Azure for two years, but I never really understood the full picture. That's what pushed me to pursue an Azure certification — and to start documenting everything I learn along the way.

---

## Why Azure? What Problems Does It Solve?

Imagine you're a software engineer in the 2000s. You land a job building an official website for a company. Before writing a single line of code, you need a server, a router, a static IP address, a physical space to store it all — and then you spend weeks wiring everything together.

Finally, the site is live. Then, one week later, the entire city loses power. The website goes down with it.

You suggest to your boss: "Maybe we should set up a backup system in another location, so the next outage doesn't take us down." Your boss says: "Too expensive. Let's keep things as they are."

Then, in 2010, Azure launches. You take a look and immediately see the potential: if you move your infrastructure to the cloud, everything becomes easier to build, easier to scale, and easier to maintain — without owning a single piece of hardware.

That's the core promise of Azure: high availability, elastic scalability, and low maintenance overhead — all without managing physical infrastructure. And perhaps most importantly: you only pay for what you use. No upfront hardware costs, no idle servers burning money at 3 a.m.

## Core Service Categories

Azure has hundreds of services, but here are the ones I use most often:

| Service | Category | What it does |
|---|---|---|
| Virtual Machine | Compute (IaaS) | A full VM in the cloud — you control everything except the physical hardware |
| Container Apps | Compute (PaaS) | Run serverless containers with automatic scaling |
| Azure Container Registry | Compute | Stores container images, like a private Docker Hub |
| Storage Account | Storage | Stores files, blobs, queues, and tables |
| Virtual Network | Networking | Isolates and connects Azure resources, like a private network in the cloud |
| Key Vault | Security | Stores secrets, passwords, and certificates securely |
| Log Analytics | Monitoring | Collects and queries logs from all your Azure services |
| Azure OpenAI | AI | Provides access to GPT and other OpenAI models |
| Azure AI Speech | AI | Text-to-speech and custom voice models |

## How Azure is Organized

Azure has data centers in dozens of countries, each called a **region**. Regions differ in pricing, and not all services are available everywhere — for example, the latest AI features often launch in the US first.

A **resource group** is a container for all the services that belong to one project. It keeps things organized and makes it easy to track costs per project.

A **subscription** sits above resource groups and acts as a higher-level boundary. You can use it to set quotas across all your resource groups — limiting how many vCPUs, IP addresses, virtual networks, and other resources can be used in total.

The hierarchy looks like this:

**Subscription → Resource Groups → Resources**

---

## Summary

Here's what we covered:

- **Why Azure?** — Cloud removes the burden of physical infrastructure. It means even a single person can build and run their own large-scale service. You get high availability, scalability, and a pay-as-you-go model that makes the "too expensive" excuse a lot harder to justify.
- **Core services** — Azure has hundreds of services, but most workloads rely on a handful: VMs, containers, storage, networking, and security primitives like Key Vault.
- **How it's organized** — Resources live in resource groups, resource groups live in subscriptions, and everything is deployed to a region of your choice.

## What's Next

This was the 30,000-foot view. Starting next week, I'll be diving into each area in more depth as I work through my Azure certification.

Next up: **Azure Identity — Entra ID vs Traditional Active Directory**. If you've ever wondered why "logging into Azure" feels different from logging into a corporate Windows machine, that's exactly what we'll unpack.

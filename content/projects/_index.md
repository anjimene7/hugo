---
title: "Projects"
type: page
---


### Hello, here are some of the projects I am working on

---------

## 1. Homelab setup

The initial driver for the homelab implementation was when Google decided to stop the free tier for unlimited photos upload (June 2019). Since that day I started looking for solutions to backup my personal photos.

I started with a Synology DS218+ NAS for which I progressively upgraded the ram to 6BG, 12GB and 16GB after dismantling the case. This was required as I had more and more Docker containers running on the machine that I use as primary hosting location.

I ended up buying a second refurbished NAS for media storage purposes mostly, with a total size of 21TB SHR. 

I also had 2 Raspberry Pis lying around and thought of using them for a new project as my previous uses cases were now covered with the primary NAS.

Over the course of 2 years I progressively started to host more and more applications for personal use and learnt quite a lot on several technologies, mostly Docker, Grafana, Prometheus, etc. All of them were initially accessible through VPN served from my router. I have recently implemented Single Sign-On (SSO) with Multi-Factor Authentication (MFA) ([Authentik](https://goauthentik.io/)) to be able to communicate safely with some applications outside of my network and have a seamless experience with native mobile apps (especially for photos backup: [Immich](https://immich.app/) and [PhotoPrism](https://www.photoprism.app/))

My current homelab topology is the following:

[//]:[![Resize](/images/homelab_topology.drawio.png)](https://viewer.diagrams.net/?tags=%7B%7D&highlight=000000&edit=_blank&layers=1&nav=1&title=homelab_topology#Uhttps%3A%2F%2Fraw.githubusercontent.com%2Fanjimene7%2Fhomelab_topology%2Fmain%2Fhomelab_topology)
[![Resize](/images/homelab_topology.drawio.png)](/images/homelab_topology.drawio.png)


2. [Firefly III cleaner](https://github.com/anjimene7/firefly)

This little tool stems from the self-hosted [firefly iii](https://www.firefly-iii.org/) application, which is a an open source finance manager. It has very nice features of connecting directly to bank APIs to extract all transactions and process them in the application. However in my case I did not have such an option and have to rely on manual extractions of transaction data from my different accounts.

The goal in this case was to create a Docker application that would take as input the extract generated from the bank and output a curated file ready for ingestion into the application. 
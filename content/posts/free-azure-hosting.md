---
title: Free Azure Web Hosting
subtitle:
date: 2025-12-26T21:56:23Z
slug: free-azure-hosting
draft: false
author:
  name: TK
  link:
  email: tk@itmns.at
  avatar:
description:
keywords:
license:
comment: false
weight: 0
tags:
  - cheap
  - webhosting
categories:
  - azure
  - microsoft
hiddenFromHomePage: false
hiddenFromSearch: false
hiddenFromRelated: false
hiddenFromFeed: false
summary:
resources:
  - name: featured-image
    src: featured-image.jpg
  - name: featured-image-preview
    src: featured-image-preview.jpg
toc: true
math: false
lightgallery: false
password:
message:
repost:
  enable: true
  url:
---

There are a few ways to host content for free on Microsoft Azure.

<!--more-->

For small/personal use only of course. Anything commercial will quickly push past the free tiers of these services.

We are talking about static files or websites like this one (generated with Hugo or anything else like Next.JS).

## Azure Storage

An Azure Storage storage account can easily be used as a webserver by utilizing its web hosting feature.

> [!IMPORTANT]
> This method only delivers stuff over HTTP, not HTTPS via your custom domain name. So it fine for assets like JS, CSS or CRLs, but probalby not for a live site. For HTTPS you can use the Microsoft-Generated "mystorage.z49.web.core.windows.net"-Hostname


1. Create Storage Account:<br />![screenshot creating azure storage account](/img/free-azure-hosting/create-storage.png)<br />![screenshot creating azure storage account allow anonymous](/img/free-azure-hosting/create-storage-2.png)


1. Make sure it as a V2 account:<br /> ![v2](/img/free-azure-hosting/v2.png)

1. Disable "Secure Transfer Required"<br />![Disable "Secure Transfer Required"](/img/free-azure-hosting/sectrans.png)

1. Enable Static Website Feature<br />![enable static website feature](/img/free-azure-hosting/enable-static-webiste.png)


1. Create a CNAME for the hostname in your DNS Panel<br />![Note the hostname](/img/free-azure-hosting/hostname.png)

1. add custom domain to storage account:<br />![add custom domain to storage account](/img/free-azure-hosting/custdom.png)

1. upload content to $web blob container:<br />![upload content to web blob container](/img/free-azure-hosting/helloworld.png)

1. access via http://mycustomdomain.something:<br />![access via http://mycustomdomain.something](/img/free-azure-hosting/helloworld-2.png)



> [!TIP]
> This can also be used to easily publish the CRLs of your PKI (Public Key Infrastructure) to the internet.

## Azure Static Web App

coming soon...
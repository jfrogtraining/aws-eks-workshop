---
title: "Create Your EKS Cluster"
chapter: false
weight: 27
pre: "<b>2.7 </b>"
---

We will use the [EKSCTL command line tool](https://docs.aws.amazon.com/eks/latest/userguide/getting-started-eksctl.html) to create an [Amazon Elastic Kubernetes (EKS)](https://docs.aws.amazon.com/eks/latest/userguide/what-is-eks.html) cluster. This powerful tool allows you to manage many aspects of your EKS cluster through simple commands. When using EKSCTL, you can still manage your cluster in the Amazon EKS dashboard in the AWS console.

{{% notice info %}}
Amazon Elastic Kubernetes Service (Amazon EKS) is a managed service that you can use to run Kubernetes on AWS without needing to install, operate, and maintain your own Kubernetes control plane or nodes. Kubernetes is an open-source system for automating the deployment, scaling, and management of containerized applications. Amazon Elastic Kubernetes Service (Amazon EKS) gives you the flexibility to start, run, and scale Kubernetes applications in the AWS cloud or on-premises. Amazon EKS helps you provide highly-available and secure clusters and automates key tasks such as patching, node provisioning, and updates.
{{% /notice %}}

1. In your Cloud9 terminal, follow these [instructions](https://docs.aws.amazon.com/eks/latest/userguide/eksctl.html) to install EKSCTL on Linux.
2. In the **Container definition** section, click **Configure** on the **custom** option.
3. For the container name, specify ```npm-app```.
4. For the **Image** specify the Docker image name for our _npm-app_. This should be ```${domain}/docker-demo/npm-app:latest```. _domain_ is the JFrog Platform instance domain (_server name_.jfrog.io).
5. Check **Private repository autentication**.

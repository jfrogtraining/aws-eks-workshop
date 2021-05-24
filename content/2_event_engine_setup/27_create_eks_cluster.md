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
2. Follow these [instructions](https://docs.aws.amazon.com/eks/latest/userguide/install-kubectl.html) to install KUBECTL on Linux.
3. Next, execute the following command to create your EKS cluster. It is that easy! This will take a few minutes.
   
   ``
   eksctl create cluster --name jfrogeksworkshop --region us-west-2 --managed
   ``
   
4. Update your kubeconfig to add the credentials for your new cluster.
   
   ``
   aws eks update-kubeconfig --name jfrogeksworkshop --region us-west-2
   ``
   
5. Execute the following command to print out your kubeconfig. Copy the output to your notepad. We will need this later.
   
   ``
   cat /home/ec2-user/.kube/config
   ``

   ![Kubecobnfig](/images/kubeconfig.png)
   
6. Check **Private repository autentication**.

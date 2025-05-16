2025-05-16 09:38

### Status: #baby 

### Tags: [[data-engineering]] [[machine-learning]] [[AWS]] [[K8s]]

# What is Amazon EKS?

Amazon *Elasti K8s Service* provides a managed K8s service that help eliminate the operation of Kubernetes clusters so you are able then to
1. deploy faster
2. scale accordingly to workload
3. have better security
4. option to chose between standard EKS or fully automated EKS

There are two approaches:

- EKS standard: AWS will managed the [Kubernetes control plane](https://kubernetes.io/docs/concepts/overview/components/#control-plane-components) and will adjust nodes, schedule workload, AWS integration automatically.
- EKS Auto Mode: All of the above but also providing infrastructure, optimal compute instances, resource scalling, cost optimization.


![[Pasted image 20250516100049.png]]

## Pricing documentaion

Amazon EKS has per cluster pricing based on Kubernetes cluster version support, pricing for Amazon EKS Auto Mode, and per vCPU pricing for Amazon EKS Hybrid Nodes.

When using Amazon EKS, you pay separately for the AWS resources you use to run your applications on Kubernetes worker nodes. For example, if you are running Kubernetes worker nodes as Amazon EC2 instances with Amazon EBS volumes and public IPv4 addresses, you are charged for the instance capacity through Amazon EC2, the volume capacity through Amazon EBS, and the IPv4 address through Amazon VPC.

Visit the respective pricing pages of the AWS services you are using with your Kubernetes applications for detailed pricing information.

- For Amazon EKS cluster, Amazon EKS Auto Mode, and Amazon EKS Hybrid Nodes pricing, see [Amazon EKS Pricing](https://aws.amazon.com/eks/pricing/).
    
- For Amazon EC2 pricing, see [Amazon EC2 On-Demand Pricing](https://aws.amazon.com/ec2/pricing/on-demand/) and [Amazon EC2 Spot Pricing](https://aws.amazon.com/ec2/spot/pricing/).
    
- For AWS Fargate pricing, see [AWS Fargate Pricing](https://aws.amazon.com/fargate/pricing).
    
- You can use your savings plans for compute used in Amazon EKS clusters. For more information, see [Pricing with Savings Plans](https://aws.amazon.com/savingsplans/pricing/).
# References

[AWS Educate](https://kubernetes.io/docs/concepts/overview/components/#control-plane-components)









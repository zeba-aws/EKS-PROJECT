# EKS-PROJECT
Provisioned an Amazon EKS cluster, deployed a Kubernetes application, and exposed it to customers using an AWS Application Load Balancer integrated with EKS.
## STEPS ##
1.Provisioned and configured an Amazon EKS cluster using eksctl, including worker nodes and IAM roles.

2.Deployed a containerized game application to EKS using Kubernetes manifests (Deployments, Services).

3.Configured AWS Application Load Balancer (ALB) using the AWS Load Balancer Controller to expose the application to customers.

4.Implemented Ingress resources to route external traffic securely to Kubernetes services.

5.Managed IAM roles for service accounts (IRSA) to allow EKS components to interact securely with AWS services.

# First configured IAM OIDC Provider for allowing the ALB controller to use iam roles for service accounts

- oidc_id=$(aws eks describe-cluster --name $cluster_name --query "cluster.identity.oidc.issuer" --output text | cut -d '/' -f 5)

- eksctl utils associate-iam-oidc-provider --cluster $cluster_name --approve

  # steps to install ALB

1.create IAM policy:

curl -O https://raw.githubusercontent.com/kubernetes-sigs/aws-load-balancer-controller/v2.11.0/docs/install/iam_policy.json

aws iam create-policy \
    --policy-name AWSLoadBalancerControllerIAMPolicy \
    --policy-document file://iam_policy.json

2.create IAM role:

eksctl create iamserviceaccount 
--cluster=demo-cluster 
--namespace=kube-system   
--name=aws-load-balancer-controller   
--role-name AmazonEKSLoadBalancerControllerRole   
--attach-policy-arn=arn:aws:iam::your accountid:policy/AWSLoadBalancerControllerIAMPolicy   --approve

![eks 3](https://github.com/user-attachments/assets/95fbf61c-5048-47e9-ba68-fa7a4270da94)

# Used Helm to install the AWS Load Balancer Controller.

curl https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-4 | bash

# Add helm repo

helm repo add eks https://aws.github.io/eks-charts

# Install ALB

helm install aws-load-balancer-controller eks/aws-load-balancer-controller -n kube-system \
  --set clusterName=demo-cluster \
  --set serviceAccount.create=false \
  --set serviceAccount.name=aws-load-balancer-controller \
  --set region=ap-south-1 \
  --set vpcId=vpc-08954d2164eec6298

# TO verify deployement

kubectl get deployment -n kube-system aws-load-balancer-controller

![eks4](https://github.com/user-attachments/assets/ec6ae435-cd58-4592-a84c-5bcc2bb1de2f)

![eks5](https://github.com/user-attachments/assets/aed47151-43a3-4f7f-bec2-c3192ad464dd) 

# Copy the ALB DNS name and check it in the browser

![eks6](https://github.com/user-attachments/assets/46da393e-a4c7-4e46-837b-c403f5a7af6e)

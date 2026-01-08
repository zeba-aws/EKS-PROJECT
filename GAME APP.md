# Create fargate profile 

eksctl create fargateprofile     --cluster demo-cluster     --region ap-south-1     --name alb-sample-app     --namespace game-2048

# Deploy the deployemant,service and ingress 

kubectl apply -f https://raw.githubusercontent.com/kubernetes-sigs/aws-load-balancer-controller/v2.5.4/docs/examples/2048/2048_full.yaml 

 create the following

kubectl get pods -n game-2048(shows the pods running)


kubectl get svc -n game-2048(Shows the service created)


kubectl get ingress -n game-2048 (shows the ingress resource created)

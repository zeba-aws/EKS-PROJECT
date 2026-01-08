## Installed the following command line tools on linux ec2 instance # 
1.AWS CLI – A command line tool for working with AWS services.

curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"

unzip awscliv2.zip

sudo ./aws/install

aws configure # pass the acess key and secret key #

 2.kubectl – A command line tool for working with Kubernetes clusters.
 
sudo yum install -y kubectl 

 3. eksctl – A command line tool for working with EKS clusters

curl --silent --location "github.com(uname -s)_amd64.tar.gz" | tar xz -C /tmp

sudo mv /tmp/eksctl /usr/local/bin  ## To move eksctl to this directory path 





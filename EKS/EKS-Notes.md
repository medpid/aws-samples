# EKSCTL - is a new tool that can be used to manage AWS EKS service.

**https://eksctl.io/introduction/#installation**

**Documentatoin for EKS Cluster using eksctl**

```
https://learn.acloud.guru/handson/f41da9b7-8408-4499-a605-e4e6870a554f
```

```
curl --silent --location "https://github.com/weaveworks/eksctl/releases/latest/download/eksctl_$(uname -s)_amd64.tar.gz" | tar xz -C /tmp
sudo mv /tmp/eksctl /usr/local/bin
```

**Bash**

To enable bash completion, run the following, or put it in ~/.bashrc or ~/.profile:
```
. <(eksctl completion bash)
```

**Examples**

https://github.com/weaveworks/eksctl/tree/main/examples


# Install kubectl

https://docs.aws.amazon.com/eks/latest/userguide/install-kubectl.html

```
curl -o kubectl https://amazon-eks.s3.us-west-2.amazonaws.com/1.21.2/2021-07-05/bin/linux/amd64/kubectl

chmod +x ./kubectl

mkdir -p $HOME/bin && cp ./kubectl $HOME/bin/kubectl && export PATH=$PATH:$HOME/bin

echo 'export PATH=$PATH:$HOME/bin' >> ~/.bashrc

kubectl version --short --client
```
**Help/Commands**  

https://kubernetes.io/docs/reference/kubectl/cheatsheet/

https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands 



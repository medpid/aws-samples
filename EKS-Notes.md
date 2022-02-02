EKSCTL - is a new tool that can be used to manage AWS EKS service.

https://eksctl.io/introduction/#installation

```
curl --silent --location "https://github.com/weaveworks/eksctl/releases/latest/download/eksctl_$(uname -s)_amd64.tar.gz" | tar xz -C /tmp
sudo mv /tmp/eksctl /usr/local/bin
```

Bash
To enable bash completion, run the following, or put it in ~/.bashrc or ~/.profile:
```
. <(eksctl completion bash)
```

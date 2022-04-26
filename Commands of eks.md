# Commands of eks

## Download eksctl
```
curl --silent --location "https://github.com/weaveworks/eksctl/releases/latest/download/eksctl_$(uname -s)_amd64.tar.gz" | tar xz -C /tmp
```

## Create cluster with Managed nodes 
```
eksctl create cluster --name eks-clusterr --region us-east-1
```
## Create cluster with fargate
```
eksctl create cluster --name my-cluster --region region-code --fargate
```

## Kubeconfig file
```
aws eks update-kubeconfig --region us-east-1 --name eks-clusterr
```

## Delete cluster
```
eksctl delete cluster --name eks-clusterr --region us-east-1
```



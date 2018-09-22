# dockerfile-for-k8s

```
将使用 Kubespray 2.6.0 安装 Kubernetes 1.10.4 所依赖的来自 gcr.io 等国内无法访问的 Docker 镜像，通过 DockerHub 自动构建在自己的命名空间下 `waychan23`。
通过修改 kuberspray 中的镜像引用，将其指向 DockerHub 上 `waychan23` 命名空间下的对应镜像，可以在不翻墙的条件下使用 Kubespray 安装 Kubernetes 集群。
```

## Docker Image List

1. `waychan23/pause:3.1` == `k8s.gcr.io/pause:3.1` 
2. `waychan23/k8s-dns-kube-dns-amd64:1.14.11` == `gcr.io/google_containers/k8s-dns-kube-dns-amd64:1.14.11`
3. `waychan23/k8s-dns-sidecar-amd64:1.14.11` == `gcr.io/google_containers/k8s-dns-sidecar-amd64/tags/1.14.11`
4. `waychan23/k8s-dns-dnsmasq-nanny-amd64:1.14.11` == `gcr.io/google_containers/k8s-dns-dnsmasq-nanny-amd64:1.14.11`
5. []`waychan23/coredns:1.2.2` == `gcr.io/google-containers/coredns:1.2.2`
6. []`waychan23/cluster-proportional-autoscaler-amd64:1.1.2` == `gcr.io/google_containers/cluster-proportional-autoscaler-amd64:1.1.2`
7. []`waychan23/tiller:v2.9.1` == `gcr.io/kubernetes-helm/tiller:v2.9.1`
8. []`waychan23/kube-registry-proxy:0.4` == `gcr.io/google_containers/kube-registry-proxy:0.4`
9. []`waychan23/defaultbackend` == `gcr.io/google_containers/defaultbackend:1.4`
10. []`waychan23/kubernetes-dashboard-amd64:v1.10.0` == `gcr.io/google_containers/kubernetes-dashboard-amd64:v1.10.0`
11. []`waychan23/nvidia-gpu-device-plugin@sha256:0842734032018be107fa2490c98156992911e3e1f2a21e059ff0105b07dd8e9e` == `k8s.gcr.io/nvidia-gpu-device-plugin@sha256:0842734032018be107fa2490c98156992911e3e1f2a21e059ff0105b07dd8e9e`
12. []`waychan23/google-containers/pause:2.0` == `gcr.io/google-containers/pause:2.0`
13. []`waychan23/ubuntu-nvidia-driver-installer@sha256:eea7309dc4fa4a5c9d716157e74b90826e0a853aa26c7219db4710ddcd1ad8bc` == `gcr.io/google-containers/ubuntu-nvidia-driver-installer@sha256:eea7309dc4fa4a5c9d716157e74b90826e0a853aa26c7219db4710ddcd1ad8bc`
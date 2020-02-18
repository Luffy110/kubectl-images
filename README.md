<h1 align="center">kubectl-images</h1>

<p align="center">
  <em>🕸 show container images used in the cluster.</em>
</p>

### 🔰 Installation

Bulid from source code
```shell
$ git clone https://github.com/chenjiandongx/kubectl-images.git
$ cd kubectl-images && go build -ldflags="-s -w" -o kubectl-images . && mv ./kubectl-images /usr/local/bin
$ kubectl images --help
```

Download the binary
```shell
export VERSION=0.1.0

# Linux
$ curl -Lo kubectl-images https://github.com/chenjiandongx/kubectl-images/releases/download/v${VERSION}/kubectl-images_linux_amd64
# MacOS
$ curl -Lo kubectl-images https://github.com/chenjiandongx/kubectl-images/releases/download/v${VERSION}/kubectl-images_darwin_amd64
# Windows
$ curl -Lo kubectl-images https://github.com/chenjiandongx/kubectl-images/releases/download/v${VERSION}/kubectl-images_windows_amd64

$ chmod +x kubectl-images && mv kubectl-images /usr/local/bin/
$ kubectl images --help
```

### 📝 Usage

```shell
~ 🐶 kubectl images --help
Show container images used in the cluster.

Usage:
  kubectl-images [podname-regex] [flags]

Examples:
  # display a table of all images in current namespace using podName/containerName/containerImage as columns.
  kubectl images

  # display a table of images that match 'nginx' podname regex in 'dev' namespace using podName/containerImage as columns.
  kubectl images -n dev nginx -c 1,2

Flags:
  -A, --all-namespaces     if present, list images in all namespaces.
  -c, --columns string     specify the columns to display, separated by comma. [0:Namespace, 1:PodName, 2:ContainerName, 3:ContainerImage] (default "1,2,3")
  -h, --help               help for kubectl-image
  -n, --namespace string   if present, list images in the specified namespace only. Use current namespace as fallback.
      --version            version for kubectl-image
```

### 🔖 Glances

![image](https://user-images.githubusercontent.com/19553554/74601790-d54f6980-50dc-11ea-90d6-004650d5ed2f.jpg)
![image](https://user-images.githubusercontent.com/19553554/74601792-de403b00-50dc-11ea-9a26-a354668b8195.jpg)

### 📃 License

MIT [©chenjiandongx](https://github.com/chenjiandongx)

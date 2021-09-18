---
name: Local Setup
layout: post
title: How to install minikube on MacOS
---

### MacOS

##### Minikube

```
$ brew install minikube

# Start minikube
$ minikube start

# Start K8s dashboard
$ minikube dashboard

# Stop minikube
$ minikube stop

```

For more details refer to [minikube](https://minikube.sigs.k8s.io/docs/start/){:target="_blank"} documentation.

**Must Read Sections**
* [Host access](https://minikube.sigs.k8s.io/docs/handbook/host-access/){:target="_blank"}
> localhost MUST be replaced with host.minikube.internal to access services running on the local machine. However, if 
> the container application is still not able to access then replace the same with minikube VM IP address. This can be 
> obtained using **minikube ip** Incorrect copy of /etc/hosts from host machine to minikube VM might be reason. Need to
> read up more on this.

* [Mounting filesystems](https://minikube.sigs.k8s.io/docs/handbook/mount/){:target="_blank"}

* [Pushing images](https://minikube.sigs.k8s.io/docs/handbook/pushing/){:target="_blank"}
> Keep in mind Tip 1, 2 and 3 mentioned in the above link. Below is the command to point your terminal to use the docker 
> daemon inside minikube
```
$ eval $(minikube docker-env)
```

##### kubectl

```
$ brew install kubectl
```

* Shell Autocompletion
```
source <(kubectl completion zsh)  # setup autocomplete in zsh into the current shell
echo "[[ $commands[kubectl] ]] && source <(kubectl completion zsh)" >> ~/.zshrc # add autocomplete permanently to your zsh shell
```

* [kubectl cheat sheet](https://kubernetes.io/docs/reference/kubectl/cheatsheet/){:target="_blank"}

* [kubectl command reference](https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands#-strong-getting-started-strong-){:target="_blank"}
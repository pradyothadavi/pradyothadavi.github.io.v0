# Kubernetes Intermediate Training

https://kubeweekly.io

https://www.meetup.com/k8s-cloudnative-online/

https://www.linkedin.com/in/neependra

# 9th Sept


## Exam
 - Sign-up
     - https://cloudyuga.guru/courses/ckad-cka-mock
     - coupon code FMOCK1
     - Go to Mycources
     - Access Mock Exam
     - Setup Exam
     - wait for 15 mins
     - launch exam
    



## Links
- https://kubernetes.io/docs/setup/production-environment/tools/kubeadm/create-cluster-kubeadm/
- https://cloudyuga.guru/blog/single-master-setup-kubeadm
- https://speakerdeck.com/thockin/kubernetes-and-networks-why-is-this-so-dang-hard
- https://aws.github.io/aws-controllers-k8s/


## Commands
```
kubectl port-forward pod/nginx-deploy-678645bf77-njhmh 9000:80
```


# 8th Sept
https://docs.docker.com/compose/wordpress/

```
docker-compose up
```

## Course Signup
- https://cloudyuga.guru/courses/intermediate-k8s-fk
    - Use coupon code "FKK8S" to enroll for free 

### Commands

```
mkdir ~/.kube
vim ~/.kube/config-fk
```

```
apiVersion: v1
clusters:
- cluster:
    certificate-authority-data: LS0tLS1CRUdJTiBDRVJUSUZJQ0FURS0tLS0tCk1JSURKekNDQWcrZ0F3SUJBZ0lDQm5Vd0RRWUpLb1pJaHZjTkFRRUxCUUF3TXpFVk1CTUdBMVVFQ2hNTVJHbG4KYVhSaGJFOWpaV0Z1TVJvd0dBWURWUVFERXhGck9ITmhZWE1nUTJ4MWMzUmxjaUJEUVRBZUZ3MHlNREE1TURndwpOREl5TlRoYUZ3MDBNREE1TURnd05ESXlOVGhhTURNeEZUQVRCZ05WQkFvVERFUnBaMmwwWVd4UFkyVmhiakVhCk1CZ0dBMVVFQXhNUmF6aHpZV0Z6SUVOc2RYTjBaWElnUTBFd2dnRWlNQTBHQ1NxR1NJYjNEUUVCQVFVQUE0SUIKRHdBd2dnRUtBb0lCQVFEcDIxQm1QeFR2Zm9TdmRocU9pNlIxcUtaOWtoc0N5ckloL0VVeUtkYlJxdjRKNjltegp4WXlPWDA4aFluVlcrN0RxVWIzMWJlK1lQYjY5SUdxZlRPNGk0ZzcxcHdnTlhBWFJqbDZHR3diNllwYjlQOGtECktZR01lODM3WlIvczB5WmxaR2JYS1B1VHEwK3o5S0ZwRkF4d2Q1bklyZVRlTDRzY0l5T2RrdlBPZkF2RkxZbWkKNTZ0MHR1SExydS9aNkx4aWY2aVN6WDNvSXlQdXRKdkNXMzJVQy9ZZGN0UFRERGJ1VDZyOE5nUkliUXowd1JiWAo4b1lFSENoS01VQklicG4xNHZvdGwwNGFnR3VyZzFUaHBVTkZ6allYbHVqeWRXODY5T2p6RHk3NXU3M0dhcDFSClJqckg1SkVnWlRUQndYMDRBQnRlMVBuK21OS0Qvbms1U1NvRkFnTUJBQUdqUlRCRE1BNEdBMVVkRHdFQi93UUUKQXdJQmhqQVNCZ05WSFJNQkFmOEVDREFHQVFIL0FnRUFNQjBHQTFVZERnUVdCQlJKS0NmM0Y5eDM1akNKTWJzdQpHYmZxUCtjNU1UQU5CZ2txaGtpRzl3MEJBUXNGQUFPQ0FRRUF4V0RBMUJSbE1rVHVYazFNTnpqQlZ0MnRVSEZzCm9hZWNTZlJjb2VQMnlNblZ1VHRQMjJidDZhSzV5OStJV0FiMktIWS9rc3NFa0NMODQzRk5HM0grMG9lMFF4cXQKdWMzbUQzNXVWUnFWR09LUVIrTk84UlJSMEE3OFpmbnZGSUpKVURyRDVjcXM2RWtkS2RwNno4UU1pdWdYaGdzMgpSeUczSWVJdjVGSHlMaHM5bzJVQTUzdktxMjJmNzVwYllOTksvdXBoQmtpYXhHcGV2citaRW5PaXA4RHNESnMrCm1uMlpKU1hkaUpMRmM3Z3lreEluY2tjZ0J6NnBOWG52M1J0NXNQYjlNQjYrOC9aODlnYkJmOEJVYUppRTVvWU8KcTFQdTdCL0h3SGZLMjErd1FGOVBubm5NcVdGTGZFZWtRSTdtdm1GSHM5ZDYwNWg4SDh0N2NNZy9Ndz09Ci0tLS0tRU5EIENFUlRJRklDQVRFLS0tLS0K
    server: https://33e4a5d3-60f0-4adb-a543-59730098e573.k8s.ondigitalocean.com
  name: do-blr1-k8s-fk
contexts:
- context:
    cluster: do-blr1-k8s-fk
    user: do-blr1-k8s-fk-admin
  name: do-blr1-k8s-fk
current-context: do-blr1-k8s-fk
kind: Config
preferences: {}
users:
- name: do-blr1-k8s-fk-admin
  user:
    token: 918fd00380ad46cc53da973dff6d404c5235cced3844278f0b30f9257e784544
```

```
export KUBECONFIG=~/.kube/config-fk
kubectl get nodes

```


```
apiVersion: v1
kind: Pod
metadata:
 name: mypod
spec:
 containers:
 - name: myc
   image: nginx:alpine
```
```

$  kubectl  create -f pod.yaml
$ kubectl create namespace nkhare
$ kubectl create -f pod.yaml -n nkhare
$ kubectl describe pod mypod -n nkhare
```

```
 kubectl get nodes -o wi
 ```


https://github.com/cloudyuga/rsvpapp


$ cp configs/5-config.yaml configs/6-rsvpconfig.yaml configs/7-backe
nd.yaml  ~/


https://docs.docker.com/compose/wordpress/

# 7th Sept
## Signup for Cloudyga

- Create an account at https://cloudyuga.guru
- Attempt Pre-tests
    - https://cloudyuga.guru/site_quizzes/basic-containers-docker
    - https://cloudyuga.guru/site_quizzes/basic-kubernetes
- Sign up for the Docker Course 
    - https://cloudyuga.guru/courses/container-fundamentals-with-docker
    - Use coupon code "FKDOCKER" to enroll for free 

## Commands

```
 sudo apt update
 sudo apt install docker.io
```

```
 sudo docker container ls
```

```
 sudo docker container run -i -t alpine sh
 ```
 
 ```
  sudo docker container ls
  sudo docker container ls -a
  sudo docker container run --name web -d nginx:alpine
    sudo docker container inspect web
  ```
 
 ```
  sudo docker container run -i -t --name myalpine alpine sh
  
  Ctrl + p + q
  ```
  ```
  sudo docker container diff myalpine
  sudo docker container commit myalpine  myimage  
   sudo docker container run -i -t myimage:latest sh
  ```
  
  
 ```
 mkdir workshop
 cd workshop 
 cat Dockerfile
 $ cat Dockerfile
   FROM alpine:latest
   RUN date > file
 ```
 
```
 sudo docker image build -t myimage:dockerfile .
 ```
 
 ```
 mkdir src
 touch src/f1

 $ cat Dockerfile
 FROM alpine:latest
RUN date > file
COPY src /tmp
 ```
 
 https://docs.docker.com/engine/reference/builder/
 
```
 $ cat Dockerfile
FROM alpine:latest
RUN date > file
COPY src /tmp
CMD ["/bin/ls", "/tmp"]
```

```
 cat Dockerfile
FROM alpine:latest
RUN date > file
COPY src /tmp
ENTRYPOINT ["/bin/ls", "/tmp"]
```


```
 sudo docker network create myn
```

```
$ sudo docker container run -d --net=mynet --name=backend  nginx:alpine
```

```
$sudo docker container run -d -p 8080:80 nginx
```

```
docker container run  -it -v /data --name volc alpine sh
docker volume creare myvol

```

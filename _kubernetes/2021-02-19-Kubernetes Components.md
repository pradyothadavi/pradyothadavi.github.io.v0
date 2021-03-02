---
name: Kubernetes Components
layout: post
---

There are two components of a Kubernetes Cluster
* Control Plane Components
* Node Components

![k8 cluster](https://d33wubrfki0l68.cloudfront.net/2475489eaf20163ec0f54ddc1d92aa8d4c87c96b/e7c81/images/docs/components-of-kubernetes.svg)
*Reference: https://kubernetes.io/docs/concepts/overview/components/*


### Control Plane Components
The control plane components make global decisions about the cluster, as well as detecting and responding to cluster 
events. 

<table class="table table-dark">
  <thead>
    <tr>
      <th scope="col">#</th>
      <th scope="col">Component</th>
      <th scope="col">Responsibility</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">1</th>
      <td>kube-apiserver</td>
      <td>Exposes the Kubernetes API</td>
    </tr>
    <tr>
      <th scope="row">2</th>
      <td>etcd</td>
      <td>Consistent and highly-available key value store for storing all cluster data</td>
    </tr>
    <tr>
      <th scope="row">3</th>
      <td>kube-scheduler</td>
      <td><li>selects node to run Pods</li><li>watches for newly created Pods</li></td>
    </tr>
    <tr>
      <th scope="row">4</th>
      <td>kube-controller-manager</td>
      <td>
        <li>It runs different controller processes</li>
        <li>Node controller</li>
        <li>Job controller</li>
        <li>Endpoints controller</li>
        <li>Service Account & Token controllers</li>
       </td>
    </tr>
    <tr>
      <th scope="row">5</th>
      <td>cloud-controller-manager</td>
      <td>
        <li>It contains cloud provider specific control logic</li>
        <li>Applications like minikube which are used for local setup will not have this component</li>
       </td>
    </tr>
  </tbody>
</table>



### Node Components

<table class="table table-dark">
  <thead>
    <tr>
      <th scope="col">#</th>
      <th scope="col">Component</th>
      <th scope="col">Responsibility</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">1</th>
      <td>kubelet</td>
      <td>Ensures that containers are running in a pod, on each node of the cluster</td>
    </tr>
    <tr>
      <th scope="row">2</th>
      <td>kube-proxy</td>
      <td>It maintains the network rules on the nodes of the cluster</td>
    </tr>
    <tr>
      <th scope="row">3</th>
      <td>container-runtime</td>
      <td>software application responsible for running the containers</td>
    </tr>
    <tr>
      <th scope="row">4</th>
      <td>Addons</td>
      <td>
        <li>DNS</li>
        <li>Web UI</li>
        <li>Container Resource Monitoring</li>
       </td>
    </tr>
  </tbody>
</table>



---
name: Kubernetes Components
layout: post
---

There are two components of a Kubernetes Cluster
* Control Plane Components
* Node Components

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
      <td><li>selects node to run Pods</li><li>watches for newly created Pods</li></td>
    </tr>
    <tr>
      <th scope="row">5</th>
      <td>cloud-controller-manager</td>
      <td><li>selects node to run Pods</li><li>watches for newly created Pods</li></td>
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
      <td>Exposes the Kubernetes API</td>
    </tr>
    <tr>
      <th scope="row">2</th>
      <td>kube-proxy</td>
      <td>Consistent and highly-available key value store for storing all cluster data</td>
    </tr>
    <tr>
      <th scope="row">3</th>
      <td>container-runtime</td>
      <td><li>selects node to run Pods</li><li>watches for newly created Pods</li></td>
    </tr>
    <tr>
      <th scope="row">4</th>
      <td>Addons</td>
      <td><li>DNS</li><li>Web UI</li><li>Container Resource Monitoring</li></td>
    </tr>
  </tbody>
</table>


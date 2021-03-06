# Kubernetes Certified Administration

Online resources that will help you prepare for taking the Kubernetes Certified Administrator Certification exam.
Disclaimer: This is not likely the comprehensive timely updated complete list as the exam will be a moving target withthe fast pace of k8s development - please make a pull request if there something wrong or that should be added, or updated in here.

I tried to restrict the cross references of resources to Kuberntes.io. youtube videos and other blog resources are optional, however, I still them useful in my k8s learning journey.
 
Ensure you have the right version of kubernetes documentation selected (e.g. v1.6.2 for the current exam) espically for API objects and annottations. 

## Exam Objectives

These are the exam objectives you review and understand in order to pass the test. The objectives are current as of September 15, 2017.

* [CNCF Exam Curriculum repository ](https://github.com/cncf/curriculum)

### [Core Concepts](https://v1-6.docs.kubernetes.io/docs/concepts/) 19%
* [Understand the Kubernetes API primitives](https://v1-6.docs.kubernetes.io/docs/api-reference/v1.6/)

  * [concepts: Kubernetes Objects](https://kubernetes.io/docs/concepts/overview/working-with-objects/kubernetes-objects/)
  * youtube: [Kubernetes Webinar Series - Kubernetes Architecture 101](https://www.youtube.com/watch?v=zeS6OyDoy78)
  
* [Understand the Kubernetes cluster architecture](https://kubernetes.io/docs/concepts/overview/components/)
  
  youtube: [A Technical Overview of Kubernetes (CoreOS Fest 2015) by Brendan Burns](https://www.youtube.com/watch?v=WwBdNXt6wO4)
  

* [Understand Services and other network primitives](https://kubernetes.io/docs/concepts/services-networking/service/)

  * youtube: [Life of a Packet [I] - Michael Rubin, Google](https://www.youtube.com/watch?v=0Omvgd7Hg1I)
  * youtube: [The ins and outs of networking in Google Container Engine and Kubernetes (Google Cloud Next '17)](https://www.youtube.com/watch?v=y2bhV81MfKQ)

### [Installation, Configuration and Validation](https://github.com/kelseyhightower/kubernetes-the-hard-way/tree/f9486b081f8f54dd63a891463f0b0e783d084307) 12%
* [Design a Kubernetes cluster]
* [Install Kubernetes masters and nodes](https://kubernetes.io/docs/getting-started-guides/scratch/)
* [Configure secure cluster communications](https://kubernetes.io/docs/tasks/tls/managing-tls-in-a-cluster/)
* [Configure a Highly-Available Kubernetes cluster](https://kubernetes.io/docs/admin/high-availability/)
* [Know where to get the Kubernetes release binaries](https://kubernetes.io/docs/getting-started-guides/binary_release/#prebuilt-binary-release)
* [Provision underlying infrastructure to deploy a Kubernetes cluster](https://github.com/kelseyhightower/kubernetes-the-hard-way/blob/f9486b081f8f54dd63a891463f0b0e783d084307/docs/01-infrastructure-gcp.md)
* [Choose a network solution](https://kubernetes.io/docs/getting-started-guides/scratch/#network)
* [Choose your Kubernetes infrastructure configuration]
* [Run end-to-end tests on your  cluster]
```
  	$kubectl cluster-info
  	$kubectl get nodes
  	$kubectl get pods -o wide --show-labels --all-namespaces
        $kubectl get svc  -o wide --show-labels --all-namespaces
```

  run a simple deployment, check out https://kubernetes.io/docs/tutorials/ 

* [Analyse end-to-end tests results]
* [Run Node end-to-end tests]



### Security 12%
* [Know how to configure authentication and authorization](https://kubernetes.io/docs/admin/authorization/rbac/)
* [Understand Kubernetes security primitives]
* [Know to configure network policies](https://kubernetes.io/docs/tasks/administer-cluster/declare-network-policy/)
  * [Blog: Kubernetes network policy](https://ahmet.im/blog/kubernetes-network-policy/)
* [Create and manage TLS certificates for cluster components](https://kubernetes.io/docs/tasks/tls/managing-tls-in-a-cluster/)
* [Work with images securely]
* [Define security contexts](https://kubernetes.io/docs/tasks/configure-pod-container/security-context/)
* [Secure persistent key value store](https://kubernetes.io/docs/concepts/configuration/secret/)


### [Networking](https://kubernetes.io/docs/concepts/cluster-administration/networking/) 11%
* [Understand the networking configuration on the cluster nodes](https://kubernetes.io/docs/concepts/cluster-administration/networking/)
* [Understand Pod networking concepts]
  * youtube: [The ins and outs of networking in Google Container Engine and Kubernetes (Google Cloud Next '17)](https://www.youtube.com/watch?v=y2bhV81MfKQ)

* [Understand service networking]
  * youtube: [Life of a Packet [I] - Michael Rubin, Google](https://www.youtube.com/watch?v=0Omvgd7Hg1I)
* [Deploy and configure network load balancer](https://kubernetes.io/docs/tasks/access-application-cluster/create-external-load-balancer/)
* [Know how to use Ingress rules](https://kubernetes.io/docs/concepts/services-networking/ingress/)
* [Know how to configure and use the cluster DNS](https://kubernetes.io/docs/tasks/access-application-cluster/create-external-load-balancer/)
* [Understand CNI](https://kubernetes.io/docs/tasks/access-application-cluster/create-external-load-balancer/)

### Cluster Maintenance 11%
* [Understand Kubernetes cluster upgrade process]
* [Facilitate operating system upgrades]
* [Implement backup and restore methodologies](


### [Troubleshooting](https://kubernetes.io/docs/tasks/debug-application-cluster/troubleshooting/) 10%
* [Troubleshoot application failure](https://kubernetes.io/docs/tasks/debug-application-cluster/determine-reason-pod-failure/)
  * [Application Introspection and Debugging](https://kubernetes.io/docs/tasks/debug-application-cluster/debug-application-introspection/)
* [Troubleshoot control plane failure]
  * youtube [Kubernetes Day 2: Cluster Operations [I] - Brandon Philips, CoreOS](https://www.youtube.com/watch?v=U1zR0eDQRYQ)
  * Safaribooksonline: [https://www.safaribooksonline.com/library/view/oscon-2016-video/9781491965153/video246982.html](https://www.safaribooksonline.com/library/view/oscon-2016-video/9781491965153/video246982.html)
* [Troubleshoot worker node failure]
* [Troubleshoot networking]




### Storage 7%
* [Understand persistent volumes and know how to create them.
* [Understand access modes for volumes.
* [Understand persistent volume claims primitive.
* [Understand Kubernetes storage objects.
* [Know how to configure applications with persistent storage.



### Application Lifecycle Management 8%
* Understand Deployments and how to perform rolling updates and rollbacks.
* Know various ways to configure applications.
* Know how to scale applications.
* Understand the primitives necessary to create a self-healing application.


### Scheduling  5%
* [Use label selectors to schedule Pods](https://kubernetes.io/docs/concepts/overview/working-with-objects/labels/)
* [Understand the role of DaemonSets](https://kubernetes.io/docs/concepts/workloads/controllers/daemonset/)
* [Understand how resource limits can affect Pod scheduling](https://kubernetes.io/docs/tasks/administer-cluster/memory-default-namespace/)
* [Understand how to run multiple schedulers and how to configure Pods to use them](https://kubernetes.io/docs/tasks/administer-cluster/configure-multiple-schedulers/)
* [Manually schedule a pod without a scheduler](https://kubernetes.io/docs/tasks/administer-cluster/static-pod/)
   If you require a pod to start on a specific node, you can specify this in POD spec.nodeName, that is what DaemonSets do.
* [Display scheduler events](https://stackoverflow.com/questions/28857993/how-does-kubernetes-scheduler-work/28874577#28874577)
  /var/log/kube-scheduler.log on the control/master node
  or use `kubectl describe` as in
``` 
  $kubectl describe pods <POD NAME UNDER Investigation>  | grep -A7 ^Events
```
* [Know how to configure the Kubernetes scheduler]


## [Logging/Monitoring](https://kubernetes.io/docs/concepts/cluster-administration/logging/)  5%
* [Understand how to monitor all cluster components](https://kubernetes.io/docs/tasks/debug-application-cluster/resource-usage-monitoring/)
* [Understand how to monitor applications]
* Manage cluster component logs
  * Master
    * /var/log/kube-apiserver.log - API Server, responsible for serving the API
    * /var/log/kube-scheduler.log - Scheduler, responsible for making scheduling decisions
    * /var/log/kube-controller-manager.log - Controller that manages replication controllers
  * Worker Nodes
    * /var/log/kubelet.log - Kubelet, responsible for running containers on the node
    * /var/log/kube-proxy.log - Kube Proxy, responsible for service load balancing

* [Manage application logs](https://kubernetes.io/docs/user-guide/kubectl/v1.6/#logs)


## Tips:

get familiar with:
* [kubectl explain](https://blog.heptio.com/kubectl-explain-heptioprotip-ee883992a243)
* [kubectl cheatsheet](https://kubernetes.io/docs/user-guide/kubectl-cheatsheet/)
* When using kubecctl for investigations and troubleshooting utilize the wide output it gives your more details
```
     $kubectl get pods -o wide --show-labels --all-namespaces
```
* In `kubectl` utilizie `--all-namespaces` to ensure deployments, pods, objects are on the right name space, and right desired state

* for events and troubleshooting utilize kubectl describe
```
     $kubectl describe pods <PODID>
```
* the '-o yaml' in conjuction with `--dry-run` allows you to create a manifest template from an imperative spec, combined with `--edit` it allows you to modify the object before creation
```
kubectl create service clusterip my-svc -o yaml --dry-run > /tmp/srv.yaml
kubectl create --edit -f /tmp/srv.yaml
```


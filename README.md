<h1 align="center">
  <br>
  <a href="https://kubernetes.io/"><img src="https://avatars1.githubusercontent.com/u/13629408?s=400&v=4" alt="Markdownify" width="200"></a>
  <br>
  Kubernetes
  <br>
</h1>

[![Submit Queue Widget]][Submit Queue] [![GoDoc Widget]][GoDoc] [![CII Best Practices](https://bestpractices.coreinfrastructure.org/projects/569/badge)](https://bestpractices.coreinfrastructure.org/projects/569)

## 🚩 Table of Contents

- [1.Introduction to Kubernetes](1.Introduction%20to%20Kubernetes.md)
  - [Environment](1.Introduction%20to%20Kubernetes.md#environment)
  - [Minikube](1.Introduction%20to%20Kubernetes.md#minikube-overview)
    - [Install kubectl](1.Introduction%20to%20Kubernetes.md#install-kubectl)
    - [Install minikube](1.Introduction%20to%20Kubernetes.md#install-minikube)
    - [Basic minikube commands](1.Introduction%20to%20Kubernetes.md#basic-minikube-commands)
  - [Your First K8S App](1.Introduction%20to%20Kubernetes.md#your-first-k8s-app)
  - [Basic kubectl commands](1.Introduction%20to%20Kubernetes.md#basic-kubectl-commands)
- [2.Basic and Core Concepts](2.Basic%20and%20Core%20Concepts.md)
  - [Scaling Kubernetes](2.Basic%20and%20Core%20Concepts.md#scaling-kubernetes)
  - [Kubernetes Deployment](2.Basic%20and%20Core%20Concepts.md#kubernetes-deployment)
  - [Labels and Selectors](2.Basic%20and%20Core%20Concepts.md#labels-and-selectors)
  - [Health Checks](2.Basic%20and%20Core%20Concepts.md#health-checks)
  - [Web Interface](2.Basic%20and%20Core%20Concepts.md#web-interface)
    - [Kubernetes Web UI](2.Basic%20and%20Core%20Concepts.md#kubernetes-web-ui)
    - [Using The Web UI](2.Basic%20and%20Core%20Concepts.md#using-the-web-ui)
- [3.Advanced - DNS and Service Discovery](3.Advanced%20-%20DNS%20and%20Service%20Discovery.md)
    - [Practical Example](A3.dvanced%20-%20DNS%20and%20Service%20Discovery.md#practical-example)
      - [MySQL](3.Advanced%20-%20DNS%20and%20Service%20Discovery.md#mysql)
      - [WordPress](3.Advanced%20-%20DNS%20and%20Service%20Discovery.md#wordpress)
    - [Deploy MySQL](3.Advanced%20-%20DNS%20and%20Service%20Discovery.md#deploy-mysql)
    - [Deploy WordPress](3.Advanced%20-%20DNS%20and%20Service%20Discovery.md#deploy-wordpress)
- [4.Advanced - Volumes](4.Advanced%20-%20Volumes.md)
    - [Introduction](4.Advanced%20-%20Volumes.md#introduction)
    - [Volumes](4.Advanced%20-%20Volumes.md#volumes)
      - [Using Volumes](4.Advanced%20-%20Volumes.md#using-volumes)
      - [Using PersistentVolumes](4.Advanced%20-%20Volumes.md#using-persistentvolumes)
      - [Creating A Volume](4.Advanced%20-%20Volumes.md#creating-a-volume)
      - [Claiming A Volume](4.Advanced%20-%20Volumes.md#claiming-a-volume)
    - [YAML Files Explanation](4.Advanced%20-%20Volumes.md#yaml-files-explanation)
    - [Practical Example](4.Advanced%20-%20Volumes.md#practical-example)
- [5.Advanced - Secrets](5.Advanced%20-%20Secrets.md)
    - [Introduction](5.Advanced%20-%20Secrets.md#introduction)
    - [Secrets](5.Advanced%20-%20Secrets.md#secrets)
    - [Creating A Secret](5.Advanced%20-%20Secrets.md#creating-a-secret)
    - [Using A Secret - As an environment variable](5.Advanced%20-%20Secrets.md#using-a-secret---as-an-environment-variable)
    - [Using A Secret - As an file](5.Advanced%20-%20Secrets.md#using-a-secret---as-an-file)
- [6.Advanced - Usage & Resource Monitoring](6.Advanced%20-%20Usage%20%26%20Resource%20Monitoring.md)
    - [Introduction](6.Advanced%20-%20Usage%20%26%20Resource%20Monitoring.md#introduction)
    - [Many Solutions](6.Advanced%20-%20Usage%20%26%20Resource%20Monitoring.md#many-solutions)
    - [Heapster](6.Advanced%20-%20Usage%20%26%20Resource%20Monitoring.md#heapster)
      - [Enabling Heapster on Minikube](6.Advanced%20-%20Usage%20%26%20Resource%20Monitoring.md#enabling-heapster-on-minikube)
    - [Grafana](6.Advanced%20-%20Usage%20%26%20Resource%20Monitoring.md#grafana)
- [7.Advanced - Namespaces & Resource Quotas](7.Advanced%20-%20Namespaces%20%26%20Resource%20Quotas.md)
    - [Introduction](7.Advanced%20-%20Namespaces%20%26%20Resource%20Quotas.md#introduction)
    - [What are namespace? Why use them?](7.Advanced%20-%20Namespaces%20%26%20Resource%20Quotas.md#what-are-namespace-why-use-them)
    - [Resource Limits in namespace](7.Advanced%20-%20Namespaces%20%26%20Resource%20Quotas.md#resource-limits-in-namespace)
    - [Useful Commands for namespaces](7.Advanced%20-%20Namespaces%20%26%20Resource%20Quotas.md#useful-commands-for-namespaces)
    - [Practical Example](7.Advanced%20-%20Namespaces%20%26%20Resource%20Quotas.md#practical-example)
      1. [Create namespace](7.Advanced%20-%20Namespaces%20%26%20Resource%20Quotas.md#1-create-namespace)
      2. [Assign Limit](7.Advanced%20-%20Namespaces%20%26%20Resource%20Quotas.md#2-assign-limit)
      3. [Deploy Tomcat with Resource Request & Replica](7.Advanced%20-%20Namespaces%20%26%20Resource%20Quotas.md#3-deploy-tomcat-with-resource-request--replica)
      4. [See Deployment Status](7.Advanced%20-%20Namespaces%20%26%20Resource%20Quotas.md#4-see-deployment-status)
- [8.Advanced - Auto Scaling.](8.Advanced%20-%20Auto%20Scaling.md)
    - [Introduction](8.Advanced%20-%20Auto%20Scaling.md#introduction)
    - [What Is The Horizontal Pod Autoscaler?](8.Advanced%20-%20Auto%20Scaling.md#what-is-the-horizontal-pod-autoscaler)
    - [Creating an HPA?](8.Advanced%20-%20Auto%20Scaling.md#creating-an-hpa)
    - [Practical Example](8.Advanced%20-%20Auto%20Scaling.md#practical-example)
      1. [Apply wordpress deployment](8.Advanced%20-%20Auto%20Scaling.md#1-apply-wordpress-deployment)
      2. [Add an HPA to Enable Auto-Scaling](8.Advanced%20-%20Auto%20Scaling.md#2-add-an-hpa-to-enable-auto-scaling)
      3. [Simulate Using an Infinite HTTP Request Loop](8.Advanced%20-%20Auto%20Scaling.md#3-simulate-using-an-infinite-http-request-loop)
      4. [Check the HPA status](8.Advanced%20-%20Auto%20Scaling.md#4-check-the-hpa-status)

## 🔖 Full Kubernetes references & Cheat Sheet
- kubectl reference: https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands
- kubectl cheat sheet: https://kubernetes.io/docs/user-guide/kubectl-cheatsheet/

## 💬 Contributing

Your contributions are always welcome! :tada:

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## 📜 License

The MIT License (MIT) 2018
> GitHub [@yinkokpheng](https://github.com/yinkokpheng)

[GoDoc]: https://godoc.org/k8s.io/kubernetes
[GoDoc Widget]: https://godoc.org/k8s.io/kubernetes?status.svg
[Submit Queue]: http://submit-queue.k8s.io/#/ci
[Submit Queue Widget]: http://submit-queue.k8s.io/health.svg?v=1

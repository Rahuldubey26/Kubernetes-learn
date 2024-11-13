# Kubernetes Configuration Examples

This repository contains examples of various Kubernetes configurations to demonstrate Pods, ConfigMaps, Jobs, and multi-container setups.

## Table of Contents
- [Simple Pod](#simple-pod)
- [ConfigMap Example](#configmap-example)
- [Job](#job)
- [Pod with Init Container](#pod-with-init-container)
- [Pod with Multiple Init Containers](#pod-with-multiple-init-containers)
- [Services](#services)
- [Multi-Container Pod](#multi-container-pod)

## Simple Pod
A basic Pod running an Ubuntu container with a simple command and arguments.
```yaml
apiVersion: v1
kind: Pod
metadata:
  name: example-pod
  labels:
    purpose: demonstrate-args
spec:
  containers:
  - name: example-container
    image: ubuntu
    command: ["/bin/echo", "Hello"]  
    args: ["Welcome", "to", "Kube Learning"]

## To run -> kubectl create -f  first.yaml and kubectl apply name.yaml
## Remember only once we can create but can apply many times.

![alt text](3FFCF935-71A5-4229-8B0B-A51348BB43C7.png)

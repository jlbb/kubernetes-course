# Kubernetes course

This repository contains the course files for my Kubernetes course on Udemy: https://www.udemy.com/learn-devops-the-complete-kubernetes-course/?couponCode=KUBERNETES_GITHUB

## Cheatsheet: Docker commands

Build image: `docker build .`

Build & Tag: `docker build -t wardviaene/k8s-demo:latest .`

Tag image: `docker tag imageid wardviaene/k8s-demo`

Push image: `docker push wardviaene/k8s-demo`

List images: `docker images`

List all containers: `docker ps -a`

## Cheatsheet: Kubernetes commands

`kubectl get pod`: Get information about all running pods

`kubectl describe pod <pod>`: Describe one pod

`kubectl expose pod <pod> --port=444 --name=frontend`: Expose the port of a pod (creates a new service)

`kubectl port-forward <pod> 8080`: Port forward the exposed pod port to your local machine

`kubectl attach <podname> -i`: Attach to the pod

`kubectl exec <pod> -- command`: Execute a command on the pod

`kubectl label pods <pod> mylabel=awesome`: Add a new label to a pod

`kubectl run -i --tty busybox --image=busybox --restart=Never -- sh`: Run a shell in a pod - very useful for debugging

`kubectl get deployments`: Get information on current deployments

`kubectl get rs`: Get information about the replica sets

`kubectl get pods --show-labels`: get pods, and also show labels attached to those pods

`kubectl rollout status deployment/helloworld-deployment`: Get deployment status

`kubectl set image deployment/helloworld-deployment k8s-demo=k8s-demo:2`: Run k8s-demo with the image label version 2

`kubectl edit deployment/helloworld-deployment`: Edit the deployment object

`kubectl rollout status deployment/helloworld-deployment`: Get the status of the rollout

`kubectl rollout history deployment/helloworld-deployment`: Get the rollout history

`kubectl rollout undo deployment/helloworld-deployment`: Rollback to previous version

`kubectl rollout undo deployment/helloworld-deployment --to-revision=n`: Rollback to any version version

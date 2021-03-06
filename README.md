# minikube
Personal documentation on minikube
# Useful command to run minikube

# Install minikube
# https://gist.github.com/gonzaloplaza/f62fdcfdb6aac3d15a0fe0d750715729

# Start Kubernetes Cluster loccally with Minikube
#Create and run Kubernetes cluster. This will take some few minutes depending on your Internet connection.

$ minikube start
# Test Kubernetes service
# We test our cluster running a demo service

$ kubectl cluster-info
$ kubectl run hello-minikube --image=gcr.io/google_containers/echoserver:1.4 --port=8080
$ kubectl expose deployment hello-minikube --type=NodePort
$ kubectl get services
$ minikube service hello-minikube --url
$ minikube dashboard
$ kubectl delete service hello-minikube
$ kubectl delete deployment hello-minikube
$ minikube stop
Adds Kubectl command 'k' alias to bash (optional)
Using command aliases for minikube and kubectl, example: "mk start", "k get po". Note: You need to restart your bash terminal to see aliases working.

$ echo "alias k='kubectl'" >> ~/.bash_aliases
$ echo "alias mk='minikube'" >> ~/.bash_aliases

**Before build in a terminal**

eval $(minikube -p minikube docker-env)

**Start a local registry**

docker run -d -p 5000:5000 --restart=always --name registry registry:2
docker build ...
docker tag  {name} localhost:5000/{name}
docker push localhost:5000/{name}

**Use yaml file**

kubectl create -f file.yaml
kubectl delete -f file.yaml
kubectl apply -f file.yaml
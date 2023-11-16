- 👋 Hi, I’m @jkdasari31
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
jkdasari31/jkdasari31 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->


kubernetes-configmap-reload
Pre-requisites:
- Install Git
- Install Maven
- Install Docker
- EKS Cluster
  
Clone code from github:
git clone https://github.com/vikash-kumar01/spring-cloud-kubernetes.git
cd spring-cloud-kubernetes/kubernetes-configmap-reload
Build Maven Artifact:
mvn clean install
Build Docker image for Springboot Application
docker build -t vikashashoke/kubernetes-configmap-reload .
Docker login
docker login
Push docker image to dockerhub
docker push vikashashoke/kubernetes-configmap-reload
Deploy Spring Application:
kubectl apply -f kubernetes-configmap.yml
Check Deployments, Pods and Services:
kubectl get deploy
kubectl get pods
kubectl get svc
Now Goto Loadbalancer and check whether service comes Inservice or not, If it comes Inservice copy DNS Name of Loadbalancer and Give in WebUI

http://a70a89c22e06f49f3ba2b3270e974e29-1311314938.us-west-2.elb.amazonaws.com:8080/home/data
2

Now we can cleanup by using below commands:
kubectl delete deploy kubernetes-configmap-reload
kubectl delete svc kubernetes-configmap-reload
springboot_k8s_application
mrdevops_java_app

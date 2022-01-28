# Kubernetes


# key words
minikube

driver

hyper-v, 虛擬交換器

Pod的概念---一組容器的集合, 而非單獨的容易。 他是短暫而非長久應用。 Pods被調度到節點 kepp在此節點上直到被銷毀

<img width="760" alt="2022-01-28_16h26_18" src="https://user-images.githubusercontent.com/66947341/151512646-5f644b5d-02de-409c-a5c4-fb3ef8074484.png">

在文件中可以得到一些資訊: 開啟port80給http traffic(http流量), 當容器啟動時, 向他傳送一些arguments參數, 這個pod由一個container容器組成(the monolith)

# key path
C:\Users\username\.minikube


# ---------- 環境設定 ----------
使用hyper-v

<img width="480" alt="2022-01-28_15h15_20" src="https://user-images.githubusercontent.com/66947341/151503677-9c6747f6-811d-4f93-b5cb-b46fed1ddc68.png">
<img width="732" alt="2022-01-28_15h17_00" src="https://user-images.githubusercontent.com/66947341/151503867-35ecb351-2a49-42a5-a9e0-214494379b83.png">

# ---------- 語法 ----------
$ kubectl create deployment <server name> --image=<image name>
  
$ kubectl expose deployment <server name> --type=<e.g. LoadBalancer, NodePort> --port <port號e.g.8080>
  
$ kubectl get port
  
$ kubectl kill
  
$ kubectl delete pod <pod_name> -n <namespace> --grace-period 0 --force
  
$ kubectl get service
  
$ kubectl delete service <service name>
  
 

(minikube v0.27.0 目前比0.30.0穩定)
  
$ minikube status
  
$ minikube stop
  
$ minikube delete
  
$ minikube service <pod/service name> --url
  
$ minikube start --vm-driver hyperv --hyperv-virtual-switch <虛擬交換器名>
  
$ minikube ssh "sudo poweroff"
  
ps $ Stop-VM -Name minikube -Force

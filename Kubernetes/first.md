# はじめての Kubernetes

## バージョン確認

````
kubectl version
````

- 表示される
````
Client Version: v1.31.2
Kustomize Version: v5.4.2
Server Version: v1.30.6+k3s1
````

kubectl run --image gcr.io/google-samples/hello-app:1.0 --restart Never helloworld

kubectl get pods

kubectl logs helloworld

kubectl describe pod helloworld

kubectl exec -it helloworld sh

kubectl run --env TEST_ENV=hello_world --image gcr.io/google-samples/hello-app:1.0 --restart Never helloworld

- curlコンテナが入った Pod を作成する
kubectl run --restart Never --image curlimages/curl:7.68.0 -it --rm curl sh

- helloworldへの curlアクセステスト
curl helloworldのIPアドレス:8080


watch -t "kubectl get pod"
Windows PowerShell では、以下で代替する
while ($true -eq $true) {kubectl get pod; sleep 1 ; clear}

- podの IPアドレスを確認する
````
kubectl get pod --output wide
````

````
NAME         READY   STATUS    RESTARTS   AGE     IP          NODE              NOMINATED NODE   READINESS GATES
helloworld   1/1     Running   0          5m59s   10.42.0.9   desktop-r8nibgo   <none>           <none>
````

- podを削除する
kubectl delete pod helloworld

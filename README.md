# MY HELM CHART

## 설명
이 chart는 테스트용 차트입니다
사전에 metallb를 설치해 두셔야 합니다!!

## 설치방법
```bash
helm repo add myrepo1 http://jinnse.github.io/aws9Chart1
helm install myrelease1 myrepo1/nginx-chart

or
helm install myrelease1 myrepo1/nginx-chart --set replicaCount=8
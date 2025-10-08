# MY HELM CHART

## 설명
이 chart는 테스트용 차트입니다
사전에 metallb를 설치해 두셔야 합니다!!
ingress controller는 nginx 사용했습니다.

## 설치방법
```bash
helm repo add myrepo1 http://jinnse.github.io/aws9btoyChart
helm install myrelease1 ./aws9bchart

or
helm install myrelease1 ./aws9bchart --set apps[0].replicacount=5 \
--set apps[1].replicacount=5 \
--set apps[2].replicacount=5
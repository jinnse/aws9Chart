# aws9Chart
aws9Chart은 https://github.com/jinnse/aws9toy aws9toy를 구성한 클러스터를 Helm Chart를 이용해서 배포합니다 

---

## 사전 준비 사항
- Kubernetes 클러스터 구축
  - master, node1, node2, node3 형태로 구성
  - metallb, nginx-controller(ingress controller), Calico 설치
- NFS 서버 구축
- 사설 DNS 서버 구축을 위한 DNS 서버 구축
  - 도메인 및 외부 접근용 ip 설정
- Harbor 설치
  - 이미지 접근 가능하도록

---

## 디렉토리 구성
```bash
├── charts
├── Chart.yaml
├── templates
│ ├── deploy.yml
│ ├── hpa.yml
│ ├── ingress.yml
│ ├── pvc.yml
│ ├── README.md
│ └── svc.yml
└── values.yaml
```

---

## 설치방법
```bash
helm repo add awsChart http://jinnse.github.io/aws9Chartdeploy
helm repo update
helm install my-chart awsChart/aws9Chart

or
helm install my-chart awsChart/aws9Chart --set replicaCount=8


# React + Argo CD + EKS Bitirme Projesi

Bu proje, Halit Elubeyt tarafından bir bitirme projesi kapsamında geliştirilmiştir.  
Amaç, bir React uygulamasının tam otomatik CI/CD hattı ile AWS üzerinde dağıtılmasını sağlamaktır.

## 🚀 Teknolojiler

- React (Frontend Uygulama) .......
- Docker (Uygulama paketleme)
- GitHub Actions (CI/CD Pipeline)
- AWS ECR (Container registry)
- AWS EKS (Kubernetes altyapısı)
- Argo CD (GitOps deployment)
- Prometheus + Grafana (Monitoring)

## 🔄 CI/CD Pipeline Akışı

1. Kod GitHub’a push edilir
2. GitHub Actions otomatik olarak:
   - Uygulama testlerini çalıştırır (`npm test`)
   - Docker image oluşturur
   - Image’i ECR’ye gönderir
3. Argo CD, değişikliği algılar ve React uygulamasını EKS’e deploy eder
4. Pod’lar güncellenir ve servis LoadBalancer üzerinden yayınlanır


## 🌍 Uygulama Erişimi

- React Uygulaması: `http://<load-balancer-ip>`
- Grafana Monitoring: `http://<grafana-lb-ip>`
  - Kullanıcı: `admin`
  - Şifre: `prom-operator`

## 👤 Geliştirici

- **Ad:** Halit Elubeyt  
- Bu proje bir DevOps bitirme projesi olarak hazırlanmıştır.

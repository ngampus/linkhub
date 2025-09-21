# linkhub
PT Data Integrasi Inovasi
# Helm Chart untuk Aplikasi Backend LinkHub

Chart ini mengelola deployment aplikasi Backend (Go API) untuk proyek LinkHub di atas Kubernetes.

## Desain Arsitektur

Infrastruktur ini dirancang untuk aman dan andal dengan menempatkan cluster Kubernetes di dalam jaringan privat. Akses masuk dikelola oleh Load Balancer dan Traefik Ingress, sementara akses keluar menggunakan NAT Gateway. Monitoring dilakukan oleh Prometheus dan Grafana.

## Prasyarat

- Kubernetes 1.19+
- Helm 3.2+
- Traefik sudah terpasang sebagai Ingress Controller di cluster.

## Cara Instalasi

1.  Clone repository chart ini.
2.  Sesuaikan parameter di dalam file `values.yaml` sesuai kebutuhan lingkungan Anda.
3.  Jalankan perintah berikut untuk melakukan instalasi atau upgrade.

    ```bash
    helm upgrade --install linkhub-backend . \
      --namespace linkhub-prod \
      --set image.tag="v1.2.5"
    ```

## Konfigurasi

Parameter berikut dapat diubah melalui file `values.yaml` atau dengan flag `--set`.

| Parameter | Deskripsi | Default |
| :--- | :--- | :--- |
| `replicaCount` | Jumlah replika pod yang akan dijalankan. | `2` |
| `image.repository`| Alamat image di Harbor Registry. | `harbor.mydomain.com/linkhub/backend` |
| `image.tag`| Tag image yang akan di-deploy (biasanya diisi CI/CD). | `""` |
| `ingress.enabled`| Aktifkan atau non-aktifkan pembuatan Ingress. | `true` |
| `ingress.hosts`| Konfigurasi hostname dan path untuk Ingress. | `api.linkhub.com` |
| `resources`| Alokasi resource CPU dan Memory untuk pod. | `{}` |

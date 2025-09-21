Berikut adalah daftar semua tools open-source yang dipilih untuk membangun dan mengelola infrastruktur aplikasi "LinkHub".

| Tool | Kategori | Alasan Pemilihan |
| :--- | :--- | :--- |
| **Jenkins** | CI/CD | Sangat powerful, fleksibel dengan ribuan plugin, dan merupakan standar industri untuk orkestrasi pipeline CI/CD yang kompleks. |
| **Docker** | Containerization | Standar de-facto untuk mengemas aplikasi. Memastikan konsistensi lingkungan dari laptop developer hingga production. |
| **Kubernetes** | Orchestration | Platform orkestrasi paling matang untuk menjalankan aplikasi kontainer dalam skala besar. Mendukung self-healing dan auto-scaling. |
| **Helm** | Deployment | Menyederhanakan proses deployment aplikasi yang kompleks di Kubernetes. Memungkinkan templating, manajemen versi, dan rollback yang mudah. |
| **Traefik** | Ingress Controller | Modern, mudah dikonfigurasi, dan memiliki fitur auto-discovery service Kubernetes. Terintegrasi baik dengan Let's Encrypt untuk SSL otomatis. |
| **Harbor** | Image Registry | Alternatif open-source untuk ACR/ECR. Menyediakan keamanan (scan kerentanan), manajemen akses, dan replikasi image. 100% OSS. |
| **PostgreSQL** | Database | Sistem database relasional open-source yang powerful, andal, dan memiliki banyak fitur canggih yang cocok untuk aplikasi modern. |
| **Prometheus** | Monitoring | Dibuat khusus untuk memantau lingkungan dinamis seperti Kubernetes. Model *pull-based* dan bahasa query PromQL sangat efektif. |
| **Grafana** | Visualization | Alat visualisasi terbaik untuk metrik dari Prometheus. Memungkinkan pembuatan dashboard interaktif untuk pemantauan real-time dan alerting. |
| **Cloudflare** | DNS & Security | Menyediakan lapisan keamanan pertama (DDoS, WAF), manajemen DNS global, dan CDN untuk mempercepat pengiriman aset Frontend. |
| **NAT Gateway** | Egress Networking | Memberikan akses internet keluar untuk node di private subnet, sambil memastikan IP sumber yang statis dan menyembunyikan IP privat node. |

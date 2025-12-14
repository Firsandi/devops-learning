# 🚀 DevOps Learning Journey 2025-2026

Dokumentasi perjalanan belajar menjadi DevOps Engineer dari Full-Stack Developer & Linux Sysadmin.

## 👤 About Me

**Status:** Mahasiswa Fasilkom UNEJ  
**Background:** Full-Stack Web Developer & Linux System Administrator  
**Goal:** Menjadi DevOps Engineer dalam 7 bulan (Des 2025 - Jul 2026)

## ✅ Current Skills

### System Administration
- Linux (Ubuntu Server, Zorin OS)
- Apache2 & Nginx web server
- Networking (DNS, Static IP, UFW firewall)
- SSH & basic security
- VirtualBox & VM management

### Web Development
- **Backend:** Laravel 12, PHP 8.3.6
- **Frontend:** Vue.js, HTML/CSS, Tailwind, Bootstrap
- **Database:** PostgreSQL, MySQL
- **Version Control:** Git

### Projects
- SIMPROK (Administrative web app)
- E-commerce websites
- Server deployment & hosting

## 🎯 DevOps Skills Progress

- [🟢] **Docker & Containerization (IN PROGRESS - 60% complete!)**
  - ✅ Installation & setup (Docker Engine 29.1.2)
  - ✅ Basic commands mastered (run, ps, stop, start, rm, logs, exec, inspect, stats)
  - ✅ Networking concepts (ADVANCED! Port mapping, bridge networks, namespaces)
  - ✅ Container isolation & architecture understanding
  - ✅ Linux permissions & security model
  - ✅ Dockerfile & custom images
  - ✅ Volumes & persistent data (MASTERED!)
  - [ ] Docker Compose for multi-container apps
  - [ ] Custom networks & network modes
- [ ] Kubernetes & Orchestration
- [ ] CI/CD (GitHub Actions, Jenkins)
- [ ] Infrastructure as Code (Terraform, Ansible)
- [ ] Cloud Platforms (AWS/GCP)
- [ ] Monitoring (Prometheus, Grafana)
- [ ] Python for automation

---

## 🗓️ 7-Month Roadmap

### Fase 1: Desember 2025 - Januari 2026
**🎯 Target: Docker Mastery & Git Advanced**

**Week 1-2 (10-24 Des):**
- [✅] Docker fundamentals: install, basic commands
- [✅] Understand containers vs VMs
- [✅] Practice with simple containers
- [✅] Create first Dockerfile
- [✅] Volumes & persistent data

**Week 3-4 (25 Des - 7 Jan):**
- [ ] Docker Compose for multi-container apps
- [ ] Dockerize simple Laravel app
- [ ] Docker networking advanced
- [ ] Git advanced: branching, merge strategies

**📦 Project:** Dockerize SIMPROK project (Laravel + PostgreSQL)

---

### Fase 2: Februari - Maret 2026
**🎯 Target: CI/CD Automation**

**Week 1-4 (Feb):**
- [ ] GitHub Actions basics
- [ ] Automated testing integration
- [ ] Deployment automation
- [ ] CI pipeline untuk Laravel

**Week 5-8 (Mar):**
- [ ] Jenkins fundamentals
- [ ] Build automated pipelines
- [ ] Webhooks & triggers
- [ ] Production deployment automation

**📦 Project:** Full CI/CD pipeline untuk Laravel app

---

### Fase 3: April - Mei 2026
**🎯 Target: Kubernetes & IaC**

**Week 1-4 (Apr):**
- [ ] Kubernetes basics (Minikube)
- [ ] Pods, Deployments, Services
- [ ] ConfigMaps & Secrets
- [ ] Deploy Laravel to K8s

**Week 5-8 (Mei):**
- [ ] Terraform fundamentals
- [ ] Ansible for configuration
- [ ] IaC best practices
- [ ] Multi-environment setup

**📦 Project:** Deploy app to Kubernetes + IaC repository

---

### Fase 4: Juni - Juli 2026
**🎯 Target: Cloud & Monitoring**

**Week 1-4 (Jun):**
- [ ] Cloud platform (GCP/AWS)
- [ ] Cloud compute, storage, networking
- [ ] Managed services
- [ ] Deploy to cloud

**Week 5-8 (Jul):**
- [ ] Prometheus & Grafana
- [ ] Logging (ELK Stack/Loki)
- [ ] Python automation basics
- [ ] Portfolio finalization

**📦 Project:** Production-ready cloud deployment + monitoring

---

## 📊 Daily Progress Log

### Week 1: Docker Fundamentals (10-16 Des 2025)

#### 📅 Day 1 - Selasa, 10 Desember 2025

**Setup & Planning**
- ✅ Membuat roadmap DevOps learning (7 bulan)
- ✅ Setup GitHub repository tracking
- ✅ Setup shortcuts (devops, devcd, devpush, devlog)
- ✅ Research Docker learning path

**Study Time:** 1 jam  
**Status:** Foundation set!

---

#### 📅 Day 2 - Kamis, 11 Desember 2025

**Docker Installation & Fundamentals - DEEP DIVE**

**Installation & Setup:**
- ✅ Install Docker Engine 29.1.2
- ✅ Fix Docker daemon startup
- ✅ Setup user permissions
- ✅ First container: hello-world

**Linux System Concepts:**
- User, Group, Others permission system
- File ownership & sudo
- Security implications

**Container Concepts:**
- Container = isolasi untuk projects
- Container vs VM comparison
- Benefits: portability, consistency

**Networking Mastery:**
- Port mapping format & rationale
- Docker bridge network
- Network namespaces
- iptables/DNAT rules

**Docker Commands Mastered:**
```bash
# Lifecycle
docker run, ps, stop, start, rm

# Inspection
docker logs, exec, inspect, stats

# Images
docker images, rmi, pull

# System
docker container prune, system prune
```

**Study Time:** 3+ hours  
**Level:** Advanced networking knowledge  
**Performance:** A+ (3-5x faster than average)

---

#### 📅 Day 3 - Kamis, 12 Desember 2025

**Custom Docker Image & Dockerfile Basics**

**Learning Objectives:**
- Docker Image vs Container
- Membuat Dockerfile pertama
- Build custom Docker image
- Deploy static HTML

**Konsep Dikuasai:**

**Image vs Container:**
- Image = Blueprint (read-only)
- Container = Running instance (writable layer)

**Base Image & Alpine Linux:**
- Alpine = OS minimal (8MB)
- nginx:alpine = Nginx + Alpine (40MB)

**Dockerfile Instructions:**
```dockerfile
FROM nginx:alpine
COPY index.html /usr/share/nginx/html/
EXPOSE 80
```

**Hands-on Practice:**
```bash
mkdir ~/docker-day3
cd ~/docker-day3
# Create index.html & Dockerfile
docker build -t nginx-day3 .
docker run -d -p 8080:80 --name test-day3 nginx-day3
```

**Result:**
- ✅ Custom image berhasil dibuat
- ✅ Container jalan dengan custom HTML
- ✅ File ter-inject permanen ke image

**Study Time:** 27 menit  
**Status:** Highly efficient!

---

#### 📅 Day 4 - Sabtu, 13 Desember 2025

Skip (acara organisasi HIMATIF)

---

#### 📅 Day 5 - Minggu, 14 Desember 2025

**Docker Volumes & Persistent Data**

**Learning Objectives:**
- Memahami masalah data temporary di container
- Implementasi Docker Volumes
- Praktik dengan MySQL container
- Test data persistence

**Problem: Container Data is Temporary**

Data yang hilang saat container dihapus:
- Database records
- User uploads
- Application logs
- Cache files

**Solution: Docker Volumes**

Volume = External storage terpisah dari container lifecycle

Karakteristik:
- Lokasi: /var/lib/docker/volumes/
- Managed by Docker
- Persistent data
- Portable & can be mounted to multiple containers

**Volume vs Bind Mount:**

| Aspek | Volume | Bind Mount |
|-------|--------|------------|
| Management | Docker CLI | Manual path |
| Location | /var/lib/docker/volumes/ | Anywhere di host |
| Best For | Production database | Development |
| Speed | Super cepat | Cepat |

**Default Data Directory:**
```
MySQL       → /var/lib/mysql
PostgreSQL  → /var/lib/postgresql/data
MongoDB     → /data/db
Redis       → /data
```

**Hands-on Practice:**

```bash
# Step 1: Create volume
docker volume create mysql-data
docker volume ls
docker volume inspect mysql-data

# Step 2: Run MySQL dengan volume
docker run -d \
  --name my-mysql \
  -e MYSQL_ROOT_PASSWORD=secret123 \
  -e MYSQL_DATABASE=belajar_db \
  -v mysql-data:/var/lib/mysql \
  -p 3307:3306 \
  mysql:8.0

# Step 3: Create table & insert data
docker exec -it my-mysql mysql -uroot -psecret123 belajar_db
```

```sql
CREATE TABLE mahasiswa (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nim VARCHAR(20),
    nama VARCHAR(100),
    jurusan VARCHAR(50)
);

INSERT INTO mahasiswa (nim, nama, jurusan) VALUES
('230101001', 'Firsandia Nur Fajri', 'Ilmu Komputer'),
('230101002', 'Ahmad Rizki', 'Sistem Informasi'),
('230101003', 'Siti Nurhaliza', 'Teknik Informatika'),
('230101004', 'Budi Santoso', 'Ilmu Komputer'),
('230101005', 'Dewi Lestari', 'Sistem Informasi');

SELECT * FROM mahasiswa;
exit
```

```bash
# Step 4: Test persistence - hapus container
docker stop my-mysql
docker rm my-mysql

# Volume tetap ada!
docker volume ls

# Step 5: Create container baru dengan volume sama
docker run -d \
  --name my-mysql-new \
  -e MYSQL_ROOT_PASSWORD=secret123 \
  -e MYSQL_DATABASE=belajar_db \
  -v mysql-data:/var/lib/mysql \
  -p 3307:3306 \
  mysql:8.0

# Cek data - MASIH ADA!
docker exec -it my-mysql-new mysql -uroot -psecret123 belajar_db
SELECT * FROM mahasiswa;
```

**Achievement:**
- ✅ Data tetap ada setelah container dihapus
- ✅ Volume persistence works perfectly
- ✅ Production-ready knowledge

**Key Insights:**
- Container lifecycle ≠ data lifecycle
- Volume adalah external storage
- docker build = ISO image
- Path mount harus sesuai app default
- Production wajib pakai volume

**Commands Mastered:**
```bash
docker volume create/ls/inspect/rm
docker run -v <volume>:<path>
docker exec -it <container> mysql
```

**Troubleshooting:**
- Port conflict: pakai port berbeda
- PostgreSQL 18+ incompatibility: recreate volume
- MySQL access denied: check password typo

**Study Time:** 86 menit (effective: 60 menit)  
**Status:** Core completed  
**Performance:** Excellent understanding

---

### Week 1 Summary

**Total Study Hours:** 5+ hours
- Day 1: 1h (roadmap)
- Day 2: 3h (Docker + networking)
- Day 3: 27 min (Dockerfile)
- Day 5: 60 min (Volumes)

**Main Achievements:**
- ✅ Docker installation & networking mastery
- ✅ Custom images dengan Dockerfile
- ✅ Persistent data dengan volumes
- ✅ Production-ready concepts

**Commands Mastered:** 20+ Docker commands with deep understanding

**Concepts Mastered:**
- Networking, isolation, permissions
- Container architecture
- Image building & layering
- Data persistence strategies

**Next Week Focus:**
- Docker Compose
- Multi-container apps
- Advanced networking
- Laravel dockerization

---

## 🎯 Projects Tracker

### 1. SIMPROK Dockerization
- **Status:** 🔴 Not Started
- **Tech Stack:** Laravel, PostgreSQL, Docker, Docker Compose
- **Timeline:** January 2026
- **Goal:** Full containerized development environment

### 2. CI/CD Pipeline
- **Status:** 🔴 Not Started
- **Tech Stack:** GitHub Actions, Jenkins, Docker
- **Timeline:** March 2026
- **Goal:** Automated build, test, deploy

### 3. Kubernetes Deployment
- **Status:** 🔴 Not Started
- **Tech Stack:** Kubernetes, Helm, Docker
- **Timeline:** May 2026
- **Goal:** Production-grade K8s deployment

### 4. Cloud Infrastructure
- **Status:** 🔴 Not Started
- **Tech Stack:** GCP/AWS, Terraform, Monitoring
- **Timeline:** July 2026
- **Goal:** Scalable cloud architecture

---

## 📚 Learning Resources

### Docker
- Docker Official Documentation
- Docker Tutorial for Beginners
- Hands-on experimentation approach

### Kubernetes
- Kubernetes Documentation
- KodeKloud Kubernetes Course

### CI/CD
- GitHub Actions Documentation
- Jenkins Official Guide
- DevOps Roadmap: roadmap.sh/devops

### General
- r/devops Community
- DevOps Indonesia Discord
- TechWorld with Nana (YouTube)

---

## 🔥 Commitment & Tracking

**Started:** 10 Desember 2025  
**Target Completion:** Juli 2026  
**Study Time Target:** 10-15 jam/minggu

**Current Streak:** 4 days (Day 1, 2, 3, 5)  
**Total Study Hours:** 5+ hours  
**Commits:** 5+ 

**Weekly Goal:** Minimal 5 commits, 10 jam study time  
**Status:** ✅ ON TRACK!

---

## 💡 Notes & Reflections

### Key Learnings

**Docker = Networking + Linux Namespaces + Isolation**
- Network namespaces provide isolated stack
- iptables/DNAT for port forwarding
- Similar to VM NAT concept

**Container Isolation**
- Each project can have different dependencies
- No conflicts between projects
- Clean, reproducible environments

**Port Mapping**
- Format: -p host:container
- Host port: bebas
- Container port: fixed by app

**Data Persistence**
- Container data = temporary
- Volume data = persistent
- Critical for production databases

### Challenges & Solutions

**Docker daemon not starting**
- Solution: systemctl start/enable docker

**Permission denied**
- Solution: usermod -aG docker + newgrp docker

**Port mapping confusion**
- Solution: Relate to VM NAT, experiments

**Data persistence**
- Solution: Docker volumes, not container storage

### Tips for Future Self

- Consistency > Intensity
- Document everything
- Practice > Theory
- Ask WHY, not just HOW
- Connect new concepts with existing knowledge
- Experiment fearlessly
- Take breaks for brain consolidation

### Performance Insights

- Learning Speed: 3-5x faster than average
- Strengths: Critical thinking, experimentation
- Approach: Deep dive vs surface learning
- Foundation: Strong Linux/networking background
- Next Level: Docker Compose, multi-container apps

---

**Last Updated:** 14 Desember 2025, 22:38 WIB  
**Next Milestone:** Docker Compose & multi-container apps  
**Current Focus:** Docker fundamentals mastery complete  
**Momentum:** Strong progress, consistent learning!
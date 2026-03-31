# 📘 Day 2 – Docker & DevOps Basics (INT332)

---

## 🚀 Introduction to DevOps
DevOps is a combination of **Development (Dev)** and **Operations (Ops)** aimed at improving collaboration, automating workflows, and delivering software faster and more reliably.

---

## 🖥️ Virtualization vs Containerization

### 🔹 Virtualization
- Divides a physical server into multiple virtual machines using a **hypervisor**
- Each VM runs its own operating system

#### ✅ Advantages
- Efficient resource utilization  
- Better security isolation  
- Disaster recovery support  
- Cost savings  

#### ❌ Drawbacks
- High resource overhead  
- Slow boot time  
- Complex management  
- Limited scalability  

---

### 🔹 Containerization
- Lightweight alternative to virtualization  
- Shares host OS kernel  
- Runs only required dependencies  

#### ✨ Key Features
- Fast startup (seconds)  
- Low resource usage  
- High scalability  
- High portability  

👉 Best suited for **microservices architecture**

---

## 📦 Need for Containers
- Transition from monolithic → microservices architecture  
- Faster deployment  
- Better portability  
- Efficient resource utilization  

---

## ⚙️ Container Runtime
A container runtime is responsible for running containers.

### 🔧 Responsibilities
- Create containers  
- Start/Stop containers  
- Manage lifecycle  
- Provide isolation  

### 🔹 Types of Runtimes

#### High-Level Runtimes
- Docker Engine  
- containerd  
- CRI-O  

#### Low-Level Runtimes
- runc  

---

## 🔐 Process Isolation & Namespaces
Containers achieve isolation using **Linux namespaces**.

### 🔹 Types of Namespaces
- **PID Namespace** → Process isolation  
- **Network Namespace** → Separate IP & ports  
- **Mount Namespace** → Filesystem isolation  
- **UTS Namespace** → Hostname isolation  
- **User Namespace** → Security mapping  

👉 *Namespaces create isolated environments*

---

## ⚡ Control Groups (cgroups)
cgroups control resource usage of containers.

### 🔧 Controls
- CPU usage  
- Memory limits  
- Disk I/O  

👉 *Namespaces isolate, cgroups control*

---

## 📦 Container Image
A container image is a **read-only blueprint** of a container.

### 📁 Contains
- Base OS  
- Application code  
- Libraries  
- Dependencies  

---

## 🧱 Image Layers
- Each Dockerfile instruction creates a layer  
- Layers are:
  - Immutable  
  - Cached  
  - Reusable  

### 🚀 Benefits
- Faster builds  
- Smaller storage  
- Efficient deployment  

---

## 🗂️ Image Registry
A registry stores and distributes container images.

### 🔹 Why Needed?
- Centralized storage  
- Version control  
- Easy deployment  
- CI/CD integration  

### 🔹 Types
- Public Registry  
- Private Registry  

---

## 🔄 Image Distribution Process
Build Image
Push to Registry
Pull from Registry
Run Container


---

## 📤 Push vs Pull
- **Push** → Upload image to registry  
- **Pull** → Download image from registry  

---

## 🔁 Role in CI/CD
Code → Build → Push → Deploy
👉 Registry acts as a **bridge between CI and CD**

---

## 🐳 Docker Architecture

### 🔧 Components
- Docker Client  
- Docker Daemon  
- Docker Images  
- Containers  
- Docker Registry (Docker Hub)  

---

## 🔄 Docker Lifecycle
Build → Ship → Run

### 📌 Container States
- Created  
- Running  
- Paused  
- Stopped  

---

## 🧠 Key Takeaways
- Docker enables lightweight containerization  
- Containers are faster than virtual machines  
- Namespaces + cgroups ensure isolation and control  
- Image registries simplify deployment  
- Docker supports modern DevOps workflows  

---

## 📝 Tasks & Learnings

### ✔ Task 1
- Issue: Container crashed due to high memory usage  
- Cause: Missing cgroups configuration  
- Solution: Apply memory limits  

---

### ✔ Task 2
- CPU control → cgroups  
- Process isolation → PID namespace  
- Same port usage → Network namespace  

---


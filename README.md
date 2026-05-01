# System Design Answers

---

## Q-1: Real-Time Traffic Management System

### Constraints

- Massive real-time data
- Low latency required
- Cost constraints
- 24/7 uptime

---

### 1. Design Real-Time Pipeline

**Step 1: Data Collection**
Sensors, cameras, and GPS devices collect live traffic data.

**Step 2: Edge Processing**
Edge devices process urgent data locally for fast signal control.

**Step 3: Cloud Processing**
Data is sent to the cloud for storage, analytics, and AI prediction.

**Step 4: Dashboard & Alerts**
Traffic authorities monitor dashboards and receive alerts.

**Simple Diagram**

```
Sensors / Cameras
        |
   Edge Devices
        |
  Cloud Platform
        |
 Dashboard & Alerts
```

---

### 2. Choose Cloud vs Edge

**Edge Computing** — Used for:
- Real-time traffic signal control
- Fast response
- Low latency

**Cloud Computing** — Used for:
- Data storage
- AI analysis
- Monitoring dashboards

**Best Choice**
Hybrid model (Edge + Cloud) is best because it provides both speed and scalability.

---

### 3. Scalable Architecture

| Layer             | Description                                          |
|-------------------|------------------------------------------------------|
| IoT Layer         | Sensors and cameras collect data                     |
| Edge Layer        | Processes urgent traffic information locally         |
| Cloud Layer       | Stores and analyzes large data                       |
| Application Layer | Dashboards used by traffic police and city authorities |

**Focus Areas**

| Area                | Purpose                          |
|---------------------|----------------------------------|
| IoT Integration     | Connect sensors and cameras      |
| Edge vs Cloud       | Decide processing location       |
| Event-Driven System | React to live traffic events     |
| Fault Tolerance     | Ensure system stays online       |

---
---

## Q-2: Online Judge / Competitive Coding Platform

### Constraints

- Secure code execution
- High concurrency during contests
- Multi-language support
- Low latency

---

### 1. Design Secure Execution System

- Use Docker containers for isolated code execution
- Each user's code runs in a separate container
- Apply memory and CPU limits for security
- Use authentication and access control for users

**Simple Flow**

```
  User Code
      |
Docker Container
      |
Code Execution
      |
Result Output
```

---

### 2. Plan Contest Infrastructure

- Use cloud servers to handle large numbers of users
- Store submissions in cloud databases
- Use load balancers to distribute traffic
- Provide real-time leaderboards and feedback

---

### 3. Suggest Scaling Strategy

**Auto Scaling**
Servers automatically increase during coding contests.

**Load Balancing**
Traffic is distributed across multiple servers.

**Containerization**
Docker containers help run multiple languages securely.

**Fault Tolerance**
Backup servers ensure continuous service.

---

### Focus Areas

| Area               | Description                                              |
|--------------------|----------------------------------------------------------|
| Containerization   | Docker used for isolated and secure code execution       |
| Isolation & Security | Each user environment remains separate and protected   |
| Auto Scaling       | Resources increase automatically during high traffic     |
| Load Balancing     | Improves performance by distributing requests            |

---

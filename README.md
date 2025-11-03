# 🧪 Performance Testing Project (JMeter)

## 📘 Overview
This project demonstrates a complete **performance and functional testing workflow** using **Apache JMeter**.  
It includes:
- Web UI testing simulation (Pet Store)
- API testing (Restful Booker)
- Load profiling with JMeter plugins

---

## 🚀 Project Structure


---

## 🧭 Task I – Functional Scripting

### **1. Web Journey Simulation**
Simulates a full user journey on the [Pet Store](https://petstore.octoperf.com/actions/Catalog.action) website:

1. Navigate to landing page  
2. Click “Sign In” → “Register Now!”  
3. Fill registration fields and save  
4. Click on “Fish” → select first Product ID  
5. Choose the first Item ID → Add to cart  
6. Update quantity to 10 → Update cart  
7. Proceed to checkout → Continue → Confirm order  
8. Validate message:  

---

### **2. API Testing Flow**
Implements CRUD operations on the [Restful Booker API](https://restful-booker.herokuapp.com/apidoc/index.html):

| Step | Method | Endpoint | Description |
|------|---------|-----------|--------------|
| 1 | POST | /auth | Create token |
| 2 | POST | /booking | Create booking |
| 3 | GET | /booking | Get all booking IDs |
| 4 | PUT | /booking/{id} | Update booking (ID=1) |
| 5 | DELETE | /booking/{id} | Delete booking (if ID=1) |

---

### **✅ Best Practices Implemented**
- Full **parameterization** via `CSV Data Set Config`
- **Assertions** based on text validation (not response code)
- **HTTP Request Defaults** for reusability
- **Constant Timers** for realistic pacing
- **Cache & Cookie Managers** for clean test iterations

---

## 🧮 Task II – Performance Run & SLA Validation

- **Thread Group:** 2 users  
- **Test Duration:** 10 minutes  
- **Report Type:** Aggregate Report  

### **SLA Validation Table**

| SLA | Target | Status |
|------|---------|---------|
| Total Errors | ≤ 10% | ✅ Passed / ❌ Failed |
| 90% of Requests | ≤ 3s | ✅ Passed / ❌ Failed |
| 99% of Requests | ≤ 5s | ✅ Passed / ❌ Failed |

*(SLA results are available in Report.pdf)*

---

## ⚙️ Task III – Load Profiling

### **1️⃣ Stepping Thread Group**
**File:** `First_Load.jmx`  
- Ramp-up: 100 users  
- Pace: 1 user/sec  
- Ramp-down: 1 user/sec  

### **2️⃣ Ultimate Thread Group (Bonus)**
**File:** `Second_Load.jmx`  
- Base load: 60 users (1 user/sec, hold 600s)  
- Spike A: +60 users at t=120s (10 users/sec)  
- Spike B: +60 users at t=360s (10 users/sec)  

---

## 🧩 Tools & Technologies
- **Apache JMeter**
- **CSV Data Config**
- **Regex & JSON Extractors**
- **jp@gc Plugins (Stepping, Ultimate Thread Groups)**
- **Assertions, Timers, Cache, Cookie Managers**
- **Aggregate Report / View Results Tree**

---

## 📄 Deliverables

| File | Description |
|------|--------------|
| `JMeter_Assignment.jmx` | Main JMeter script (UI + API) |
| `Test_Data.csv` | Test data for parameterization |
| `Report.pdf` | SLA report with color-coded results |
| `First_Load.jmx` | Stepping thread group configuration |
| `Second_Load.jmx` | Ultimate thread group (spikes) |

---

## 👨‍💻 Author
**Mohamed Elmy**  
Software Testing Engineer | ITI Graduate  
📧 [mohamedelmy37@gmail.com].

---

# Smart Energy Logger & Optimizer  
**Honors Project — CS 537: Introduction to Operating Systems (Fall 2025)**  

## 📖 Overview  
This project applies core **operating system abstractions**—processes, scheduling, synchronization, memory management, and persistence—to a real-world sustainability challenge. Using an Arduino Uno (ELEGOO UNO R3 Starter Kit and Smart Robot Car Kit), the system monitors environmental conditions (temperature and light), **logs data** to an SD card, and **optimizes energy usage** by scheduling control of LEDs and a fan.  

The result is a **low-cost, embedded demonstration of OS principles** that also showcases how these abstractions can benefit society through **sustainability and energy awareness**.  

Similar Arduino kits used:  
- [ELEGOO UNO R3 Project Most Complete Starter Kit (200+ components)](https://www.amazon.com/EL-KIT-001-Project-Complete-Starter-Tutorial/dp/B01CZTLHGE?th=1)  
- [ELEGOO UNO R3 Smart Robot Car Kit V4](https://www.amazon.com/dp/B07KPZ8RSZ/ref=sspa_dk_detail_4?psc=1&pd_rd_i=B07KPZ8RSZ&pd_rd_w=MSEK2&content-id=amzn1.sym.386c274b-4bfe-4421-9052-a1a56db557ab&pf_rd_p=386c274b-4bfe-4421-9052-a1a56db557ab&pf_rd_r=10KSHERYXGKGCEQWSWRA&pd_rd_wg=VfoNp&pd_rd_r=96fe162c-b09a-4192-ad30-75a81e221bb3&sp_csd=d2lkZ2V0TmFtZT1zcF9kZXRhaWxfdGhlbWF0aWM)  

---

## Goals  
- **Relate OS concepts** directly to a physical system.  
- Show how **scheduling, concurrency, and persistence** work in a constrained environment.  
- Create a practical **sustainability demo** that highlights real-world benefits of efficient resource management.  

---

## Operating Systems Concepts Applied  

- **Processes & Concurrency**  
  - Multiple tasks: sensor readings, logging, fan control, LED control.  
  - Cooperative scheduling ensures fair execution without conflicts.  

- **Synchronization (Locks & Shared Resources)**  
  - Tasks share access to the SD card and serial output.  
  - Mutual exclusion prevents race conditions when writing logs.  

- **Scheduling & Resource Management**  
  - Implements priority-based scheduling (e.g., fan control > logging).  
  - Demonstrates trade-offs between fairness and responsiveness.  

- **Memory Management**  
  - Uses limited Arduino SRAM to buffer sensor data.  
  - Simulates paging by flushing logs to SD card when memory fills.  

- **Persistence (File Systems)**  
  - Data stored on SD card with simple file system operations (create, write, append).  
  - Demonstrates abstraction layer between hardware storage and applications.  

---

## Benefit to Society  
This project highlights how **resource scheduling and energy optimization**—core responsibilities of operating systems—can reduce waste and increase efficiency in the physical world. A small-scale classroom demo can:  
- Teach students the connection between **software resource management** and **energy sustainability**.  
- Encourage sustainable practices by showing data-driven energy control.  
- Serve as a **low-cost IoT-style prototype** for green computing and smart environments.  

---

## ⚙️ Implementation Plan  

1. **Sensor Input**  
   - Temperature sensor (DHT11/DHT22 or similar).  
   - Light sensor (photoresistor).  

2. **Scheduler**  
   - Round-robin baseline.  
   - Priority scheduling (fan > LED > logging).  

3. **Synchronization**  
   - Lock-based mechanism for SD writes.  
   - Shared buffer for storing sensor values.  

4. **Output Devices**  
   - LED: simulates lights controlled for energy savings.  
   - Fan: simulates cooling load.  
   - SD Card: logs environmental readings and decisions.  

---

## 📂 Repository Structure  


# 🌉 What is an API?

> [!info] Definition  
> - An **API (Application Programming Interface)** is a set of rules and protocols that lets different software apps **communicate and exchange data**.  
> - Acts as an **intermediary/bridge**: apps can access functionalities of other systems **without knowing internal workings**.  
> - Example: connects a **client** ↔ **server**.

---

## 🍽️ API Analogy (Restaurant)

- **Menu** = API specification  
- **Waiter** = API interface  
- **Kitchen** = Backend/server  
- **Dish** = Response  

> [!tip] Rules in the analogy  
> - 🚫 Order not on menu → Error  
> - 🔑 Only staff/managers enter kitchen → Permissions/restricted API  
> - 🔗 Restaurant ordering ingredients → One API calling another  

---

## 🌐 Importance of APIs

- 80%+ of modern web apps rely on APIs (login, payments, real-time updates, third-party integrations).  
- Benefits:  
  - ⚡ Faster development (reuse existing functions).  
  - 🔗 Integration across systems.  
  - 🌍 Power modern, scalable, connected software.  

---

## ⚙️ How APIs Work

1. **Request** → Client sends request via API’s **URI**.  
2. **Processing** → API forwards to server.  
3. **Response** → Server processes and sends back data.  
4. **Delivery** → API delivers response to client.  

---

# 🏗️ API Architectures

> [!info] Definition  
> - APIs = “bridge” between systems.  
> - Architectural styles define **data structure, transmission, and consumption**.  
> - Choosing architecture impacts **performance, scalability, security, and integration**.  

**Common Architectures**  
- 🌐 REST (Representational State Transfer)  
- 📜 SOAP (Simple Object Access Protocol)  

---

## 🌐 REST (Representational State Transfer)

- Communication over internet via **requests/responses** (commonly JSON).  
- Uses **HTTP methods** (GET, POST, PUT, PATCH, DELETE) aligned with **CRUD** operations.  
- Request via URL → Server responds with resource (HTML, XML, JSON, etc., JSON most common).  

### 🔑 Key Features
- **Stateless** → Each request contains all required info (no session state).  
- **Client-Server** → Independent operation, scalable.  
- **Cacheable** → Server can mark responses cacheable/non-cacheable.  
- **Uniform Interface** → Standard URLs, methods, status codes.  
- **Layered System** → Multi-layer deployment for scalability & security.  

---

### 📊 HTTP Methods & CRUD

| CRUD Operation | HTTP Method | Example Status Codes |
|----------------|-------------|----------------------|
| Create         | POST        | ✅ 201 Created, 🔗 Location header |
| Read           | GET         | ✅ 200 OK, ❌ 404 Not Found |
| Update         | PUT / PATCH | ✅ 200 OK / 204 No Content |
| Delete         | DELETE      | ✅ 200 OK, ❌ 400 Bad Request |

---

### 🔍 Method Details

> [!tip] **GET**  
> - Retrieve resource.  
> - Returns: 200 (OK) if found, 404 (Not Found) or 400 (Bad Request) on error.  

> [!tip] **POST**  
> - Create new resource (or subordinate resource).  
> - Returns: 201 (Created) + `Location` header.  

> [!tip] **PUT**  
> - Update/replace resource. If not found, may create new one.  

> [!tip] **PATCH**  
> - Partially update resource (send only changed fields).  

> [!tip] **DELETE**  
> - Remove resource by URI.  
> - Returns: 200 (OK) on success.  

---

## 📜 SOAP (Simple Object Access Protocol)

- Network protocol for **structured data exchange**.  
- Uses **XML format** + protocols like **HTTP/SMTP**.  
- Cross-platform & cross-language.  

> [!tip] History  
> - Created in **1998** by Bob Atkinson, Don Box, Dave Winer, Mohsen Al-Ghosein (Microsoft).  
> - Maintained by **W3C XML Protocol Working Group** until 2009.  

---

### 📦 SOAP Message Format

- **Envelope** → Declares it’s a SOAP message.  
- **Header** (optional) → Extra info (auth, routing, etc.).  
- **Body** → Main message & faults.  
- **Fault** (optional) → Errors/status.  

# ✅ Advantages of SOAP

- 🪶 **Lightweight** (XML-based)  
- 💻 **OS & platform-independent**  
- 🌍 **Built on top of widely supported HTTP**  
- 📜 **Backed by W3C (standardized)**  
- 🏢 **Used in enterprise systems** (banking, healthcare, government)  

---

# 🧩 Types of APIs

> [!info] Categories  
> APIs classified by function, application, and communication type.

### 🌐 Web APIs  
- Open-source/public (e.g., Google Maps, Twitter, Weather APIs).

### 💻 Local APIs  
- Interact with local system/software (e.g., TAPI, .NET APIs).

### 📡 Program APIs  
- Abstract remote programs via **RPCs (Remote Procedure Calls).**

---

# 🔄 Other Types

> [!tip] JSON-RPC  
- Lightweight, uses JSON.  
- Procedure-based (direct method calls).  

> [!tip] XML-RPC  
- Early RPC standard, uses XML over HTTP.  
- Platform-independent, verbose but reliable.  

> [!tip] SOAP API  
- Protocol-based, XML messages.  
- Secure, strict standards, used in enterprise.  

> [!tip] REST API  
- Web service conforming to REST.  
- Uses HTTP methods + JSON/XML.  

---

# ✅ Advantages of APIs

> [!success] Benefits  
- ⚡ **Efficiency** → Faster communication, fewer errors.  
- 📱 **Flexibility** → Works across platforms (web, mobile, desktop).  
- 🔗 **Integration** → Modern systems “talk” seamlessly.  
- 🤖 **Automation** → Machines communicate without humans.  
- 🛠️ **New Functionality** → Extend apps via third-party APIs.  
- 📈 **Scalability** → Scale apps by leveraging external services.  

---

# ⚠️ Disadvantages of APIs

> [!danger] Cost  
- Development, maintenance, and usage fees (e.g., Twitter, Google Maps).  
- Can burden startups/small businesses.  

> [!danger] Security  
- Expanded attack surface.  
- Risks:  
  - 🔓 Unauthorized access  
  - 📂 Data breaches  
  - 🌐 DoS attacks  

> [!warning] Third-Party Dependency  
- Provider changes pricing/features or downtime → directly affects your app.  

> [!warning] Integration Complexity  
- Configs, authentication, versioning challenges.  
- Continuous updates required.  

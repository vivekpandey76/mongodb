# 📘 MongoDB Documentation

## 📂 Section 1: Introduction to MongoDB

### 🔍 What is MongoDB?

**MongoDB** is a **NoSQL**, **document-oriented database** designed to store large amounts of unstructured or semi-structured data. It uses a flexible, JSON-like format called BSON (Binary JSON), making it ideal for fast development and scalability.

- Developed by **MongoDB Inc.**
- Known for **high performance**, **scalability**, and **ease of use**
- Great for modern apps, real-time analytics, IoT, and more

---

### 🔁 SQL vs NoSQL (MongoDB)

| Feature           | SQL (Relational DB)        | NoSQL (MongoDB)                    |
|------------------|----------------------------|------------------------------------|
| **Data Model**   | Tables (Rows & Columns)    | Collections (Documents)            |
| **Schema**       | Fixed Schema               | Dynamic Schema (Schema-less)       |
| **Joins**        | Native support             | Manual or `$lookup`                |
| **Transactions** | Fully ACID compliant       | ACID in replica sets (v4.0+)       |
| **Scalability**  | Vertical                   | Horizontal (Sharding)              |
| **Language**     | SQL                        | MongoDB Query Language (MQL)       |

> ✅ Use **SQL** for strict relational data.  
> 🚀 Use **MongoDB** for flexibility, scalability, and high-velocity projects.

---

### 💡 When to Use MongoDB

Choose MongoDB when:
- You need to store **unstructured/semi-structured data**
- Your schema evolves over time
- You want **fast read/write performance**
- You're building:
  - Real-time analytics systems
  - Chat or messaging apps
  - CMS platforms
  - IoT/mobile backend services

---

### 🧱 Core MongoDB Terminologies

| Term          | Meaning |
|---------------|---------|
| **Database**  | A container for collections (like a folder) |
| **Collection**| A group of related documents (like a table) |
| **Document**  | A single record, stored in BSON (like a row) |
| **Field**     | A key-value pair in a document (like a column) |

#### 📄 Example MongoDB Document:
```json
{
  "name": "Jane Doe",
  "email": "jane@example.com",
  "skills": ["Node.js", "MongoDB"],
  "profile": {
    "age": 30,
    "location": "India"
  }
}
```

#### BSON vs JSON

# Overview
MongoDB uses **BSON** (Binary JSON) as its primary data format, while **JSON** (JavaScript Object Notation) is the standard text-based format for data interchange. Below is a detailed comparison:

## Key Differences

| Feature          | JSON                        | BSON                          |
|------------------|----------------------------|-------------------------------|
| **Format**       | Text-based                 | Binary-encoded                |
| **Readability**  | Human-readable             | Machine-optimized             |
| **Data Types**   | Basic types only           | Extended types (Date, BinData)|
| **Size**         | Larger (plaintext)         | Smaller (binary compression)  |
| **Parsing Speed**| Slower (requires parsing)  | Faster (native binary format) |
| **Usage**        | API responses, config files | MongoDB storage format        |

## When to Use Each

### JSON
✔ Human-readable data exchange  
✔ Configuration files  
✔ Web API responses  
✔ When working with frontend applications  

### BSON
✔ MongoDB database storage  
✔ High-performance applications  
✔ When you need extended data types  
✔ Binary data storage  

## Example Comparison

**JSON Example** (Text-based):
```json
{
  "name": "Alice",
  "created_at": "2023-05-20T12:00:00Z",
  "age": 30
}
```

**BSON Equivalent (Binary-encoded):
```json
{
  "name": "Alice",
  "created_at": ISODate("2023-05-20T12:00:00Z"),
  "age": Int32(30)
}
```

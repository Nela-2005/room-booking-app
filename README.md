# Room Booking and Product Management System

This is a full-stack Java Spring Boot application developed during the Java course at **SDA Albania**. It demonstrates backend concepts like REST APIs, CRUD operations, pagination, role-based access control, and dynamic HTML rendering using Thymeleaf.

---

## 📌 Features

### 🏨 Room Booking Module
- Add rooms (admin only)
- Book available rooms (with conflict checking)
- Paginated room listing
- Public and secured endpoints

### 🛒 Product Management Module
- Add, edit, delete products
- Assign products to categories
- Display product list using REST and Thymeleaf (MVC)
- Paginated product listing

### 🧮 Calculator API
- Add, subtract, multiply, divide basic operations exposed as REST endpoints

### 🔐 Security
- In-memory authentication with Spring Security
- Role-based access control: `ADMIN` and `USER`
- HTTP Basic Auth with BCrypt password encryption

---

## 🛠 Technologies Used

- Java 17+
- Spring Boot
- Spring Web, Spring Data JPA
- Spring Security
- Hibernate
- Lombok
- ModelMapper
- Thymeleaf
- H2 Database (in-memory)
- Maven

---

## 🔐 Default Users

| Username | Password   | Role  |
|----------|------------|-------|
| admin    | admin12334 | ADMIN |
| john     | john1234   | USER  |

---

## 📁 Project Structure

com.e_commerce.web_commerce
├── config # Security configuration
├── controller # REST + MVC endpoints
├── dto # Data Transfer Objects
├── entity # JPA Entity Models
├── repository # Spring Data JPA interfaces
├── service # Business logic layer
└── WebCommerceApplication # Main Spring Boot class

pgsql
Copy
Edit

---

## 🔗 API Endpoints

### Booking API
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST   | `/api/booking/rooms` | Add a room (public) |
| POST   | `/api/booking` | Book a room |
| GET    | `/api/booking/rooms` | List rooms (paginated) |

### Admin Booking API
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST   | `/api/admin/rooms` | Add a room (admin-only) |

### Product API
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST   | `/api/products` | Create new product |
| GET    | `/api/products` | Paginated product list |
| GET    | `/api/products/{id}` | Get product by ID |
| GET    | `/api/products/low_stock/{limit}` | (Stub) Low stock alert |

### Product MVC (Thymeleaf HTML Views)
| URL | Description |
|-----|-------------|
| `/products` | View all products |
| `/products/add` | Add a new product (form) |
| `/products/edit-product/{id}` | Edit existing product |

### Calculator API
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET    | `/api/calculator/add?a=5&b=3` | Add two numbers |
| GET    | `/api/calculator/substract` | Subtract |
| GET    | `/api/calculator/multiply` | Multiply |
| GET    | `/api/calculator/divide` | Divide |

---


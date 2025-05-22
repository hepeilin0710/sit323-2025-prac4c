# 🧮 Calculator Microservice – Credit Task Submission

This project is a Node.js-based calculator microservice built using Express.  
It is developed as a submission for **Part I – Credit Task**, with the selection of:

---

## ✅ Option A: Additional Arithmetic Operations

This microservice expands basic calculator functionality by including:

- **Exponentiation** (`/power`)
- **Modulo** (`/modulo`)
- **Square Root** (`/sqrt`)

It also includes essential arithmetic operations:

- Addition
- Subtraction
- Multiplication
- Division

Proper input validation and error handling are included to ensure reliability and robustness.

---


## 📡 API Endpoints

All endpoints use the `POST` method and accept JSON bodies.

---

### ➕ `/add`

**Request:**
```json
{ "num1": 5, "num2": 3 }
```

**Response:**
```json
{ "result": 8 }
```

---

### ➖ `/subtract`

**Request:**
```json
{ "num1": 10, "num2": 4 }
```

**Response:**
```json
{ "result": 6 }
```

---

### ✖️ `/multiply`

**Request:**
```json
{ "num1": 6, "num2": 7 }
```

**Response:**
```json
{ "result": 42 }
```

---

### ➗ `/divide`

**Request:**
```json
{ "num1": 10, "num2": 2 }
```

**Response:**
```json
{ "result": 5 }
```

⚠️ Error if `num2 == 0`

---

### 🧮 `/power`

**Request:**
```json
{ "num1": 2, "num2": 3 }
```

**Response:**
```json
{ "result": 8 }
```

---

### ➰ `/modulo`

**Request:**
```json
{ "num1": 10, "num2": 3 }
```

**Response:**
```json
{ "result": 1 }
```

⚠️ Error if `num2 == 0`

---

### √ `/sqrt`

**Request:**
```json
{ "num": 25 }
```

**Response:**
```json
{ "result": 5 }
```

⚠️ Error if `num < 0`

---

## ❗ Error Handling

### Invalid Input Types

**Request:**
```json
{ "num1": "abc", "num2": 3 }
```

**Response:**
```json
{ "error": "The input parameters num1 and num2 must be numeric types" }
```

---

### Division or Modulo by Zero

**Request:**
```json
{ "num1": 10, "num2": 0 }
```

**Response:**
```json
{ "error": "The divisor cannot be 0" }
```

---

### Negative Square Root

**Request:**
```json
{ "num": -9 }
```

**Response:**
```json
{ "error": "The input to the square root operation cannot be negative." }
```

---

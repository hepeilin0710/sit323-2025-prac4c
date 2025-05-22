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

```json
Request: { "num1": 5, "num2": 3 }
Response: { "result": 8 }
```

---

### ➖ `/subtract`

```json
Request: { "num1": 10, "num2": 4 }
Response: { "result": 6 }
```

---

### ✖️ `/multiply`

```json
Request: { "num1": 6, "num2": 7 }
Response: { "result": 42 }
```

---

### ➗ `/divide`

```json
Request: { "num1": 10, "num2": 2 }
Response: { "result": 5 }
```

⚠️ Error if `num2 == 0`

---

### 🧮 `/power`

```json
Request: { "num1": 2, "num2": 3 }
Response: { "result": 8 }
```

---

### ➰ `/modulo`

```json
Request: { "num1": 10, "num2": 3 }
Response: { "result": 1 }
```

⚠️ Error if `num2 == 0`

---

### √ `/sqrt`

```json
Request: { "num": 25 }
Response: { "result": 5 }
```

⚠️ Error if `num < 0`

---

## ❗ Error Handling

### Invalid Input Types

```json
Request: { "num1": "abc", "num2": 3 }
Response: { "error": "The input parameters num1 and num2 must be numeric types" }
```

---

### Division or Modulo by Zero

```json
Request: { "num1": 10, "num2": 0 }
Response: { "error": "The divisor cannot be 0" }
```

---

### Negative Square Root

```json
Request: { "num": -9 }
Response: { "error": "The input to the square root operation cannot be negative." }
```

---

# SIT737-2025-Prac4C: Enhanced Calculator Microservice

## Overview
This project enhances the calculator microservice from Prac4P for SIT737 Cloud Native Application Development. It includes basic arithmetic operations (addition, subtraction, multiplication, division) and advanced operations (exponentiation, square root, modulo) implemented as REST API endpoints using Node.js, Express, and Winston for logging.

## Features
- REST API endpoints for basic and advanced arithmetic operations
- Input validation and error handling
- Request logging with Winston (console and file output)

## Prerequisites
- Node.js (v14+)
- Git
- Visual Studio Code

# Step-by-Step Process Undertaken

## **Part I: Additional Arithmetic Operations**
This section outlines the steps taken to enhance the **calculator microservice** by adding **new arithmetic operations**, improving **error handling**, and integrating **logging mechanisms**.

### **Step 1: Use Previous Calculator App as Base**
- The existing **calculator microservice** from **Prac4P** was used as the foundation.
- Reviewed its current structure, including:
  - API endpoints (`/add`, `/subtract`, `/multiply`, `/divide`)
  - Error handling methods
  - Logging setup using **Winston**
- Confirmed that the existing functionality was stable before adding new features.

### **Step 2: Identify New Functionalities to Add**
- Decided to add three new arithmetic operations:
  1. **Exponentiation (`power`)**: Computes `base^exp`
  2. **Square Root (`sqrt`)**: Returns the square root of a number
  3. **Modulo (`modulo`)**: Returns the remainder of division
- Evaluated potential edge cases:
  - **Negative input for `sqrt`**
  - **Zero divisor in `modulo`**
  - **Large exponent values in `power`**

### **Step 3: Install and Verify Existing Dependencies**
- Verified the installation of:
  - **Express.js** for handling API requests
  - **Winston** for logging requests and errors
  - **Jest** for unit testing
- Used `npm install` to ensure all necessary dependencies were present.

### **Step 4: Design New API Endpoints**
- Planned **three new REST API endpoints**:
  - `GET /power?base=2&exp=3` → Returns **8** (`2^3`)
  - `GET /sqrt?num=9` → Returns **3**
  - `GET /modulo?a=10&b=3` → Returns **1**
- Defined required query parameters:
  - `/power`: Requires **base** and **exp**
  - `/sqrt`: Requires **num** (must be ≥ 0)
  - `/modulo`: Requires **a** and **b** (b ≠ 0)

### **Step 5: Implement New Endpoints in Existing App**
- Added the following logic to `server.js`:
  - `power`: Uses `Math.pow(base, exp)`
  - `sqrt`: Uses `Math.sqrt(num)`
  - `modulo`: Uses the `%` operator
- Ensured all endpoints returned JSON responses:
  ```json
  { "operation": "power", "result": 8 }


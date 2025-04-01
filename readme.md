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

## Step-by-Step Process Undertaken

### Part I: Additional Arithmetic Operations
1. **Use Previous Calculator App as Base**:  
   - I started with the calculator microservice from Prac4P, which I had previously developed with Node.js, Express, and Winston logging.  
   - I cloned the existing repository (`sit737-2025-prac4p`) to reuse its structure and functionality as the foundation for this enhancement:  
     ```bash
     git clone https://github.com/s223623837/sit737-2025-prac4p.git sit737-2025-prac4c
     cd sit737-2025-prac4c

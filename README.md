# yellow-bank-ai-agent
Gen AI Banking Agent built using Yellow.ai to authenticate users and fetch loan details using workflows, mock APIs, and dynamic UI components.

# 🏦 Yellow Bank AI Agent

## 📌 Overview

This project is a Gen AI Banking Agent built using the Yellow.ai platform.
The agent helps users securely view their loan details through authentication, API workflows, and dynamic UI components.

---

## 🎯 Objective

* Authenticate users using Phone Number, DOB, and OTP
* Fetch loan accounts and loan details
* Optimize API data using projection
* Provide a smooth conversational experience
* Collect user feedback using CSAT

---

## ⚙️ Tech Stack

* Yellow.ai (Bot Development)
* Beeceptor (Mock APIs)
* JSON (API Responses)

---

## 🔄 Flow Architecture

1. User asks for loan details
2. Bot collects Phone Number and DOB
3. OTP is generated via mock API
4. User enters OTP → verification
5. Fetch loan accounts (Workflow A)
6. Display loan accounts using cards
7. User selects a loan account
8. Fetch loan details (Workflow B)
9. Display details with quick replies
10. Collect feedback (CSAT)

---

## 🔌 Mock APIs

### 1. OTP API

**Endpoint:** `/triggerOTP`
**Method:** POST

**Response:**

```json
{
  "status": "success",
  "otp": "1234"
}
```

---

### 2. Loan Accounts API

**Endpoint:** `/getLoanAccounts`
**Method:** GET

**Response:**

```json
{
  "status": "success",
  "data": [
    {
      "loan_account_id": "LA001",
      "loan_type": "Home Loan",
      "tenure": "20 years",
      "internal_code": "INT123",
      "audit_date": "2023-01-01"
    }
  ]
}
```

---

### 3. Loan Details API

**Endpoint:** `/loanDetails`
**Method:** POST

**Response:**

```json
{
  "status": "success",
  "data": {
    "tenure": "20 years",
    "interest_rate": "8.5%",
    "principal_pending": "500000",
    "interest_pending": "50000",
    "nominee": "Ravi Kumar"
  }
}
```

---

## 🚀 Key Features

### 🔐 Authentication Flow

* Phone Number + DOB validation
* OTP verification with retry logic

### ⚡ Token Optimization

* Used projection to filter only required fields
* Reduced unnecessary API data processing

### 🎴 Dynamic UI (DRM)

* Loan accounts displayed as interactive cards
* Easy selection for users

### 🔁 Edge Case Handling

* Incorrect OTP handling
* Invalid inputs
* Change phone number flow reset
* API failure handling

### ⭐ CSAT Feedback

* Rating options: Good / Average / Bad
* User feedback collection

---

## 🌐 Language Restriction

The agent supports only English.
If the user inputs another language, the bot responds politely.

---

## 📽️ Demo

(Add your screen recording link here)

---

## 👤 Author

Sriram Reddy

---

## 📌 Note

All APIs are mocked using Beeceptor. No real backend is used.

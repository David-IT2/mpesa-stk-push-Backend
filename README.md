
# M-Pesa STK Push Backend Integration

A backend application that integrates with Safaricom Daraja API to initiate and handle M-Pesa STK Push payments. Users enter their phone number and receive a payment prompt on their device.

## Features

* Initiate STK Push requests
* Generate access tokens from Daraja API
* Secure API authentication
* Callback handling for payment confirmation
* Transaction tracking
* Error handling and logging

## ⚙️ Prerequisites

* Safaricom Daraja API credentials:

  * Consumer Key
  * Consumer Secret
  * Shortcode
  * Passkey


##  API Endpoints

### 1. Initiate STK Push

POST /api/mpesa/stkpush

Request Body:

{
"phone": "2547XXXXXXXX",
"amount": 100
}

Response:

{
"message": "STK Push sent successfully"
}

---

### 2. Callback URL

POST /api/mpesa/callback

This endpoint receives payment confirmation from Safaricom.

## 🔄 STK Push Flow

1. User submits phone number and amount
2. Backend generates access token
3. STK Push request sent to Safaricom
4. User receives prompt on phone
5. User enters PIN
6. Safaricom sends response to callback URL
7. Backend processes and stores transaction

##  Authentication (Daraja API)

GET /oauth/v1/generate?grant_type=client_credentials

Use Basic Auth with Consumer Key and Consumer Secret.



sing logic
* Or complete working project 🚀

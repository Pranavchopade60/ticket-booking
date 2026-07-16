# 🎟 AWS Movie Booking System

A modern cloud-based **Movie Ticket Booking System** built using **Amazon EC2, AWS Lambda, Amazon API Gateway, Amazon DynamoDB, Amazon SNS, HTML, CSS, and JavaScript**. The application enables users to browse movies, select seats, book tickets, and receive booking confirmations through a fully serverless backend.

---

## 🚀 Live Demo

**Hosted on Amazon EC2**

```
http://YOUR-EC2-PUBLIC-IP
```

---

# 📸 Screenshots

## Home Page

![Home](screenshots/home.png)

---

## Movies

![Movies](screenshots/movies.png)

---

## Seat Selection

![Seats](screenshots/seat-booking.png)

---

## Booking Confirmation

![Booking](screenshots/booking-confirmation.png)

---

## Booking History

![History](screenshots/history.png)

---

# ✨ Features

- Browse Available Movies
- View Movie Details
- Interactive Seat Selection
- Real-Time Seat Availability
- Prevent Double Booking using DynamoDB
- Book Movie Tickets
- Booking Confirmation
- Email Notifications using Amazon SNS
- Responsive User Interface
- REST API Integration
- Cloud Hosted Frontend
- Serverless Backend
- Fast and Secure Booking Process

---

# 🏗 Architecture

```
User Browser
      │
      ▼
Amazon EC2 (Apache Web Server)
      │
      ▼
Amazon API Gateway
      │
      ▼
AWS Lambda
      │
      ▼
Amazon DynamoDB
      │
      ├────────────► Amazon SNS
      │                  │
      ▼                  ▼
 Seat Booking Data   Email Notification
```

---

# ☁️ AWS Services Used

- Amazon EC2
- AWS Lambda
- Amazon API Gateway
- Amazon DynamoDB
- Amazon SNS
- AWS IAM
- Amazon CloudWatch

---

# 💻 Tech Stack

## Frontend

- HTML5
- CSS3
- JavaScript (Vanilla)

## Backend

- Python
- AWS Lambda

## Database

- Amazon DynamoDB

## Cloud

- Amazon EC2
- Amazon API Gateway
- Amazon SNS
- AWS IAM
- Amazon CloudWatch

---

# 📁 Project Structure

```
Movie-Booking-System
│
├── frontend
│   ├── index.html
│   ├── movies.html
│   ├── booking.html
│   ├── confirmation.html
│   ├── css
│   ├── js
│   └── assets
│
├── lambda
│   ├── bookTicket.py
│   ├── getMovies.py
│   ├── getSeats.py
│   └── bookingHistory.py
│
├── screenshots
│   ├── home.png
│   ├── movies.png
│   ├── seat-booking.png
│   ├── booking-confirmation.png
│   └── history.png
│
└── README.md
```

---

# ⚙️ API Endpoints

## Get Movies

```
GET /movies
```

---

## Get Seat Availability

```
GET /seats?movieId=101
```

---

## Book Ticket

```
POST /book
```

Request Body

```json
{
    "movieId": "101",
    "seatId": "A5",
    "username": "John",
    "email": "john@example.com"
}
```

---

## Booking History

```
GET /history
```

---

# 🎯 Booking Workflow

1. Browse available movies.
2. Select a movie.
3. Choose preferred seats.
4. Check seat availability.
5. Confirm booking.
6. Store booking in DynamoDB.
7. Send confirmation through Amazon SNS.
8. Display booking success message.

---

# 🚀 Deployment

The frontend is hosted on an Ubuntu EC2 instance using the Apache Web Server.

The backend APIs are deployed on AWS Lambda and exposed through Amazon API Gateway.

Booking information is securely stored in Amazon DynamoDB.

Amazon SNS is used to send booking confirmation notifications.

Amazon CloudWatch is used for monitoring Lambda execution and API logs.

---

# 🔐 IAM Permissions

The Lambda execution role includes permissions for:

- dynamodb:GetItem
- dynamodb:PutItem
- dynamodb:UpdateItem
- dynamodb:Scan
- sns:Publish
- logs:CreateLogGroup
- logs:CreateLogStream
- logs:PutLogEvents

---

# 📦 Installation

Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/Movie-Booking-System.git
```

Navigate to the project

```bash
cd Movie-Booking-System
```

Deploy the frontend files to an Apache web server or Amazon EC2.

Deploy the Lambda functions.

Create a DynamoDB table for bookings.

Configure Amazon SNS.

Create API Gateway endpoints.

Update the API endpoint URLs inside the frontend JavaScript files.

Launch the application.

---

# 🔮 Future Improvements

- User Authentication using Amazon Cognito
- Online Payment Gateway Integration
- QR Code Ticket Generation
- Admin Dashboard
- Movie Search and Filters
- Booking Cancellation
- Refund Management
- Multi-Theatre Support
- Movie Reviews and Ratings
- Booking Analytics Dashboard
- Mobile Responsive PWA
- SMS Notifications
- Seat Recommendation System

---

# 👨‍💻 Author

**Pranav Chopade**

GitHub

https://github.com/YOUR_USERNAME

---

# ⭐ Support

If you found this project helpful, please consider giving it a **⭐ Star** on GitHub.

# Event Announcement System 📢

A serverless event announcement platform built with AWS and modern web technologies.

![License](https://img.shields.io/badge/license-MIT-blue.svg) ![AWS](https://img.shields.io/badge/AWS-Serverless-orange)

## 🏗️ Architecture

This project leverages a serverless architecture to ensure scalability and cost-efficiency.

```mermaid
graph LR
    User[👤 User] -->|View Events| Web[🌐 Static Website (S3)]
    User -->|Subscribe| API[🚪 API Gateway]
    User -->|Create Event| API
    
    API -->|Trigger| Lambda[λ Lambda Functions]
    
    Lambda -->|Store/Retrieve| DB[(DynamoDB/JSON)]
    Lambda -->|Publish| SNS[📢 SNS Topic]
    
    SNS -->|Notify| Email[📧 Email Subscribers]
```

## ✨ Features

- **Browse Events**: View upcoming events with details.
- **Create Events**: Admin interface to post new event announcements.
- **Subscribe**: Users can subscribe via email to receive instant notifications (powered by AWS SNS).
- **Responsive Design**: optimized for both desktop and mobile devices.

## 🛠️ Technologies

- **Frontend**: HTML5, CSS3, JavaScript (Vanilla)
- **Backend**: AWS Lambda (Node.js/Python)
- **API**: AWS API Gateway
- **Notifications**: Amazon SNS (Simple Notification Service)
- **Hosting**: AWS S3 (Static Website Hosting)

## 🚀 Getting Started

### Prerequisites

- A modern web browser
- (Optional) AWS Account for backend deployment

### Local Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/Sosthenes-arch/Event-Announcement-System-using-SNS-Lambda-and-API-Gateway.git
   ```
2. Navigate to the project directory:
   ```bash
   cd Event-Announcement-System-using-SNS-Lambda-and-API-Gateway
   ```
3. Open `index.html` in your browser.

> **Note**: To make the "Subscribe" and "Create Event" features functional, you must replace the placeholder API endpoints in `index.html` with your deployed AWS API Gateway URLs.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is open source and available under the MIT License.

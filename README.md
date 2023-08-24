# AeroVerve - Reminder Microservice

Welcome to the Reminder Microservice of the AeroVerve. This microservice handles email notifications and reminders for flight bookings within the larger AeroVerve. It uses an MVC (Model-View-Controller) architecture and integrates with a message broker for asynchronous communication.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Scheduled Jobs](#scheduled-jobs)
- [Message Queue](#message-queue)
- [Contributing](#contributing)
- [License](#license)

## Introduction

The Reminder Microservice is a crucial part of the AeroVerve, responsible for managing email notifications and reminders for flight bookings. It interacts with Nodemailer for sending emails, Sequelize for database operations, and a message broker (like RabbitMQ) for communication with other microservices.

## Features

- Send email reminders for flight bookings.
- Utilize Nodemailer for email sending functionality.
- Integrate with a message broker for asynchronous communication.
- Utilize Sequelize for database operations related to email reminders.

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/SudoKMaar/aeroverve-reminder-service.git
   cd aeroverve-reminder-service
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

## Configuration

1. Configure environment variables:

   Create a `.env` file in the root directory and set the required values:

   ```env
   PORT=4003
   EMAIL_ID=your_email@gmail.com
   EMAIL_PASS=your_email_app_password
   MESSAGE_BROKER_URL=rabbitmq://localhost
   EXCHANGE_NAME=booking_exchange
   REMINDER_BINDING_KEY=booking_reminder
   ```

2. Update `config/config.json` with your database settings.

## Usage

1. Start the microservice:

   ```bash
   npm start
   ```

2. Access the microservice's functionality via appropriate routes.

## API Endpoints

- `POST /api/v1/tickets`: Create a new email reminder for a flight booking.

## Scheduled Jobs

The microservice employs scheduled jobs to manage pending email notifications. The jobs run at intervals to check for pending emails and send them accordingly.

## Message Queue

The microservice uses a message broker (e.g., RabbitMQ) to communicate asynchronously with other microservices. It subscribes to relevant events and publishes messages when required.

## Contributing

Contributions are welcome! Feel free to open issues or pull requests related to the Reminder Microservice.

## License

This project is licensed under the [MIT License](LICENSE).

---

AeroVerve - Elevating Flight Booking Experiences

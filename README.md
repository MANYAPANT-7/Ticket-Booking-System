# Ticket Booking System

## Overview
The Ticket Booking System is a Python application that allows users to book tickets for various events, view existing bookings, modify bookings, and cancel bookings. It utilizes a MySQL database to store and manage booking data efficiently.

## Features
- **Book Tickets:** Users can book tickets for different events by entering event details, customer name, number of tickets, and the booking date.
- **View Bookings:** Users can view all current bookings with details such as event name, customer name, number of tickets, and booking date.
- **Modify Bookings:** Users can modify existing bookings, including changing the event name and the number of tickets.
- **Cancel Bookings:** Users can cancel their bookings by providing the booking ID.
- **Database Integration:** The application connects to a MySQL database to store booking information securely.

## Technologies Used
- Python
- MySQL
- `mysql-connector-python` library for database interaction

## Requirements
- Python 3.x
- MySQL Server
- MySQL Connector for Python

## Setup Instructions

### Database Setup
1. **Install MySQL Server** if you haven't already.
2. **Create the Database and Table:**
   - Run the following SQL commands in your MySQL Workbench or any SQL client:

   ```sql
   -- Create the TicketBooking database
   CREATE DATABASE TicketBooking;

   -- Use the TicketBooking database
   USE TicketBooking;

   -- Create the Tickets table
   CREATE TABLE Tickets (
       booking_id INT AUTO_INCREMENT PRIMARY KEY,
       event_name VARCHAR(255) NOT NULL,
       customer_name VARCHAR(255) NOT NULL,
       num_tickets INT NOT NULL CHECK (num_tickets > 0),
       booking_date DATE NOT NULL,
       created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
   );
```
3. Clone the repository or download the project files.
4. Install Required Libraries: Make sure you have mysql-connector-python installed. You can install it using pip:
```Python
pip install mysql-connector-python
```
## Usage Instructions
Upon launching the application, users will be presented with a menu with options to book a ticket, view bookings, modify bookings, cancel bookings, or exit the application.
Follow the prompts to complete your desired action.
## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Contributing
Contributions are welcome! Please open an issue or submit a pull request for any enhancements or bug fixes.

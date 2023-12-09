# Backend:

This is the frontend part of my, "Restaurant Reservation App" which is built with Node.js and Express, offering a robust API for the seamless handling of restaurant reservations and table management.

## Features

- Comprehensive API endpoints for reservations and table management.
- Secure request processing with validation and error handling.

  Backend: [Restaurant Reservations Backend](https://restaurant-reservations-capstone-b.onrender.com) <
  Frontend: [Restaurant Reservations Frontend](https://restaurant-reservations-capstone-f.onrender.com) <

## Installation

1. Clone the repository.
2. Navigate to the backend directory.
3. Run `npm install` to install dependencies.
4. Start the server using `npm start`.

## API Documentation

- This document provides an overview of the back-end functionalities, API endpoints, and instructions for setup and execution. 

## Endpoints

### List Reservations
- **Endpoint**: `/reservations`
- **Method**: `GET`
- **Description**: Retrieves all existing reservations.
- **Query Parameters**: 
  - `date`: The date to filter reservations (optional).
- **Returns**: An array of reservation objects.

### Create Reservation
- **Endpoint**: `/reservations`
- **Method**: `POST`
- **Description**: Posts a new reservation to the reservations page.
- **Body**: Reservation object.
- **Returns**: The created reservation object.

### List Tables
- **Endpoint**: `/tables`
- **Method**: `GET`
- **Description**: Returns all tables.
- **Returns**: An array of table objects.

### Create Table
- **Endpoint**: `/tables`
- **Method**: `POST`
- **Description**: Posts a new table to the tables page.
- **Body**: Table object.
- **Returns**: The created table object.

### Read Reservation
- **Endpoint**: `/reservations/:reservationId`
- **Method**: `GET`
- **Description**: Retrieves a reservation by its ID.
- **URL Parameters**:
  - `reservationId`: The ID of the reservation.
- **Returns**: The reservation object.

### Edit Reservation
- **Endpoint**: `/reservations/:reservationId`
- **Method**: `PUT`
- **Description**: Updates data for a given reservation.
- **URL Parameters**:
  - `reservationId`: The ID of the reservation to update.
- **Body**: Updated reservation object.
- **Returns**: The updated reservation object.

### Update Reservation Status
- **Endpoint**: `/reservations/:reservationId/status`
- **Method**: `PUT`
- **Description**: Updates the status of a reservation.
- **URL Parameters**:
  - `reservationId`: The ID of the reservation to update.
- **Body**: Status update object.
- **Returns**: The updated reservation object.

### Finish Table
- **Endpoint**: `/tables/:tableId/seat`
- **Method**: `DELETE`
- **Description**: Removes a table from the seating page.
- **URL Parameters**:
  - `tableId`: The ID of the table to finish.
- **Returns**: Confirmation of the operation.

### Seat Table
- **Endpoint**: `/tables/:tableId/seat`
- **Method**: `PUT`
- **Description**: Updates the table status and displays it in the tables list.
- **URL Parameters**:
  - `tableId`: The ID of the table to update.
- **Body**: Reservation ID for seating.
- **Returns**: Confirmation of the operation.

### Example POST /api/reservations Request

```json
{
    "reservation_date": "2023-12-10",
    "reservation_time": "18:00",
    "people": 4,
    "customer_name": "John Doe"
}

### Example Response

{
    "reservation_id": 123,
    "reservation_date": "2023-12-10",
    "reservation_time": "18:00",
    "people": 4,
    "customer_name": "John Doe",
    "status": "booked"
}

### Note
 ♦ For more in depth [README.md](https://github.com/Thinkful-Ed/starter-restaurant-reservation/blob/main/README.md) with the structure and initial frameworkbehind the application.

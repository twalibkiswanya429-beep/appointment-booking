# Data Dictionary: Appointment Booking System

## 1. Customers Table
 purpose: Stores client contact details.
* customer_id (INT, Primary key)- are unique identifiers for the customer.

* full-name (VARCHAR, NOT NULL)- Name of the customer.

* phone_number (VARCHER, NOT NULL)- Contact number.

* email (VARCHER,Optional )- email address.

## 2. Service Table
* purpose: outlines  the types of services available for booking.

* service_id (INT, Primary key)- Unique identifier for the service

* Service_name (VARCHER, NOT NULL)- Name of the service.

* duration_time (INT, NOT NULL)- Expected length of time for the service.

* price (DECIMAL,(10, 2), NOT NULL)- Cost of the service.

## 3. Staff table
* purpose: Stores internal staff members who handle appointments.

* staff_id (INT, PRIMARY KEY)- Unique identifier for the staff member.

* staff_name (VARCHAR, NOT NULL)- Full name of the staff member.

* phone_number (VARCHAR, NOT NULL)- staff contact number.

## 4. Appointments Table
* purpose: Records the scheduling link between customers, services and staff.

* appointment_id (INT, Primary key)- Unique identifier for the appointment record.

* customer_id (INT, foreign key, customers.customer_id, NOT NULL)- The client booking the slot.

* service_id (INT, foreign key referencing services.service_id, NOT NULL)- The service requested.

* staff_id (INT, foreign key referencing staff.staff_id, NOT NULL)- The assigned staff member.

* appointment_date (DATETIME, NOT NULL)- scheduled date and time.

* status (VARCHAR, NOT NULL, Default: 'pending')- current status (pending, confirmed, completed, cancelled).


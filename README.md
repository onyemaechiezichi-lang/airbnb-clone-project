# Airbnb Clone Project

## Overview
This project aims to replicate the core functionalities of the Airbnb platform, providing users with the ability to search for and book accommodations, as well as host listings.

## Project Goals
- Develop a user-friendly interface for searching and booking accommodations.
- Implement user authentication and profiles.
- Allow hosts to create and manage their listings.
- Integrate a payment system for transactions.

## Tech Stack
- **Frontend**: HTML, CSS, JavaScript, React
- **Backend**: Node.js, Express
- **Database**: MongoDB
- **Authentication**: JWT (JSON Web Tokens)

## Team Roles

### Backend Developer
Responsible for server-side application logic and integration. The backend developer will create APIs, manage server-side logic, and ensure data flow between the server and client.

### Frontend Developer
Focuses on the user interface and experience. The frontend developer will implement the design, ensuring that the application is responsive and user-friendly.

### Database Administrator
Manages the database infrastructure. The database administrator is responsible for database design, optimization, and maintenance, ensuring data integrity and performance.

### UI/UX Designer
Handles the design aspects of the project, focusing on user experience and interface design. The UI/UX designer will create wireframes and prototypes to enhance usability.

### Project Manager
Oversees the project timeline, resources, and team collaboration. The project manager ensures that the project stays on track and meets its goals.

### Quality Assurance Tester
Responsible for testing the application to identify bugs and ensure quality. The QA tester will develop test cases and perform manual and automated tests to validate functionalities.

## Database Design

### Key Entities

1. **Users**
   - **Fields**:
     - `user_id`: Unique identifier for each user.
     - `name`: Full name of the user.
     - `email`: User's email address.
     - `password`: Hashed password for authentication.
     - `role`: Role of the user (e.g., guest, host).
   - **Relationships**: A user can have multiple properties and bookings.

2. **Properties**
   - **Fields**:
     - `property_id`: Unique identifier for each property.
     - `user_id`: Foreign key referencing the owner (User).
     - `location`: Address or location of the property.
     - `price_per_night`: Cost of staying per night.
     - `description`: Brief description of the property.
   - **Relationships**: A property belongs to one user and can have multiple bookings and reviews.

3. **Bookings**
   - **Fields**:
     - `booking_id`: Unique identifier for each booking.
     - `property_id`: Foreign key referencing the booked property.
     - `user_id`: Foreign key referencing the user who made the booking.
     - `start_date`: Start date of the booking.
     - `end_date`: End date of the booking.
   - **Relationships**: A booking belongs to one property and one user.

4. **Reviews**
   - **Fields**:
     - `review_id`: Unique identifier for each review.
     - `property_id`: Foreign key referencing the reviewed property.
     - `user_id`: Foreign key referencing the user who wrote the review.
     - `rating`: Rating given by the user (e.g., 1 to 5 stars).
     - `comment`: Textual feedback about the property.
   - **Relationships**: A review belongs to one property and one user.

5. **Payments**
   - **Fields**:
     - `payment_id`: Unique identifier for each payment.
     - `booking_id`: Foreign key referencing the associated booking.
     - `amount`: Total amount paid.
     - `payment_date`: Date when the payment was made.
     - `payment_method`: Method used for payment (e.g., credit card, PayPal).
   - **Relationships**: A payment is linked to one booking.

## Technology Stack

- **HTML**: The standard markup language used to create the structure of web pages.
- **CSS**: A style sheet language used for describing the presentation of the document written in HTML.
- **JavaScript**: A programming language used to create dynamic content and interactive features on web pages.
- **React**: A JavaScript library for building user interfaces, allowing for component-based architecture for reusable UI elements.
- **Node.js**: A JavaScript runtime built on Chrome's V8 engine, used for building scalable server-side applications.
- **Express**: A web application framework for Node.js, designed for building APIs and web applications with minimal setup.
- **MongoDB**: A NoSQL database that stores data in flexible, JSON-like documents, allowing for easy scalability and high performance.
- **JWT (JSON Web Tokens)**: An open standard used for securely transmitting information between parties as a JSON object, commonly used for authentication and information exchange.

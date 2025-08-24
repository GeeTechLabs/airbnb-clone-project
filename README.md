# Airbnb Clone (Backend – Django)

## Overview
A backend-focused Airbnb clone built with **Django**, aiming to support user registration/login, property listings, bookings, reviews, and payments. This project practices professional backend workflows: clean architecture, robust database design, secure APIs, and CI/CD.

## Project Goals
- Ship a production-ready Django backend.
- Model core domain entities (Users, Properties, Bookings, Reviews, Payments).
- Provide well-documented APIs (GraphQL and/or REST) for the frontend.
- Enforce strong security (auth, permissions, rate limiting).
- Use CI/CD to automate testing and deployment.

## Tech Stack (initial)
- **Django** (Python web framework)
- **PostgreSQL** (relational database)
- **GraphQL** (flexible data query layer; optional REST for utility/endpoints)
- **Docker** (containerized dev/prod environments)
- **GitHub Actions** (CI/CD for tests and deployments)


## Team Roles

- **Backend Developer**  
  Responsible for implementing Django models, views, serializers, and APIs. Ensures business logic is correct, scalable, and maintainable.  

- **Database Administrator (DBA)**  
  Designs and manages the PostgreSQL database schema. Handles migrations, indexing, backups, and ensures data consistency.  

- **DevOps Engineer**  
  Manages CI/CD pipelines, Docker environments, and deployment. Ensures smooth integration and reliable delivery of the application.  

- **QA Engineer**  
  Creates and runs tests (unit, integration, end-to-end). Ensures APIs meet requirements, catches bugs early, and validates overall system quality.  

- **Project Manager**  
  Coordinates team activities, tracks progress, manages deadlines, and ensures alignment with project goals.  

  ## Technology Stack
- **Django**: Python web framework used to build scalable APIs and manage business logic.  
- **PostgreSQL**: Relational database to store structured data like users, properties, and bookings.  
- **GraphQL**: API query language enabling flexible data fetching for frontend clients.  
- **Docker**: Containerization to provide consistent environments across development and production.  
- **GitHub Actions**: Automation for CI/CD, including testing and deployment pipelines.  

---
## Database Design
Key entities and relationships:

- **Users**  
  - Fields: `id`, `username`, `email`, `password`, `role`  
  - A user can be a host (property owner) or a guest (renter).  

- **Properties**  
  - Fields: `id`, `title`, `description`, `location`, `price`, `host_id`  
  - A property belongs to a host (user).  

- **Bookings**  
  - Fields: `id`, `user_id`, `property_id`, `check_in`, `check_out`, `status`  
  - A booking is made by a user for a property.  

- **Reviews**  
  - Fields: `id`, `user_id`, `property_id`, `rating`, `comment`  
  - A user can leave a review for a property they booked.  

- **Payments**  
  - Fields: `id`, `booking_id`, `amount`, `status`, `payment_date`  
  - A payment is linked to a booking.  

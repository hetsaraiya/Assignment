# Vendor Management System (VMS)

Welcome to the Vendor Management System (VMS) repository! This application is designed to help you manage vendors, track purchase orders, and evaluate vendor performance.

## Table of Contents

- [Project Overview](#project-overview)
- [Features](#features)
- [Deployment](#deployment)
- [Getting Started](#getting-started)
- [API Endpoints](#api-endpoints)

## Project Overview

The Vendor Management System (VMS) is a Django application that provides a comprehensive solution for managing vendors and purchase orders. It includes features such as vendor profile management, purchase order tracking, and vendor performance evaluation.

## Features

- **Vendor Profile Management:** Create, update, delete, and retrieve vendor profiles.
- **Purchase Order Tracking:** Create, update, delete, and retrieve purchase orders, and acknowledge purchase orders.
- **Vendor Performance Evaluation:** Retrieve vendor performance metrics such as on-time delivery rate, quality rating, and fulfillment rate.

## Deployment

The application has been deployed on an AWS EC2 instance using Gunicorn and Nginx. The project can be accessed at [http://3.110.185.255/](http://3.110.185.255/).

## Getting Started

To run the application locally, follow these steps:

1. Clone this repository:
   ```shell
   git clone [REPOSITORY_URL]
   cd [REPOSITORY_NAME]

2. Create and activate a virtual environment:
    ```shell
    python3 -m venv venv
    source venv/bin/activate

3. Install the required dependencies:
    ```shell
    pip install -r requirements.txt

4. Apply migrations and create a superuser:
    ```shell
    python manage.py makemigrations
    python manage.py migrate
    python manage.py createsuperuser

5. Run the Django development server:
    ```shell
    python manage.py runserver

## api-endpoints
API Endpoints
Here are some of the key API endpoints:

6. Vendor Endpoints:

   POST /api/vendors/: Create a new vendor.

   GET /api/vendors/: List all vendors.

   GET /api/vendors/{vendor_id}/: Retrieve a specific vendor's details.

   PUT /api/vendors/{vendor_id}/: Update a vendor's details.

   DELETE /api/vendors/{vendor_id}/: Delete a vendor.

7. Purchase Order Endpoints:

   POST /api/purchase_orders/: Create a purchase order.

   GET /api/purchase_orders/: List all purchase orders, with optional filtering by vendor.

   GET /api/purchase_orders/{po_id}/: Retrieve details of a specific purchase order.

   PUT /api/purchase_orders/{po_id}/: Update a purchase order.

   DELETE /api/purchase_orders/{po_id}/: Delete a purchase order.

   POST /api/purchase_orders/{po_id}/acknowledge/: Acknowledge a purchase order.

8. Vendor Performance Endpoint:

   GET /api/vendors/{vendor_id}/performance/: Retrieve a vendor's performance metrics.
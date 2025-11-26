# Railway Reservation System

A web-based Railway Reservation System that allows users to search trains, check seat availability, book tickets, cancel tickets, and view booking history.  
Admins can manage trains, schedules, fares, and monitor bookings.

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Database Design](#database-design)
  
---

## Overview

The **Railway Reservation System** is a mini-project built as part of a Software Engineering / SDLC-based assignment.  
It demonstrates:

- Requirements gathering  
- System design  
- Implementation  
- Testing  
- Project management using Jira, Confluence, and GitHub  

This repository contains the **source code** and associated configuration files.

---

## Features

### User

- User registration & login
- Search trains by source, destination, and date
- View seat availability for selected trains
- Book tickets (select class, number of seats, etc.)
- Generate ticket with unique **PNR**
- View booking history
- Cancel booked tickets

### Admin

- Add / update / delete train details
- Manage train schedules (arrival, departure, route)
- Set and update fares & seat quotas
- View booking reports

---

## Tech Stack

- **Frontend:** HTML, CSS, JavaScript (or React / Angular / Vue)
- **Backend:** Node.js / Express (or Java / Spring / Python / PHP)
- **Database:** MySQL / PostgreSQL
- **Tools:** Jira, Confluence, GitHub
- **Other:** REST APIs, MVC / 3-tier architecture

---

## Database Design

- **users**: `user_id`, `name`, `email`, `password`, `phone`
- **trains**: `train_id`, `train_name`, `source`, `destination`
- **schedules**: `schedule_id`, `train_id`, `date`, `departure_time`, `arrival_time`
- **seats**: `seat_id`, `train_id`, `class`, `total_seats`, `available_seats`
- **bookings**: `booking_id`, `user_id`, `train_id`, `schedule_id`, `seat_count`, `pnr`, `status`
- **payments**: `payment_id`, `booking_id`, `amount`, `status`
- **cancellations**: `cancel_id`, `booking_id`, `refund_amount`, `cancel_date`

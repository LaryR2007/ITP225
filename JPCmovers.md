# JPC Best Movers - Reservation System

## Overview

This is a web-based reservation system built with Django for **JPC Best Movers**, my father's moving company. It allows clients to view services, make moving reservations, and receive confirmation via email. It also gives admin users full control over managing these reservations.

## What It Does

- Lets clients:
  - View all moving services we offer
  - Choose a service, number of workers, and hours needed
  - Pick a move date and time
  - See the total price before booking
  - Receive an email confirmation after booking

- Lets admins (aka me and dad):
  - Add, edit, or remove services
  - View all reservations
  - Edit or cancel reservations
  - Manage pricing based on worker count and hours

- Sends automatic email confirmations to both the client and the company when a reservation is made.
- Includes checks to make sure email is valid and required.
- Adds the company logo and contact info to email messages.

## How It Works

- Services are added by the admin through the Django admin dashboard.
- Clients visit the site, choose a service, fill out a form with their info, and submit it.
- The system calculates the total cost based on how many workers and how many hours they choose.
- Clients are shown a success page and receive an email with all the reservation details.
- Admins can view and manage all reservations in the dashboard.

## Technologies Used

- Python
- Django
- HTML, CSS, JavaScript
- SQLite (for the database)
- Gmail SMTP (for sending emails)

## Why I Built It

I built this to help my dad manage reservations for his moving company more easily. Instead of doing everything by phone or paper, this website lets clients book online and helps us stay organized.
# ClinicFlow V1 - Technical Architecture

Version: 1.0

---

# Objective

Build a simple, low-cost AI-powered appointment booking system for clinics.

The architecture should be:

- Easy to maintain
- Easy to customize for different clinics
- Low cost
- Fast to develop
- Scalable enough for future improvements

---

# Technology Stack

## Website

Technology:
React + Vite

Purpose:
Provide a modern clinic website where patients can:

- Learn about the clinic
- View doctors
- View services
- Read FAQs
- Contact the clinic
- Click "Book on WhatsApp"

---

## AI

Provider:
OpenAI API (GPT)

Purpose:

- Answer FAQs
- Understand patient requests
- Collect booking details
- Communicate naturally

The AI is responsible ONLY for conversation.

It does NOT store appointments.

It does NOT check schedules directly.

---

## WhatsApp

Technology:
WhatsApp Cloud API

Purpose:

Allow patients to communicate using WhatsApp.

---

## Automation

Technology:
n8n

Purpose:

Acts as the workflow engine.

Responsibilities:

- Receive booking request
- Read Google Sheets
- Check doctor availability
- Save appointment
- Create Google Calendar event
- Send confirmation message

---

## Google Sheets

Purpose:

Acts as the clinic's database.

Contains:

Clinic Information

Doctors

Services

Doctor Schedule

Appointments

The clinic staff can edit this information directly.

---

## Google Calendar

Purpose:

Acts as the doctor's appointment calendar.

Every confirmed appointment automatically creates a calendar event.

Benefits:

- Easy for doctors to manage daily schedule
- Can send reminders
- Familiar interface
- Works on phone and desktop

---

# System Flow

Patient

↓

Website

↓

Book on WhatsApp

↓

WhatsApp Cloud API

↓

AI Receptionist

↓

n8n Workflow

↓

Google Sheets

↓

Google Calendar

↓

Confirmation Message

---

# Responsibilities

Website

Responsible for displaying clinic information.

AI

Responsible for conversation only.

n8n

Responsible for automation.

Google Sheets

Responsible for storing clinic information and appointments.

Google Calendar

Responsible for managing appointment schedule.

---

# Future Upgrades

Possible future improvements:

- Admin Dashboard
- Supabase Database
- Online Payments
- SMS Notifications
- Patient Login
- Multi-clinic Support
- Analytics Dashboard
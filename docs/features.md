# ClinicFlow V1 - Features

Version: 1.0

---

# 1. Website

## Purpose

Provide a modern online presence for the clinic and guide patients to book appointments through WhatsApp.

---

## Pages

### Home

Contains:

- Hero Section
- Clinic Introduction
- Why Choose Us
- Services Preview
- Doctors Preview
- Testimonials
- CTA: Book Appointment on WhatsApp

---

### About Clinic

Contains:

- Clinic Story
- Mission
- Vision
- Clinic Images

---

### Services

Contains:

- List of Treatments
- Description
- Consultation Fee (Optional)

Example:

- Dental Cleaning
- Root Canal Treatment
- Teeth Whitening
- Braces
- Dental Implants

---

### Doctors

Each doctor should display:

- Photo
- Name
- Qualification
- Experience
- Specialization
- Consultation Fee

---

### FAQ

Examples:

- What are the clinic timings?
- Do I need an appointment?
- What payment methods are accepted?
- Where is the clinic located?
- Do you treat children?

---

### Contact

Contains:

- Phone Number
- Email
- Address
- Google Maps
- Clinic Timings
- WhatsApp Button

---

# 2. WhatsApp AI Receptionist

## Purpose

Allow patients to book appointments and answer common clinic questions.

---

## Capabilities

The AI should answer:

- Clinic timings
- Services offered
- Consultation fees
- Clinic location
- Doctor information

The AI should NOT provide:

- Medical diagnosis
- Treatment advice
- Emergency guidance

---

## Appointment Booking Flow

The AI should collect:

- Patient Name
- Phone Number
- Doctor (optional if only one doctor)
- Preferred Date
- Preferred Time

After collecting all details:

- Check doctor availability
- Confirm appointment
- Store appointment
- Send confirmation message

---

# 3. Google Sheets

The spreadsheet should contain the following sheets.

---

## Doctors

Columns

- Doctor Name
- Specialization
- Qualification
- Consultation Fee

---

## Schedule

Columns

- Doctor
- Day
- Start Time
- End Time
- Available

---

## Appointments

Columns

- Timestamp
- Patient Name
- Phone Number
- Doctor
- Date
- Time
- Status

---

# 4. Google Calendar

(Optional for V1)

Every confirmed appointment should automatically create a Google Calendar event.

---

# 5. n8n Automation

Workflow:

Patient submits booking

↓

If the patient specifies a doctor:
    → Check that doctor's availability.

Otherwise:
    → Automatically assign the first available doctor.

↓

If slot available

↓

Create appointment in Google Sheets

↓

(Optional) Create Google Calendar event

↓

Send WhatsApp confirmation

If slot unavailable

↓

Offer alternative available slots

---

# 6. Future Features (Not Part of V1)

- Admin Dashboard
- Online Payments
- Patient Login
- Appointment History
- Analytics
- SMS Notifications
- Multi-clinic Support
- AI Voice Calling
# ClinicFlow V1 - User Flow

Version: 1.0

---

# Patient Journey

## Step 1 - Discover the Clinic

The patient searches for the clinic on Google or receives the website link.

↓

Patient opens the website.

---

## Step 2 - Explore the Website

The patient can browse:

- Home
- About
- Services
- Doctors
- FAQ
- Contact

If the patient wants to book an appointment,

↓

Clicks

"Book Appointment on WhatsApp"

---

## Step 3 - WhatsApp Opens

Patient is redirected to the clinic's WhatsApp.

The AI Receptionist greets the patient.

Example:

Hello 👋

Welcome to Smile Dental Clinic.

How may I help you today?

---

## Step 4 - Understand Patient Intent

The AI identifies whether the patient wants to:

- Book an appointment
- Ask about clinic timings
- Ask about doctors
- Ask about fees
- Ask about services
- Ask for clinic location

If the patient only asks a question,

↓

Answer it.

↓

End conversation.

If the patient wants to book,

↓

Continue booking flow.

---

## Step 5 - Collect Patient Details

The AI asks for:

- Patient Name
- Phone Number
- Preferred Date
- Preferred Time

If the patient requests a specific doctor,

↓

Use that doctor.

Otherwise,

↓

Assign the first available doctor.

---

## Step 6 - Check Availability

The AI requests availability.

↓

n8n checks Google Sheets.

If available,

↓

Continue.

If unavailable,

↓

Offer alternative available slots.

---

## Step 7 - Confirm Booking

AI summarizes the booking.

Example:

Doctor:
Dr. Sharma

Date:
22 July

Time:
11:00 AM

Reply YES to confirm.

---

## Step 8 - Save Appointment

After confirmation,

n8n

↓

Creates a new row in Google Sheets.

↓

(Optional)

Creates Google Calendar event.

---

## Step 9 - Confirmation Message

AI sends:

"Your appointment has been confirmed.

Doctor:
Dr. Sharma

Date:
22 July

Time:
11:00 AM

Thank you for choosing Smile Dental Clinic."

---

## Step 10 - End Conversation

Conversation ends.

Patient can message again anytime.
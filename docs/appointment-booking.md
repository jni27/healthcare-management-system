# Appointment Booking

## User Story

**As a patient, I want to book an appointment with a doctor so that I can receive medical consultation at an available time slot.**

---

## Functional Requirements

### Functional Requirements

1. Only registered patients can book an appointment.
2. Patients can choose a doctor.
3. Patients can select an available date and time.
4. The system should verify that the doctor is available for the selected slot.
5. The appointment should be created with the status **BOOKED**.
6. Patients should be able to view their appointments.
7. Patients should be able to cancel an appointment before the scheduled time.
8. Doctors should be able to view their appointment schedule.

### Non-Functional Requirements

1. Appointment booking should be completed within a few seconds.
2. Two patients should not be able to book the same time slot simultaneously.
3. Only authenticated users can access the booking API.
4. The system should maintain data consistency.

---

## Request API

**HTTP Method**

```http
POST /api/v1/appointments
```

**Purpose**

Creates a new appointment.

---

## Request JSON

```json
{
  "patientId": 101,
  "doctorId": 25,
  "appointmentDate": "2026-07-25",
  "appointmentTime": "10:30",
  "reasonForVisit": "High Fever"
}
```

---

## Response JSON

```json
{
  "appointmentId": 501,
  "status": "BOOKED",
  "message": "Appointment booked successfully."
}
```

---

## Validation Rules

1. Patient must exist.
2. Doctor must exist.
3. Doctor must be active.
4. Patient must be active.
5. Appointment date cannot be in the past.
6. Appointment time must be within the doctor's working hours.
7. Doctor should not already have another appointment for the selected slot.
8. Patient should not have another active appointment for the same time.
9. Reason for visit should not be empty.

---

## Backend Flow

```
Client
   │
   ▼
AppointmentController
   │
   ▼
AppointmentService
   │
   ├── Validate Patient
   │
   ├── Validate Doctor
   │
   ├── Check Doctor Availability
   │
   ├── Create Appointment
   │
   ├── Save Appointment
   │
   ▼
Return Success Response
```

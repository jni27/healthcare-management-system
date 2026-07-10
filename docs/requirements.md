# Healthcare Management System

## 1. Project Overview

The Healthcare Management System is a backend application designed to manage
hospital operations digitally.

The system allows patients to register, book appointments with doctors,
view prescriptions, and access medical records.

Doctors can manage appointments, prescribe medicines, and maintain patient records.

Administrators manage users, doctors, hospital data, and monitor the overall system.

The goal is to replace manual record keeping with a secure, scalable, and
maintainable backend system.

---

# 2. User Roles

There are three primary users in the system.

## Admin

Responsibilities

- Create doctor accounts
- Update doctor details
- Delete doctor accounts
- Manage patient accounts
- View all appointments
- View hospital reports
- Manage departments
- Block or unblock users

Permissions

- Full system access

---

## Doctor

Responsibilities

- Login securely
- View today's appointments
- Access patient medical history
- Write prescriptions
- Upload medical records
- Update appointment status
- Cancel appointments if required

Permissions

- Can access only assigned patients
- Cannot modify admin information
- Cannot delete patients

---

## Patient

Responsibilities

- Register
- Login
- Update profile
- Search doctors
- Book appointment
- Cancel appointment
- View appointment history
- Download prescriptions
- View medical records

Permissions

- Can access only their own data
- Cannot view other patients' records

---

# 3. Functional Requirements

## Authentication

- User Registration
- User Login
- JWT Authentication
- Refresh Token
- Logout
- Password Encryption
- Role Based Authorization

---

## Doctor Management

- Add Doctor
- Update Doctor
- Delete Doctor
- Search Doctor
- Filter by Department
- View Doctor Profile

---

## Patient Management

- Register Patient
- Update Patient Profile
- View Patient Details
- Soft Delete Patient

---

## Appointment Management

- Book Appointment
- Cancel Appointment
- Reschedule Appointment
- Approve Appointment
- Reject Appointment
- View Appointment History

---

## Prescription Management

Doctor can

- Create Prescription
- Update Prescription
- Download Prescription PDF

Patient can

- View Prescription
- Download Prescription

---

## Medical Record Management

Doctor can

- Upload Reports
- Upload Lab Results
- Add Diagnosis

Patient can

- View Medical Records
- Download Reports

---

# 4. Non Functional Requirements

## Security

- JWT Authentication
- Password Encryption using BCrypt
- Role Based Access
- HTTPS
- Input Validation

---

## Performance

- API response should be less than 2 seconds
- Pagination for large datasets
- Database Indexing

---

## Scalability

The system should support microservices architecture.

---

## Reliability

- Global Exception Handling
- Logging
- Retry Mechanism
- Database Backup

---

# 5. Main Entities

## User

- id
- firstName
- lastName
- email
- password
- phoneNumber
- role
- status
- createdAt
- updatedAt

---

## Doctor

- doctorId
- specialization
- experience
- qualification
- department
- consultationFee

---

## Patient

- patientId
- age
- gender
- bloodGroup
- allergies
- address
- emergencyContact

---

## Appointment

- appointmentId
- appointmentDate
- appointmentTime
- status
- doctorId
- patientId

---

## Prescription

- prescriptionId
- diagnosis
- medicines
- dosage
- notes

---

## MedicalRecord

- recordId
- patientId
- doctorId
- reportName
- reportType
- uploadedDate

---

# 6. Business Rules

1. Patient email must be unique.

2. Doctor email must be unique.

3. Appointment cannot be booked in the past.

4. One doctor cannot have two appointments at the same time.

5. Patients can cancel appointments only before consultation.

6. Only doctors can create prescriptions.

7. Only authenticated users can access APIs.

8. Medical records are visible only to the patient and authorized doctors.

9. Admin has access to all data.

10. Password must always be encrypted.

---

# 7. Future Enhancements

- Online Payments
- Video Consultation
- SMS Notifications
- Email Notifications
- AI Health Assistant
- Medicine Inventory
- Pharmacy Module
- Insurance Management

---

# 8. Questions for Client

1. Can a patient consult multiple doctors?

2. Can doctors belong to multiple departments?

3. How long should medical records be stored?

4. Can doctors edit prescriptions?

5. Can patients reschedule appointments?

6. Is online payment required?

7. Should appointment reminders be sent?

8. Is file upload size limited?

9. Can doctors work in multiple hospitals?

10. Should patients be able to download all reports?

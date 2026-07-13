# Entity Relationships

## 1. User ↔ Doctor

Relationship:
One-to-One (1:1)

Reason:
Every doctor is a user, but not every user is a doctor.

------------------------------------

## 2. User ↔ Patient

Relationship:
One-to-One (1:1)

Reason:
Every patient is a user, but not every user is a patient.

------------------------------------

## 3. Department ↔ Doctor

Relationship:
One-to-Many (1:N)

Reason:
One department has many doctors.
A doctor belongs to one department.

------------------------------------

## 4. Doctor ↔ Appointment

Relationship:
One-to-Many (1:N)

Reason:
One doctor can have many appointments.
Each appointment belongs to one doctor.

------------------------------------

## 5. Patient ↔ Appointment

Relationship:
One-to-Many (1:N)

Reason:
One patient can book many appointments.
Each appointment belongs to one patient.

------------------------------------

## 6. Appointment ↔ Prescription

Relationship:
One-to-One (1:1)

Reason:
One appointment generates one prescription.

------------------------------------

## 7. Patient ↔ MedicalRecord

Relationship:
One-to-Many (1:N)

Reason:
One patient can have many medical records.

------------------------------------

## 8. Doctor ↔ MedicalRecord

Relationship:
One-to-Many (1:N)

Reason:
One doctor can upload many medical records.
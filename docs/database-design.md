# Database Design

## Entities
 - User
 - Doctor
 - Patient
 - Appointment
 - Prescription
 - Medical Records
 - Department

 ### User
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

  ### Doctor
- doctorId
- specialization
- qualification
- experience
- consultationFee
- departmentId

### Patient
- patientId
- dateOfBirth
- gender
- bloodGroup 
- allergies
- emergencyContact
- address

### Appointment
- appointmentId
- appointmentDate
- appointmentTime
- status
- doctorId
- patientId
- reasonForVisit

### Prescription
- prescriptionId
- appointmentId
- diagnosis
- medicines
- notes

### MedicalRecord
- recordId
- patientId
- doctorId
- reportName
- reportType
- filePath
- uploadedAt

### Department
- departmentId
- departmentName
- description



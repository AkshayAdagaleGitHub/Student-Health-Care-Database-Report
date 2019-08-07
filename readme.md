````
Student Health Care System


1. Summary
We decide on designing a database system for Student Clinic in a University offering primary health care services to current students 
and faculties. We have chosen the University of North Carolina, Charlotte as our model University. For this project, we have planned to modulate a part of
scope of already existing health care resources at UNC Charlotte.

2. Scope
As per our system design, our health care project features services including primary Medical Care, HIV Testing,
Sports Medicine, Nurse Clinic, Digital Laboratory, Immunizations, Travel Medicine, Allergy Injections, Psychiatric Care
and Physical Therapy. The entire unit comprises of departments of health care featuring doctors and services provided,
management and maintenance featuring the daily check and resource availability factors. To be able to store and maintain data in
normalized form, we have maintained tables for users , which is then being referenced by patient and doctor classes. 
To enable check on patient’s insurance availability, we have created an insurance class. This class is correlated
with patient_insurance_relation class that references the patient’s ID from patient table to retrieve information 
regarding the type and validity of insurance. We are maintaining a table for services provided called the services table, 
a basic chart that will contain each service with dedicated doctor’s ID. Every patient will be able to book an appointment, and on
doing so, will be listed in appointments table with patient and appointment details. To maintain record of patient’s visits, 
we have a class visit_information that will be updated each time the patient visits clinic with date, time, doctor and 
reason of visit details. As there are some standard tests to be carried out for particular symptoms, and for each patient 
the result will be varied, thus, we have maintained three distinct yet co-related tables of visit_clinic_care_information comprising of
symptoms, prescriptions and suggested diagnosis, visit_information_tests to list down particular tests as per symptoms stated 
in clinic care table and tests table that will maintain records for all tests of each patient. Lastly, we have a billing table that adds up service charges and doctor fees thereby reflecting the final bill in bills table. The table will have a status field indicating the bill being paid or unpaid, and each time the value will be set as and when user makes the payment.The tables created and structure of each with dedicated attributes is shown as follows:

Following tables created:
 ● usertype
    ○ `typeID`
    ○ `TypeName`
● paymenttype
    ○ `PaymentType_ID`
    ○ `Payment_Method`
● address
    ○ `AddressID`
    ○ `Address`
    ○ `zipcode`
    ○ `city`
    ○ `State`
● `insurance
    ○ `Insurance_ID`
    ○ `Start_date`
    ○ `End_date`
    ○ `Insurance_Name`
● `user`
    ○ `user_Id`
    ○ `user_type`
    ○ `address_ID`
● `doctor`
    ○ `ID`
    ○ `first_name`
    ○ `last_name`
    ○ `Speciality`
    ○ `Email`
● `patient`
    ○ `ID`
    ○ `first_name`
    ○ `last_name`
    ○ `InsuranceId`
    ○ `Email`
● `appointment`
    ○ `ID`
    ○ `patient_id`
    ○ `doctor_id`
    ○ `date`
● `prescription`
    ○ `Prescription_ID`
    ○ `Patient Name`
    ○ `Doctor Name`
    ○ `Prescription_Date`
    ○ `Medicine`
● `prescription_doctor_patient`
    ○ `Prescription_ID`
    ○ `Doctor_ID`
    ○ `Patient_id`
● `tests`
    ○ `ID`
    ○ `patient_id`
    ○ `doctor_id`
    ○ `test_type`
    ○ `result`
● `bill`
    ○ `Bill ID`
    ○ `Patient ID`
    ○ `Doctor ID`
    ○ `Test ID`
    ○ `Insurance Num`
    ○ `Bill Date`
    ○ `Total Cost`

● `payment`
    ○ `Payment ID`
    ○ `Bill ID`
    ○ `Payment Type`
    ○ `Payment date`
    ○ `Total Cost`
● `visit_information`
    ○ `ID`
    ○ `Patient_ID`
    ○ `Date`
    ○ `doctor_ID`
● `visit_clinic_care_information`
    ○ `ID`
    ○ `visit_information_id`
    ○ `Symptoms`
    ○ `Prescription`
    ○ `diagnosis`
● visit_information_test_relation
    ○ visit_information_id
    ○ test_id
````

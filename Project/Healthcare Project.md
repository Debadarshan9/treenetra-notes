# Date: 13-October-2026

### **What is healthcare domain ?**

&rarr; Healthcare domain refers to the industry that provides the medical services, patient care, diagnosis, treatment, hospital management, health insurance and medical data management.

&rarr; In the IT industry the healthcare domain involves developing, maintaining and testing software application used by hospitals, doctors, patients, labs, pharmacies, insurance companies and medical equipment provider.

## **Major modules in the healthcare domain**

**HMS - Hospital Management System**

Manages patient registration, appointments, admissions, discharge, billing and hospital operations.

**EHR/EMR - Electrical Health Record**

Stores patient medical history, diagnosis, prescriptions, allergies, treatment plan and clinical observations.

**PACKS / Radiology Info System**

Here we can manage x-rays, CT scan, MRI images, radiology orders, reports and image workflow.

**LIS - Laboratory information system**

Manages lab test order, sample collection, processing test result and reports.

**Health Insurance and Claims**

Manages insurance eligibility, prior authorization, claim submissions, payment processing and claim denials.

## **Who uses the healthcare software ?**

**Hospitals and clinics**

They manage patients, doctors, bed and operation.

**Doctors**

Write prescriptions and view patient history and order test.

**Nurses**

Record vitals, manage medication schedules and word duets.

**Patients**

Book appointments, view reports, pay bills online.

**Insurance Companies (Payers)**

Received and approved the claims.

**Labs**

Collect samples and upload test reports.

**Pharmacies**

Dispense medicines and manage docs.

**Diagnosis center**

Perform MRI, CT scan and other scans.

**Govt. health care system**

Track public health and vaccine drivers.

## **Common Healthcare application**

**EHR**

&rarr; An EHR is a digital collection of patient's medical information designed to support are over time and facilitate authorize share among healthcare providers

&rarr; Give doctor's comprehension views of a patient's health, history and treatment.

**What information is stored ?**

Patient's demography

Medical history and previous diagnosis

Allergies and medications

Lab result

Radiology reports

Surgery and hospitalization history

Doctor

**EMR (Electrical Medical Record)**

EMR is a digital version of patient's medical chart maintained by

Help doctor and hospital staff manage

**HMS (Hospital Management System)**

It manages hospital administrative operations and clinical activities

Patient registration

Doctor's schedule and availability

Admission Discharge and Transfer (ADT)

**LIS - Laboratory Information System**

It is a software that manages the medical lab

**RIS - Radiology Info System**

It manages the radiology department operation including image orders, scheduling, examination tracking, report and radiology workflow

**PACKS (Picture Achieving Communication System)**

It stores, retrieves, distributes medical images

**Pharmacies Management System**

A pharmacy management system manages medications, prescriptions, inventory, dispenses, and pharmacies billings.

**Insurance Claim System**

It processes claim request submitted by hospital, provider or patients to insurance companies

**Patient Portal**

A patient portal is a secure website or mobile application allowing patient to access their health information and interact with healthcare providers.

# Date: 14-Oct-2026

## **Important Healthcare terms and vocabulary**

**Patient**

The person who is seek and receives treatment.

**Provider**

The doctor, hospital, clinic or anyone who gives treatment.

**Payer**

The insurance company or government agency that pays the hospital bills.

**Claim**

A bill sent by the hospital to the insurance company for the payment.

**Encounter**

One visit of a patient to a doctor or hospital.

**Diagnosis**

The disease that the doctor confirm after checking the patient.

**Prescription**

The list of medicines and tests that the doctor writes for the patient.

**Lab Order**

A request from the doctor to do a blood test,urine test and etc.

**Radiology order**

A request from the doctor to do a CT scan, MRI, X-ray and etc.

**Medical History (EHR/EMR)**

All past illnesses, surgeries, allergies of the patient.

**PHI (Protected Health Information)**

Any data that identifies the patient.

**ePHI (Electronic Protected Health Information)**

Any data that identifies the patient and stored in electronic format (email, database, APIs).

**HIPAA (Health Insurance Portability and Accountability Act)**

&rarr; It is a law in the USA that protects patient's data in every healthcare application touches USA patient data.

&rarr; If HIPAA is violated, the company or hospital or clinic can be fined a millions of dollar and the responsible employee can even go to the jail.

&rarr; So as a tester we are literally protecting the company every time you log a security defect.

| PHI                                                           | ePHI                                                                                           |
| ------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| Protected Health Information                                  | Electronic Protected Health Information                                                        |
| Any piece of info tha can be use to verify a patient identity | Any piece of info that can be use to verify a patient identity and stored in electronic format |
| Patient full name, dob, phone number                          | Patient's all details                                                                          |

**PHI minimal rules & regulation**

&rarr; Unauthorized user must not see any patient data.

&rarr; Role based access must be correctly (a lab technician should not see billing, a receptionist should not see technical data).

&rarr; All sensitive data must be encrypted in transit and at rest database encryption.

&rarr; Application logs must be contain PHI or ePHI (No patient name, no dob, no MRI).

&rarr; Session must timeout automatically after a few minutes of inactivity.

&rarr; Every action (view, create, update, delete) must be saved in audit file.

&rarr; Download reports must be open only with proper authorization, ideally password protected.

&rarr; API must not return extra patient field.

# Date: 21-Oct-2026

### **Healthcare standards**

#### **HL7 (Health Level 7)**

&rarr; HL7 is the oldest and most widely used health care messaging standard, think of it as a special envelope format that all hospital system agree to use.

&rarr; Basically HL7 exchanging patient data between EHR to hospital, clinic and LIS.

&rarr; When the EHrR sent a lab order to LIS, It put the data in HL7 message and send it across.

&rarr; The message looks strength with pipeline (|) and carets (^).

Ex: MSH|^-\&|EHR-SYS|HOSPITAL-A|LAB-SYS|LAB-CENTER|20260527|ORM^001|123|P|2.5

PID||P1001||DASH^RABI||19800101|M

### **FHIR - (First Healthcare Interoperability Resources)**

&rarr; FHIR is the modern replacement of HL7, it use restAPI and json exactly like API in web project.

&rarr; In FHIR everything is called resource(patient, observation, encounter, medication request).

### **Dicom - (Digital Imaging and Communication in Medicine)**

It is a standard of medical image, every x-ray, MRI, ct-scan kept as `.dcm` file (handled in python - pydicom).

&rarr; It is a file not just an image, it also store patient metadata, hospital info, machine info and the date the scan was taken.

### **EDI - (Electronic Data Interchange)**

&rarr; It is the format (`EDI 835`) used to insurance claim

&rarr; When a hospital send a claim to insurance company, it doesn't send a right json.

&rarr; It send `EDIx12` file

**`ICD`** - Standardize code for Diagnosis

**`CPT`** - Standardize code for Procedure

**`NPI`** - Standardize code for doctors

| Code Type | Meaning                   | Example                                     |
| --------- | ------------------------- | ------------------------------------------- |
| ICD-10    | Disease/Diagnosis         | I10 - High blood pressure                   |
| CPT       | Service                   | 99213 - Hospital Visit , 99453 - Admit ward |
| NPI       | Unique Provider ID (docs) | 1237943 - Dr. Das                           |

### **End to end Flow using standards**

Doctor creates lab order in EHR

&darr;

HL7 / FHIR message sent

&darr;

Lab System (LIS) receives the order

&darr;

Sample Collected, test done

&darr;

Lab upload result

&darr;

Result message sent to backend

&darr;

EHR updates the patient record

&darr;

Patient sees report in patient portal

&darr;

Hospital generates bill --> Create EDI 835 --> Sends to insurance

&darr;

Insurance Pays &rarr; Sends back EDI 835 &rarr; Hospital updates billing

# Date: 22-Oct-2026

## **End to end HealthCare flow**

Medi Assist AI (Intelligent HealthCare Patient care and Claim Management Platform)

### **Business Goal**

&rarr; Medi Assist AI is a complete hospital com AI platform.

&rarr; It covers the entire patient journey from moment they enter to the hospital to the moment the insurance claim is fully paid.

&rarr; On top of that is has an AI assistant and agentic AI workflow for smart automation.

### **Platform Manages:-**

&rarr; Patient registration

&rarr; Appointment booking

&rarr; Doctor consultation

&rarr; Lab order and radiology order

&rarr; Prescriptions and pharmacy dispensing

&rarr; Billing and invoice generation

&rarr; Insurance claim submission

&rarr; Patient report and history

&rarr; AI based patient support (chatbot)

&rarr; Agentic AI based workflow and automation (Claim agent, appointment agent, report agent)

## **Project Stakeholder**

`Product Owner` &rarr; Decide business priority and features

`Business Analyst` &rarr; Write requirements and user stories

`Solution Architect` &rarr; Design the technical architecture

`Dev Lead and developers` &rarr; Build the application

`QA Lead and QA engineers` &rarr; Test the application

`DevOps Engineer` &rarr; Manages CI/CD pipeline and docker and aws

`Clinical SME (Subject Matter Expert)` &rarr; Subject matter expert for healthcare domain

`Compliance and Security Officer` &rarr; Ensure HIPAA compliance

`AI/ML Engineer` &rarr; Build RAG, agents and LLM workflow

### **High Level Architecture**

Patient Portal | Doctor Portal | Management | Admin Portal

&darr; API Gateway

Patient, appointment, billing, auth

&darr;

Healthcare workflow engineer

&darr;

EHR / EMR / LIS / RIS / Packs Insurance

&darr;

Database + Audit Logs + Reports

&darr;

AI Layer / Agentic AI Layer

&darr;

RAG agent, claim agent, appointment, compliance agent

## **Layer by Layer Explanation**

### **Layer 1 - Frontend (UI)**

Built is typical using React, angular and QA tests UI flows help of selenium and playwright.

### **Layer 2 - API Gateway**

&rarr; All UI request first land on the API gateway, It checks authentication, rate limits and routes to request to the correct microservices.

&rarr; As a QA we test gateway level concern, valid and invalid tokens, authentication and authorization help of REST API methods.

### **Layer 3 - Microservices**

As a QA we test separately each and every microservice independently.

### **Layer 4 - Workflow Engine**

Many healthcare flows have multiple steps (lab order, sample, result, approval, patient).

### **Layer 5 - Integration with external system**

&rarr; Medi assist talks to LIS, RIS, packs and insurance using HL7, FHIR and EDI.

&rarr; This is the hardest part of test because failure can be happen on either site the integration test live here.

### **Layer 6 - Database and audit layer**

&rarr; All data lives in database (SQL server, MongoDB)

&rarr; A separate audit log database records every user action, required for HIPAA.

### **Layer 7 - AI / Agentic AI Layer**

&rarr; It is an orchestration layer for the llm, rag and different different agents call the different hospital application and modules.

# Date: 27-Oct-2026

## **Hospital,Insurance, Payer, Billing and Payment transaction**

#### **1. TPA (Third Party Administrator)**

It process claims and coordinates cashless claims.

#### **2. Policy**

Insurance contract describing benefits and conditions.

#### **3. Claim**

Request for insurance payments

#### **4. Pre-authorization**

Approval process before certain cashless statement

#### **5. Deductible**

Amount patient must pay before specified insurance benefits.

#### **6. Copay**

Patients cared some items covered expense.

#### **7. EOB (Explanation of Benefits)**

It shows claim processing and payment responsibility

#### **8. Settlement**

Payment made against an approved claim

# Date: 11-Nov-2026

## **1. MediAssist AI - Intelligent Healthcare Patient Care Management**

Manage a patient's complete hospital journey

Registration, Appointment, Consultation, Treatment, Discharge, Follow-up

### **AI Agents :-**

Patient Registration

Appointment Registration

Clinical Summary Agent

Follow-up Agent

### **Agent Workflow**

Patient Request &rarr; Patient Registration Agent &rarr; Appointment Agent &rarr; EHR Agent &rarr; Clinical Summary Agent &rarr; Doctor Review &rarr; Follow-up Agent

### **QA Validation**

UI Automation with Playwright using python and in pytest framework

CRUD APIs:- REST API validation (postman, py req,playwright API-CONTEXT)

FHIR validation:- API/JSON API validation

SQL validation with help of SQL query

RBAC :- Authentication (JWT, Oauth2.0)

Agentic AI

RAG Validation (Precision, Recall, Context Precision, Context Recall, P@K, R@K, MRR, Hit Rate)

## **2. RadVision AI - Intelligent Radiology and Imaging Platform**

Manage imaging order

CT scan, MRI, X-ray, examination workflow

Image retrieval (DICOM)

Radiology Report

Doctor Notification

### **AI Agent :-**

Image order agent

DICOM retrieval agent

Radiology report drafting agent

Doc Notification agent

### **Agent Workflow**

Image Order &rarr; RIs &rarr; PACKS &rarr; DICOM retrieval agent &rarr; Imaging model / report draft &rarr; Radiology Approval &rarr; EHR update

### **QA Validation**

UI Automation with Playwright using python and in pytest framework

CRUD APIs:- REST API validation (postman, py req,playwright API-CONTEXT)

DICOM metadata - OCR

APIs CRUD to store data in EHR

RAG hallucination

Tool accuracy testing

LLM validation

## **3. LabCare AI - Intelligent Laboratory Diagnostic System**

Manage lab order (blood, store, urine, etc.)

Specimen collection, after physical collection then it will update on application

Barcode tracking

Test result

Report generation

clinical alerts

### **AI Agents:-**

Lab order agent

Sample tracking agent

Result interpretation support agent (3 metrics)

Critical alert agent

### **Agentic Workflow**

Doctor Lab Order &rarr; LIS &rarr; Sample tracking &rarr; Analyzer result agent &rarr; Result validation &rarr; AI agent explanation &rarr; Clinical review

## **QA Validation**

UI Automation with Playwright using python and in pytest framework

CRUD APIs:- REST API validation (postman, py req,playwright API-CONTEXT)

Sample mapping:- APIs

Patient identity and validate LIS result and store in EHR

FHIR Observation validation:- APIs validation
status
request body
response json schema
header
authentication & authorization

RAG hallucination

tool accuracy testing

LLM validation

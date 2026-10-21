ITC327W — UPDATED SOFTWARE REQUIREMENTS SPECIFICATION (SRS)
Student Accommodation Management System
Module: ITC327W — Work-Integrated Learning
Stakeholder: Makhele PC — Student Accommodation Owner
Organisation: Makhele Stud Accommodation
Date: 25 October 2026
Version: 3.0 (Combined Phases 1, 2 & 3)
GitHub Repository: https://github.com/222093279/BizUp_Group_G
Group G Members: Matlhoane Lebohang (222059872), Mohlomi Ramadulwane D (222082927),
Kayane Thabo William (219015324), Moloi Letlotlo (222093279), Kalo KI (220046482), Tshabalala MV (222044346)

TABLE OF CONTENTS
1. Introduction
2. Overall Description
3. Business Rules
4. Functional Requirements
5. Use Cases
6. Data Requirements
7. External Requirements
8. Reporting Requirements
9. Feasibility Study
10. Project Risk Register
11. Requirements Change Log
12. Refined Project Scope
13. Non-Functional Requirements
14. Integration Requirements
15. Supplemental Information
16. Stakeholder Evidence
17. Implementation and Final Prototype (PHASE 3)

=====================================================================
1. INTRODUCTION
=====================================================================
1.1 Purpose
This Software Requirements Specification (SRS) describes the complete requirements for the Student
Accommodation Management System. The document combines the work completed in Phases 1 and 2 and the
implementation completed in Phase 3, and reflects the current project baseline following feasibility analysis,
risk assessment, stakeholder confirmation and final prototype development.
The system will assist an accommodation owner in managing two off-campus, unaccredited student
accommodation rooms by replacing handwritten records and verbal communication with a centralised digital
solution comprising a Flutter mobile application, an ASP.NET web application and a shared Supabase backend.

1.2 Project Background
The stakeholder manages three off-campus student rooms under 11-month rental contracts. Current management
relies on handwritten records, verbal terms and conditions, and manual payment tracking. This creates
organisational difficulties, misunderstandings and challenges monitoring late payments while students remain
under active contracts.

1.3 Problem Statement
The accommodation owner currently relies on handwritten records and verbal communication to manage three
off-campus student accommodation rooms and their 11-month rental contracts. This creates difficulties in
organising accommodation information, clearly communicating rental terms and conditions, and monitoring
rental payments. The problem affects both the accommodation owner and student tenants because unclear or
verbally communicated information can lead to misunderstandings and conflicts. Late payments also create
difficulties for the owner when managing students who still have active contracts. An improved digital solution
is required to provide organised records and improve the management of students, rooms, rental agreements,
terms and conditions and rental payments.

1.4 Project Aim
To develop a Student Accommodation Management System that provides a centralised digital method for
managing student accommodation information, rental agreements, terms and conditions and rental payments
through a Flutter mobile application, an ASP.NET web application and a shared Supabase backend.

1.5 Objectives
1. Digitise the stakeholder's handwritten accommodation records.
2. Provide organised student information management.
3. Manage information relating to the two accommodation rooms.
4. Record and manage 11-month rental agreements.
5. Digitally record rental terms and conditions.
6. Record and monitor rental payments.
7. Identify outstanding or late payments.
8. Reduce misunderstandings caused by relying on verbal communication.
9. Provide students with access to relevant accommodation information.
10. Provide the owner with a web-based platform for managing accommodation information.

1.6 Scope
1.6.1 In Scope
- Student information management.
- Three-room accommodation management.
- 11-month rental agreement management.
- Digital recording of rental terms and conditions.
- Rental payment recording.
- Monitoring of outstanding payments.
- Student access to relevant accommodation information (Flutter mobile app).
- Owner management platform (ASP.NET web app).
- Supabase shared data storage and backend services.
- Basic reporting (payment, occupancy, agreements).

1.6.2 Out of Scope
- Direct online banking or payment processing.
- Legal eviction procedures or contract termination automation.
- Legal advice.
- Government accreditation of the accommodation.
- Management of university-owned accommodation.
- Management of other landlords' properties.
- Full accounting or financial-management software.
- Advanced analytics or predictive reporting.

1.7 Definitions and Abbreviations
Term / Abbreviation | Meaning
SRS | Software Requirements Specification
Stakeholder | The accommodation owner who provides the problem context and requirements
Student Tenant | A student renting one of the accommodation rooms
Rental Agreement | An agreement between the accommodation owner and student for the rental period
11-Month Contract | The rental agreement period used by the stakeholder
Flutter | Framework used to develop the mobile application
ASP.NET | Platform used to develop the web application
Supabase | Backend and database platform for shared system information
Mobile Application | Application intended primarily for student users
Web Application | Application intended primarily for the accommodation owner
Unaccredited Accommodation | The stakeholder's off-campus accommodation that is not accredited
POPIA | Protection of Personal Information Act (South Africa)
BR | Business Rule
FR | Functional Requirement
NFR | Non-Functional Requirement
RR | Reporting Requirement
UC | Use Case
ERD | Entity Relationship Diagram

=====================================================================
2. OVERALL DESCRIPTION
=====================================================================
2.1 Product Perspective
The system consists of three integrated components:
- Flutter Mobile Application — used by student tenants to access accommodation and rental information.
- ASP.NET Web Application — used by the accommodation owner to manage students, rooms, rental
  agreements, terms and conditions and payments.
- Supabase Backend — shared database and backend service storing and exchanging information between
  both applications.
Product Flow: Student → Flutter Mobile App → Supabase ← ASP.NET Web App ← Accommodation Owner

2.2 Stakeholders and User Groups
2.2.1 Accommodation Owner (Primary Stakeholder)
Manages three off-campus student rooms. Responsible for student tenants, rental agreements, terms and
payments. Requires organised digital records and payment monitoring.
2.2.2 Student Tenants
Users who occupy the accommodation rooms. Use the mobile application to access relevant accommodation,
rental agreement and terms information.
2.2.3 Project Group
Responsible for analysis, requirements, design, development and evaluation of the prototype.

2.3 Current Process
The owner rents two rooms under 11-month contracts. Information is recorded by hand; terms are communicated
verbally. Payments are monitored manually. Late payments create management difficulties while contracts
remain active.
Main Problems:
1. Handwritten records are disorganised and difficult to retrieve.
2. Information is not centrally organised.
3. Rental terms and conditions are communicated verbally.
4. Verbal communication leads to misunderstandings and conflicts.
5. Late payments are difficult to monitor.
6. Active contracts complicate payment follow-up.

2.4 Proposed System Overview
The system provides a centralised digital platform. The owner uses the ASP.NET web application for management.
Students use the Flutter mobile application for information access. Supabase provides shared data storage and
backend services.

2.5 Product Functions
2.5.1 Flutter Mobile Application
- View accommodation information.
- View rental agreement details.
- View applicable terms and conditions.
- Access personal accommodation-related information.
2.5.2 ASP.NET Web Application
- Manage student information.
- Manage room information.
- Record and manage rental agreements.
- Record rental terms and conditions.
- Record and monitor rental payments.
- View outstanding or late payments.
- Generate basic reports.
2.5.3 Supabase Backend
- Store student, room, agreement, terms and payment records.
- Provide shared data access to both applications.
- Enforce authentication and authorisation.
- Handle real-time data synchronisation.

2.6 Constraints
1. Academic semester deadline (final submission 25 October 2026).
2. System initially designed for two accommodation rooms only.
3. Development team consists of six students with limited time.
4. Mobile application must use Flutter.
5. Web application must use ASP.NET.
6. Supabase must be used as the shared backend.
7. No budget for commercial software licences or cloud infrastructure beyond free tiers.
8. Prototype scope must remain focused on identified accommodation-management problems.

2.7 Assumptions
1. The stakeholder will provide necessary accommodation information for development and testing.
2. Students will have access to Android smartphones.
3. The owner will have access to a computer with a modern web browser.
4. Users will have reliable internet connectivity.
5. The stakeholder's three rooms remain the initial scope.
6. The stakeholder will provide feedback during requirements and evaluation stages.
7. Test data will be used during development to protect real student privacy.

=====================================================================
3. BUSINESS RULES
=====================================================================
ID | Business Rule
BR1 | The stakeholder manages two accommodation rooms.
BR2 | Accommodation is provided to student tenants.
BR3 | Each student must be associated with the relevant room.
BR4 | Rental arrangements use 11-month contracts.
BR5 | Rental agreements must be associated with students and rooms.
BR6 | Rental agreement information must be recorded digitally.
BR7 | Rental agreement information must be accessible to the owner.
BR8 | Rental terms and conditions form part of the accommodation arrangement.
BR9 | Important terms and conditions should be digitally recorded.
BR10 | Students should be able to access applicable terms and conditions.
BR11 | Payments must be associated with the relevant student and agreement.
BR12 | Payments must be recorded.
BR13 | Late or outstanding payments must be identifiable.
BR14 | The owner must be able to view outstanding payments.
BR15 | Late payment does not automatically terminate an active contract.
BR16 | The owner requires management access.
BR17 | Students should only access their own relevant information.
BR18 | Private information must be protected and not exposed publicly.

=====================================================================
4. FUNCTIONAL REQUIREMENTS
=====================================================================
4.1 Student Management
ID | Functional Requirement | Priority
FR1 | The owner must be able to add a tenant to the system. | Must Have
FR2 | The owner must be able to view tenant information. | Must Have
FR3 | The owner must be able to update student tenant information. | Must Have
FR4 | The owner must be able to associate a student with an accommodation room. | Must Have

4.2 Room Management
ID | Functional Requirement | Priority
FR5 | The owner must be able to view the two accommodation rooms. | Must Have
FR6 | The owner must be able to view the student associated with a room. | Must Have
FR7 | The system must indicate whether a room is occupied or available. | Should Have

4.3 Rental Agreement Management
ID | Functional Requirement | Priority
FR8 | The owner must be able to create a rental agreement for a student. | Must Have
FR9 | The owner must be able to record the start date of a rental agreement. | Must Have
FR10 | The owner must be able to record the end date of a rental agreement. | Must Have
FR11 | The owner must be able to view a student's rental agreement information. | Must Have
FR12 | The system must associate the rental agreement with the relevant student and room. | Must Have

4.4 Terms and Conditions Management
ID | Functional Requirement | Priority
FR13 | The owner must be able to record terms and conditions. | Must Have
FR14 | The owner must be able to update the recorded terms and conditions. | Must Have
FR15 | Students must be able to view the terms and conditions applicable to their rental agreement. | Should Have
FR16 | The system must associate the relevant terms and conditions with the student's rental agreement. | Must Have

4.5 Payment Management
ID | Functional Requirement | Priority
FR17 | The owner must be able to record a rental payment. | Must Have
FR18 | The owner must be able to view payment records for a student. | Must Have
FR19 | The system must associate a payment with the relevant student and rental agreement. | Must Have
FR20 | The system must allow the owner to identify outstanding payments. | Must Have
FR21 | The owner must be able to update payment information when a payment is received. | Must Have

4.6 Outstanding Payment Management
ID | Functional Requirement | Priority
FR22 | The system must identify payments that are outstanding. | Must Have
FR23 | The owner must be able to view a list of students with outstanding payments. | Must Have
FR24 | The owner must be able to view the relevant rental information when checking an outstanding payment. | Should Have

4.7 Student Mobile Functions
ID | Functional Requirement | Priority
FR25 | Students must be able to access the mobile application. | Must Have
FR26 | Students must be able to view their accommodation information. | Should Have
FR27 | Students must be able to view their rental agreement information. | Should Have
FR28 | Students must be able to view applicable terms and conditions. | Should Have

4.8 Owner Web Functions
ID | Functional Requirement | Priority
FR29 | The owner must be able to access the accommodation management dashboard. | Must Have
FR30 | The owner must be able to manage student records. | Must Have
FR31 | The owner must be able to manage room records. | Must Have
FR32 | The owner must be able to manage rental agreements. | Must Have
FR33 | The owner must be able to manage rental terms and conditions. | Must Have
FR34 | The owner must be able to manage payment records. | Must Have
FR35 | The owner must be able to view outstanding payments. | Must Have

4.9 Shared Information and Integration
ID | Functional Requirement | Priority
FR36 | The system must store relevant accommodation information in Supabase. | Must Have
FR37 | The system must allow the ASP.NET web application to retrieve relevant information from Supabase. | Must Have
FR38 | The system must allow the Flutter mobile application to retrieve relevant student information from Supabase. | Must Have
FR39 | Changes to relevant information must be reflected in the shared data in real time. | Must Have

=====================================================================
5. USE CASES
=====================================================================
5.1 Actors
- Accommodation Owner — primary administrator using the ASP.NET web application.
- Student Tenant — end user using the Flutter mobile application.

5.2 Use Case List
ID | Use Case | Primary Actor | Priority
UC01 | Manage Student Information | Accommodation Owner | Must Have
UC02 | Manage Rooms | Accommodation Owner | Must Have
UC03 | Manage Rental Agreement | Accommodation Owner | Must Have
UC04 | Manage Terms and Conditions | Accommodation Owner | Must Have
UC05 | Record Rental Payment | Accommodation Owner | Must Have
UC06 | View Payment Records | Accommodation Owner | Must Have
UC07 | View Outstanding Payments | Accommodation Owner | Must Have
UC08 | View Accommodation Information | Student Tenant | Should Have
UC09 | View Rental Agreement | Student Tenant | Should Have
UC10 | View Terms and Conditions | Student Tenant | Should Have

5.3 Use Case Descriptions
UC01 — Manage Student Information
Purpose: Maintain accurate student tenant records. Precondition: Owner is authorised.
Main Flow: Owner opens student management → adds/selects student → enters/updates information →
system validates → system saves.
Postcondition: Student information is stored and available for authorised use.

UC02 — Manage Rooms
Purpose: Manage information about the three accommodation rooms. Precondition: Owner is authorised.
Main Flow: Owner opens room management → system displays rooms → owner selects room →
views/updates information → system saves.
Postcondition: Current room information is stored.

UC03 — Manage Rental Agreement
Purpose: Record and manage 11-month rental agreements.
Precondition: Relevant student and room exist in the system.
Main Flow: Owner selects student → creates/views agreement → records contract information →
system associates with student and room → system saves.
Postcondition: Agreement is stored and linked.

UC04 — Manage Terms and Conditions
Purpose: Digitally record rental terms and conditions. Precondition: Owner is authorised.
Main Flow: Owner opens terms section → records/updates terms → system saves → associates with
rental arrangement.
Postcondition: Terms are digitally available.

UC05 — Record Rental Payment
Purpose: Maintain organised payment records. Precondition: Student and rental agreement exist.
Main Flow: Owner selects student → selects agreement → enters payment information → system
validates → system saves.
Postcondition: Payment is recorded and associated.

UC06 — View Payment Records
Purpose: Review recorded rental payments. Precondition: Payment information exists.
Main Flow: Owner opens payment records → system displays records → owner selects
student/agreement → system displays relevant information.
Postcondition: Owner can review payment history.

UC07 — View Outstanding Payments
Purpose: Identify students with outstanding payments. Precondition: Payment information is available.
Main Flow: Owner opens outstanding payments → system identifies outstanding records → displays
relevant students and payment information.
Postcondition: Owner can identify outstanding payments.

UC08 — View Accommodation Information
Purpose: Allow students to access relevant accommodation information. Precondition: Student is authorised.
Main Flow: Student opens mobile app → accesses accommodation information → system displays
relevant information.
Postcondition: Student can view accommodation information.

UC09 — View Rental Agreement
Purpose: Allow student to view rental agreement information.
Precondition: Rental agreement is associated with the student.
Main Flow: Student opens rental information → system retrieves agreement → displays information.
Postcondition: Student can view agreement information.

UC10 — View Terms and Conditions
Purpose: Reduce misunderstandings by providing access to rental terms.
Precondition: Terms are recorded for the student's rental arrangement.
Main Flow: Student opens terms section → system retrieves applicable terms → displays terms and
conditions.
Postcondition: Student can review applicable terms.

=====================================================================
6. DATA REQUIREMENTS
=====================================================================
6.1 Student Information
Data Item | Description
Student ID | Unique identifier
Student name | Full name
Contact information | Phone, email
Room ID | Allocated room
Contract ID | Rental agreement
Student status | Active, completed, etc.

6.2 Room Information
Data Item | Description
Room ID | Unique identifier
Room description | Identifies/describes the room
Room status | Occupied or available
Student ID | Current occupant

6.3 Rental Agreement Information
Data Item | Description
Contract ID | Unique identifier
Student ID | Associated student
Room ID | Associated room
Start date | Agreement start
End date | Agreement end
Contract status | Active, completed, terminated

6.4 Terms and Conditions Information
Data Item | Description
Terms ID | Unique identifier
Contract ID | Associated agreement
Terms description | Applicable rental rules
Date recorded | When terms were added
Status | Currently applicable or not

6.5 Payment Information
Data Item | Description
Payment ID | Unique identifier
Student ID | Associated student
Contract ID | Associated agreement
Payment date | Date recorded
Amount | Payment amount
Payment status | Paid, outstanding, late
Payment period | Month/year of rental

6.6 User and Access Information
Data Item | Description
User ID | Unique system identifier
Username/email | Login identifier
Password | Securely hashed credential
User role | Owner or student
Account status | Active or inactive
Security Note: Passwords and authentication credentials must be securely hashed (e.g., bcrypt) and
must never be stored in project documentation or GitHub.

6.7 Data Relationships
- One student is associated with one accommodation room.
- A student has one rental agreement (per room/period).
- A room is associated with one rental agreement (per period). A rental agreement has applicable
  terms and conditions.
- A rental agreement has multiple associated payment records.
- A student may have multiple payment records during the contract period.

6.8 Data Validation Requirements
1. A student must have a unique student record.
2. A rental agreement must be associated with an existing student.
3. A rental agreement must be associated with an existing room.
4. A payment must be associated with an existing rental agreement.
5. Required fields must not be left empty.
6. Payment amounts must contain valid numerical values.
7. Contract dates must be valid and logical (end date after start date).
8. A payment must not be recorded without identifying the relevant student or agreement.
9. Email addresses must follow valid format.
10. Phone numbers must contain valid digits.

=====================================================================
7. EXTERNAL REQUIREMENTS
=====================================================================
7.1 User Interface Requirements
Flutter Mobile Application:
- Clear login/access screen.
- Navigation to accommodation information.
- Clear display of rental agreement information.
- Display of applicable terms and conditions.
- Smartphone-optimised layout.
- Clear feedback when information cannot be retrieved.
- Offline-friendly error messages when network is unavailable.
ASP.NET Web Application:
- Owner login/access interface.
- Dashboard for accommodation management.
- Navigation between students, rooms, agreements and payments.
- Clear visual identification of outstanding payments (e.g., colour coding).
- Understandable labels and navigation.
- Success/failure messages for operations.
- Responsive design for different screen sizes.

7.2 Hardware Requirements
Student: Android smartphone or compatible mobile device; internet connection.
Accommodation Owner: computer or laptop; internet connection; modern web browser (Chrome, Edge, Firefox).
Development Team: computers capable of running Flutter, ASP.NET, Git/GitHub and modern browsers.

7.3 Software Requirements
Component | Required Technology
Mobile application | Flutter (Dart)
Web application | ASP.NET Core
Shared backend/database | Supabase (PostgreSQL)
Source-code management | GitHub
Project planning | Microsoft Project
API communication | REST/JSON via Supabase client libraries

7.4 Browser Requirements
The ASP.NET web application must be accessible through: Google Chrome (latest), Microsoft Edge
(latest), Mozilla Firefox (latest).

7.5 Network Requirements
1. Internet connection required for Supabase communication.
2. Applications must connect to Supabase REST API.
3. System must retrieve and submit data to shared backend.
4. Appropriate feedback when network connection is unavailable.
5. Supabase real-time subscriptions for live data updates.

7.6 Security Requirements
- Authorised access required for all management functions.
- Students cannot access another student's private information.
- Owner management functions restricted to authorised owner accounts.
- Authentication information protected with secure hashing.
- Database credentials and API keys excluded from GitHub.
- Row-Level Security (RLS) enforced in Supabase. HTTPS required for all communications.
- Input validation to prevent SQL injection and XSS.
- POPIA compliance for handling personal information.

7.7 Integration Requirements
- Flutter application communicates with Supabase via REST API and Supabase client SDK.
- ASP.NET application communicates with Supabase via REST API or official .NET client.
- Shared data schema enforced in Supabase PostgreSQL database.
- Real-time updates reflected across both applications.
- Authentication handled through Supabase Auth with role-based access.

7.8 Performance Requirements
- Page/screen load times under 3 seconds under normal conditions.
- Avoid redundant data requests through caching where appropriate.
- Feedback provided when operations are processing.
- Graceful handling of common errors without application crashes.
- Support for concurrent access by owner and up to two students.

7.9 Compatibility Requirements
Component | Environment
Flutter application | Android 8.0+ (API level 26+)
ASP.NET application | Modern web browsers
Supabase | Cloud-based backend (accessible globally)
GitHub | Web-based source-code repository

=====================================================================
8. REPORTING REQUIREMENTS
=====================================================================
ID | Report | Main User | Purpose | Priority
RR1 | Student Summary | Owner | View current student tenants | Should Have
RR2 | Room Occupancy | Owner | View room status and occupants | Should Have
RR3 | Rental Agreement | Owner | Review contract information | Must Have
RR4 | Payment Report | Owner | Review payment records | Must Have
RR5 | Outstanding Payment | Owner | Identify late/outstanding payments | Must Have
RR6 | Terms and Conditions | Owner | Review recorded rental terms | Must Have

Reporting Principles:
1. Present information clearly with understandable headings.
2. Show information relevant to the selected student or room.
3. Avoid displaying unnecessary private information.
4. Allow easy identification of outstanding payments (colour coding, sorting).
5. Use shared Supabase database as the single source of truth.
6. Reflect updated information immediately after changes.

=====================================================================
9. FEASIBILITY STUDY
=====================================================================
9.1 Technical Feasibility
Evaluation:
- Technology: Flutter, ASP.NET Core and Supabase are well-documented, modern technologies with
  strong community support. Supabase provides a managed PostgreSQL backend with authentication,
  real-time subscriptions and REST APIs out of the box.
- Equipment: The development team has access to computers capable of running Flutter and ASP.NET
  development environments. The stakeholder has a computer and smartphone. No specialised hardware
  is required.
- Integration: Both Flutter and ASP.NET can communicate with Supabase via REST APIs and official
  client libraries. The integration pattern is standard and well-supported.
- Group Skills: The group has completed coursework in mobile and web development. Flutter and
  ASP.NET are technologies covered in the programme. Supabase is new but well-documented.
Limitations:
- The team has limited prior experience with Supabase real-time features.
- Integration testing between three platforms requires careful coordination.
Conclusion: Technically feasible with learning-curve allowance for Supabase advanced features.

9.2 Operational Feasibility
Evaluation:
- Stakeholder Suitability: The owner currently uses manual processes and has expressed willingness
  to transition to a digital system. The web application interface will be simpler than current
  handwritten management.
- User Acceptance: Students are familiar with mobile applications. The Flutter app provides read-only
  access to their own information, minimising training needs.
- Process Fit: The digital system directly replaces existing manual processes (recording students,
  agreements, payments) without requiring major business process redesign.
Limitations:
- The owner may require initial training on the web application.
- Internet connectivity is required; offline functionality is not included in the prototype.
Conclusion: Operationally feasible. The stakeholder is motivated and the solution fits existing
processes.

9.3 Economic Feasibility
Evaluation:
- Development Cost: Academic project with no external budget. Development tools (Flutter, ASP.NET
  Core, VS Code, GitHub) are free. Supabase free tier is sufficient for a two-room prototype.
- Operational Cost: No ongoing licensing fees. Supabase free tier includes sufficient database rows
  and API requests for prototype demonstration.
- Stakeholder Cost: The stakeholder incurs no cost. She already owns a computer and smartphone.
- Benefit: Reduced time spent on manual record-keeping, fewer conflicts with students, improved
  payment tracking.
Limitations:
- If scaled beyond three rooms, a paid Supabase tier may be required.
- No revenue generation is expected from this academic prototype.
Conclusion: Economically feasible for prototype scope. Zero direct costs for stakeholder.

9.4 Schedule Feasibility
Evaluation:
- Phase 1 Deadline: 31 August 2026 — completed on schedule.
- Remaining Phases: System design, development, testing and final presentation fit within the
  remaining academic semester.
- Task Breakdown: system design 1 week; Supabase setup and schema 3 days; ASP.NET web application
  3 weeks; Flutter mobile application 3 weeks; integration and testing 2 weeks; documentation and
  presentation prep 1 week.
Limitations:
- Student team limits parallel development capacity.
- Academic deadlines for other modules may reduce available development time.
- Stakeholder availability for testing and feedback may delay iterations.
Conclusion: Feasible with disciplined time management. Buffer time was reserved for integration
challenges (see the final Microsoft Project schedule, Section 17.8).

9.5 Legal Feasibility
Evaluation:
- Data Privacy: The system will store student personal information (names, contact details, payment
  records). This falls under POPIA (Protection of Personal Information Act) in South Africa.
Compliance Measures:
- Consent obtained from stakeholder for data storage.
- Test data used during development.
- Row-Level Security in Supabase restricts data access.
- No confidential information uploaded to GitHub.
- Passwords hashed using industry standards.
- Exclusions: The system deliberately excludes legal eviction processing and legal advice to avoid
  practising law without authority.
- Rental Contracts: The system records contract information but does not generate legally binding
  documents.
Limitations:
- Full POPIA compliance audit is beyond academic project scope.
- The team is not legal experts; the system is a prototype, not a production legal tool.
Conclusion: Legally feasible for prototype purposes with appropriate privacy safeguards and clear
limitations.

9.6 Ethical Feasibility
Evaluation:
- Information Use: Information is used solely for accommodation management as consented by the
  stakeholder. No data mining or secondary use.
- Stakeholder Treatment: The stakeholder is treated fairly — she receives a solution to her genuine
  problem at no cost, and her time is respected through efficient meetings.
- Student Privacy: Student tenants' information is protected. They can only access their own records.
- Academic Honesty: All requirements are based on actual stakeholder evidence, not assumptions.
  External sources are acknowledged.
- Transparency: The stakeholder understands the prototype limitations (two rooms, no payment
  processing, no legal features).
Limitations:
- Using real student data for testing would be unethical; test data must be used.
- The prototype must not be misrepresented as a production-ready system.
Conclusion: Ethically feasible with responsible information handling and honest representation of
capabilities.

9.7 Overall Feasibility Decision
Decision: FEASIBLE WITH CHANGES
The project is feasible within the academic context provided the following conditions are met:
1. Scope remains strictly limited to two rooms and excluded features are not added.
2. Supabase free tier limitations are monitored; schema design must be efficient.
3. Schedule buffer is maintained for integration testing.
4. Only test data is used during development; real student data is protected.
5. The stakeholder understands this is a prototype, not a commercial product.
The six feasibility areas all support proceeding with the project, but the schedule and technical
integration risks require active management.

=====================================================================
10. PROJECT RISK REGISTER
=====================================================================
10.1 Risk Identification and Analysis
Risk ID | Category | Risk Statement | L | I | Score | Level | Mitigation Action | Contingency Action | Risk Owner
R01 | Stakeholder | Stakeholder becomes unavailable for meetings, feedback or testing. | 4 | 4 | 16 | High | Schedule meetings in advance; multiple contact methods; structured agendas. | Use documented requirements as baseline; remote meetings; email confirmation. | Matlhoane L
R02 | Technical | Supabase free-tier limits exceeded during development or demonstration. | 3 | 3 | 9 | Medium | Monitor usage; optimise schema; minimise API calls. | Archive old test data; upgrade only if absolutely necessary. | Mohlomi R.D
R03 | Technical | Integration failures between Flutter, ASP.NET and Supabase (API mismatches, auth errors). | 4 | 4 | 16 | High | Official client libraries; test API endpoints independently first. | Fallback error handling; mock data layers; consult Supabase docs/forums. | Both members
R04 | Project | Scope creep beyond two rooms (multiple properties, advanced accounting). | 3 | 4 | 12 | High | Strict traceability matrix; refer to exclusions list; formal change requests. | Reject/defer out-of-scope features to post-prototype phase. | Matlhoane L
R05 | Resource | Team members fall behind schedule (illness, academic pressure). | 4 | 4 | 16 | High | Detailed MS Project schedule; clear handover points; weekly check-ins. | Re-prioritise Should-Have to Could-Have; redistribute tasks. | Mohlomi R.D
R06 | Technical | Outstanding payment identification logic becomes overly complex. | 3 | 3 | 9 | Medium | Simplify logic; clear status flags (paid, outstanding, late). | Basic manual-flagging version first; automate later. | Mohlomi R.D
R07 | Security | Student/payment data exposed via insecure GitHub commits or weak RLS. | 2 | 5 | 10 | High | RLS in Supabase; env variables for keys; .gitignore; security review before commits. | Rotate exposed credentials; clean Git history (BFG); notify stakeholder. | Matlhoane L
R08 | Environmental | Unreliable internet at stakeholder location or during presentation. | 3 | 3 | 9 | Medium | Offline screenshots and recordings; mobile hotspot; reliable venue Wi-Fi. | Prerecorded video walkthrough as backup. | Mohlomi R.D
R09 | Schedule | Insufficient time for comprehensive testing. | 4 | 3 | 12 | Medium | Unit testing during development; dedicated testing sprint in MS Project. | Prioritise Must-Have testing; known-issue list for presentation. | Both members
R10 | Technical | Flutter UI does not render correctly on specific Android device. | 3 | 2 | 6 | Medium | Test on multiple emulators/screen sizes; responsive widgets. | Adjust layouts; web-based fallback if mobile fails. | Matlhoane L
R11 | Technical | MS Project file corruption or version incompatibility. | 2 | 4 | 8 | Low | Regular backups; cloud storage; export PDF as secondary record. | Reconstruct from GitHub history and meeting notes. | Mohlomi R.D
R12 | Technical | GitHub access issues or merge conflicts disrupt development. | 2 | 3 | 6 | Medium | Feature branches; clear commit messages; resolve conflicts immediately; local backups. | GitHub Desktop conflict resolution; revert to last stable commit. | Both members

10.2 Risk Scoring Legend
Measure | Meaning
Likelihood | 1 = Rare, 2 = Unlikely, 3 = Possible, 4 = Likely, 5 = Almost Certain
Impact | 1 = Negligible, 2 = Minor, 3 = Moderate, 4 = Major, 5 = Catastrophic
Score | Likelihood × Impact
Level | 1–6 = Low, 8–12 = Medium, 15–25 = High

10.3 Three Highest Project Risks
1. R01 — Stakeholder Unavailability (Score 16): Without stakeholder engagement, requirements cannot
   be validated and acceptance criteria cannot be verified.
2. R03 — Integration Failures (Score 16): The three-platform architecture is the core technical
   challenge; integration failure would prevent the system from functioning as an integrated solution.
3. R05 — Team Member Schedule Delays (Score 16): One member falling behind affects a large share of
   team capacity.

=====================================================================
11. REQUIREMENTS CHANGE LOG
=====================================================================
This log records important changes made to requirements after the initial Phase 1 SRS, following
stakeholder feedback, feasibility analysis and risk assessment.
Change ID | Date | Section Changed | Description | Change Reason | Approved By
CL01 | 20 Aug 2026 | 1.6 Scope | Added "Advanced analytics or predictive reporting" to Out of Scope. | Exceeds academic timeframe and two-room scope. | Group consensus
CL02 | 22 Aug 2026 | 4.6 | Changed FR24 from Must Have to Should Have; FR22–FR23 remain Must Have. | Schedule risk R06 identified complexity. | Group consensus
CL03 | 24 Aug 2026 | 7.6 Security | Added explicit requirement for Row-Level Security (RLS) in Supabase and POPIA compliance. | Data privacy obligations for student personal information. | Group consensus
CL04 | 26 Aug 2026 | 2.5.3 / 7.7 | Added real-time data synchronisation as a specific Supabase requirement. | Stakeholder confirmed immediate updates would improve trust. | Stakeholder confirmation
CL05 | 28 Aug 2026 | 1.6.2 | Added "Automatic eviction or contract termination" to Out of Scope with explicit justification. | Automating legal consequences could be misused. | Group consensus
CL06 | 29 Aug 2026 | 4.9 / 7.7 | Clarified Flutter uses Supabase client SDK and ASP.NET uses REST API or .NET client. | Platform-appropriate integration methods. | Group consensus
CL07 | 30 Aug 2026 | 9.4 Schedule | Reduced system design estimate to accommodate integration testing buffer. | Risk R09 mitigation required schedule adjustment. | Group consensus
CL08 | 20 Oct 2026 | 17 (new) | Phase 3 implementation confirmed all Must-Have FRs delivered; minor date adjustments recorded in MS Project actuals. | Actual progress during implementation. | Group consensus

=====================================================================
12. REFINED PROJECT SCOPE
=====================================================================
12.1 Confirmed In-Scope Deliverables
1. Flutter Mobile Application: Student login, view accommodation info, view rental agreement, view
   terms and conditions.
2. ASP.NET Web Application: Owner dashboard, student management, room management, rental agreement
   management, terms management, payment recording, outstanding payment identification, basic reports.
3. Supabase Backend: PostgreSQL database schema, authentication, Row-Level Security, REST API access
   for both applications, real-time subscriptions.
4. Project Documentation: Updated SRS, Microsoft Project plan, GitHub repository with organised
   documentation, ITC327W Progress Tracker.
5. Stakeholder Evidence: Meeting notes, requirement confirmations, email/WhatsApp communications.

12.2 Explicitly Excluded (Not in Prototype)
- Direct bank payment processing or integration.
- Legal eviction procedures or automated contract termination.
- Legal advice or legally binding document generation.
- Government accreditation processes.
- University residence management.
- Multi-property landlord management.
- Full accounting software (general ledger, tax reporting).
- Offline mode / local database sync.
- Push notifications.
- Advanced dashboard analytics or charts.

12.3 Scope Boundaries
- Room Limit: Exactly two rooms (Room 1 and Room 2). No dynamic room addition.
- User Limit: One owner account, up to two active student accounts (one per room).
- Contract Type: 11-month fixed contracts only. No month-to-month or variable duration.
- Payment Tracking: Manual recording by owner only. No student-initiated payments.
- Data Retention: Active contract period + 3 months post-completion for prototype demonstration.

12.4 Acceptance Criteria (Refined)
1. Owner can add, view and update student records for three rooms.
2. Owner can create 11-month rental agreements linked to students and rooms.
3. Owner can record rental terms and conditions digitally.
4. Owner can record payments and identify outstanding payments visually.
5. Student can log in to the mobile app and view their own accommodation, agreement and terms information.
6. Data entered via the web app is visible in the mobile app within 5 seconds (real-time sync).
7. All "Must Have" functional requirements are implemented and tested.
8. No confidential stakeholder or student data is present in GitHub.
9. Stakeholder confirms the prototype solves her three main problems: handwritten records, verbal
   terms, payment tracking.

=====================================================================
13. NON-FUNCTIONAL REQUIREMENTS
=====================================================================
13.1 Usability Requirements
NFR-U01: The web application must be usable by the accommodation owner without prior software
training. All labels must use plain language (e.g., "Record Payment" not "POST /payments").
NFR-U02: The mobile application must follow Android Material Design guidelines for intuitive navigation.
NFR-U03: Error messages must explain what went wrong and how to fix it, not display technical stack traces.
NFR-U04: The owner dashboard must present outstanding payments in red/orange visual indicators for
immediate recognition.
NFR-U05: All forms must indicate required fields with asterisks and provide inline validation feedback.

13.2 Performance Requirements
NFR-P01: Web application pages must load within 3 seconds on a standard broadband connection.
NFR-P02: Mobile application screens must load within 3 seconds on 4G/LTE connection.
NFR-P03: Database queries for student, room and payment lists must execute within 1 second for up to
10 records.
NFR-P04: Real-time updates between web and mobile must propagate within 5 seconds under normal
network conditions.
NFR-P05: The system must support concurrent access by the owner and up to two students simultaneously
without performance degradation.

13.3 Security Requirements
NFR-S01: All API communication must use HTTPS/TLS 1.2 or higher.
NFR-S02: Passwords must be hashed using bcrypt or equivalent adaptive hashing algorithm.
NFR-S03: Supabase Row-Level Security (RLS) must enforce that students can only read their own records.
NFR-S04: API keys, database credentials and service role keys must be stored in environment variables,
never in source code.
NFR-S05: The system must implement input validation to prevent SQL injection, XSS and CSRF attacks.
NFR-S06: Failed login attempts must be rate-limited to prevent brute-force attacks.
NFR-S07: Personal information must be handled in accordance with POPIA principles (minimality, purpose
specification, security safeguards).

13.4 Availability Requirements
NFR-A01: The system must be available during demonstration periods (scheduled presentations and
stakeholder meetings).
NFR-A02: Supabase free tier uptime (99.9% SLA) is acceptable for prototype purposes.
NFR-A03: If Supabase is unreachable, applications must display a user-friendly "System temporarily
unavailable" message rather than crashing.
NFR-A04: Critical data (student records, agreements, payments) must be backed up before major schema
changes.

13.5 Quality Requirements
NFR-Q01: Code must follow consistent naming conventions and include comments for complex logic.
NFR-Q02: The system must handle invalid inputs gracefully without data corruption.
NFR-Q03: All "Must Have" features must be tested with at least one positive and one negative test case.
NFR-Q04: Documentation (README, API notes, setup instructions) must be current and accurate in GitHub.

=====================================================================
14. INTEGRATION REQUIREMENTS
=====================================================================
14.1 Architecture Overview
The Student Accommodation Management System follows a three-tier architecture with a shared backend:
the Flutter mobile application (student users) and the ASP.NET web application (owner users) both
connect to one shared Supabase backend (PostgreSQL database, Authentication + RLS, Realtime
subscriptions, REST/client APIs).
[ PLACEHOLDER — INSERT: System architecture diagram (from Phase 2) ]

14.2 Data Integration
- Single shared Supabase PostgreSQL database as the source of truth for both applications.
- Both applications use the same table schema (Section 6); no duplicated or separate databases.
- Supabase Table Editor used as verification point during the shared-process demonstrations.

14.3 Communication Integration
- Flutter → Supabase: official Supabase Dart client SDK (REST under the hood).
- ASP.NET → Supabase: official .NET client or REST API.
- Supabase Realtime: PostgreSQL change events pushed to subscribed clients.

14.4 Real-Time Integration
- Realtime subscriptions on payments and agreements reflect owner-made changes in the student app.
- Fallback: If real-time connection fails, Flutter refreshes data on screen load or pull-to-refresh
  gesture.

14.5 Security Integration
- RLS Policies: owners can read/write all records in their scope; students can only read records where
  student_id matches their authenticated user ID; students cannot read other students' records; no
  unauthenticated access to any table.
- API Key Management: Flutter uses the public anon key. ASP.NET server-side operations use the service
  role key stored securely. The service role key is never exposed to the client-side web application;
  it resides only on the ASP.NET server.

14.6 Error Handling Integration
- Network Errors: Both applications detect Supabase connectivity issues and display appropriate messages.
- Auth Errors: Expired sessions redirect to login screens in both applications.
- Data Validation Errors: PostgreSQL constraint messages parsed and displayed as user-friendly equivalents.

14.7 Deployment Integration
- GitHub: Flutter and ASP.NET source in separate directories within the same repository. Supabase
  migrations (SQL schema) stored in /supabase/migrations.
- Environment Configuration: environment-specific configuration files (not committed to GitHub)
  containing Supabase URL and API keys.

=====================================================================
15. SUPPLEMENTAL INFORMATION
=====================================================================
15.1 Requirements Prioritisation Summary
Must Have (Essential for first working prototype):
- Student, room, contract, terms, payment management.
- Outstanding payment identification.
- Owner web management functions.
- Student mobile access functions.
- Supabase shared data storage.
- Authentication and RLS security.
Should Have (Important but refinable):
- Room availability indication.
- Student information access (mobile).
- Student and room summary reports.
- Real-time data synchronisation.
Could Have (Optional if time permits):
- Additional dashboard widgets.
- Push notifications for payment reminders.
- Advanced filtering and sorting.
- Export reports to PDF/Excel.

15.2 Requirements Traceability
Stakeholder Problem | System Response | Related Requirements
Handwritten records | Digital student, room, contract and payment records | FR1–FR24
Terms communicated verbally | Digital terms and conditions with student access | FR13–FR16, NFR-U01
Conflicts from misunderstandings | Students can access applicable terms and conditions | FR15, FR16, UC10
Students pay late | Outstanding payment tracking and visual alerts | FR20–FR24, NFR-U04
Difficulty monitoring payments | Payment records, reports and real-time updates | FR17–FR24, RR4–RR5
Difficulty managing accommodation info | Centralised web dashboard | FR29–FR35
Information needs to be shared | Supabase shared backend with real-time sync | FR36–FR39, 14.4

15.3 Project Constraints Summary
1. Academic semester deadline.
2. Two-room scope limit.
3. Six-member student development team with limited time.
4. Mandatory technology stack (Flutter, ASP.NET, Supabase).
5. No budget for paid services.
6. Prototype focus only.

15.4 Definitions and Abbreviations
(See Section 1.7)

15.5 Project Scope Boundary
(See Section 12 — Refined Project Scope)

=====================================================================
16. STAKEHOLDER EVIDENCE
=====================================================================
16.1 Stakeholder Profile Confirmation
Organisation: Makhele Stud Accommodation
Type: Private student accommodation (unaccredited, off-campus)
Stakeholder Name: Pulane Makhele Constance
Contact: Makhele P.C, 0655674393, makhelepulane1@gmail.com
Role: Owner and manager of two student accommodation rooms

16.2 Interview Summary
Date: 24 Aug 2026
Method: In-person / Microsoft Teams
Attendees: Matlhoane Lebohang (Facilitator ), Mohlomi Ramadulwane Daniel (Timekeeper), Kayane Thabo William ( Note-Taker ), Moloi Letlotlo (Requirements Checker), Kalo KI, Tshabalala MV, Makhele PC (Stakeholder)
Key Questions and Confirmed Responses:
1. Current Process: Stakeholder confirmed she manages three rooms with handwritten records and verbal
   terms under 11-month contracts.
2. Main Problem: Difficulty organising records, misunderstandings about terms, tracking late payments
   while contracts are active.
3. Mobile App Users: Students should view their own accommodation, agreement and terms information.
4. Web App Users: Owner should manage students, rooms, contracts, terms and payments.
5. Information to Store: Student details, room info, agreement dates, terms, payment amounts and dates,
   payment status.
6. Reports Needed: Payment summary, outstanding payment list, room occupancy status.
7. Confirmation: Stakeholder agreed that a digital system replacing handwritten records and verbal
   terms would solve her main difficulties.

16.3 Requirement Confirmations
The stakeholder confirmed the following requirements after reviewing the organised findings:
- Replacement of handwritten records with digital student and room records.
- Digital recording of 11-month rental agreements.
- Digital recording of terms and conditions (no longer verbal only).
- Payment recording and outstanding payment identification.
- Student mobile access to personal accommodation information.
- Three-room scope is correct and sufficient for initial prototype.
- Exclusions (bank payments, legal eviction, accreditation) are acceptable.
Confirmation Method: Email / WhatsApp / Signed meeting notes
Date: 26–28 Aug 2026

16.4 Communication Evidence Sample
Email Confirmation:
Subject: ITC327W Project — Requirement Confirmation
To: makhelepulane1@gmail.com
From: Matlhoane L (222059872)
Date: 24 Aug 2026
"Dear Ms Makhele, Thank you for participating in our interview for the Student Accommodation
Management System. Based on our discussion, we have identified the following needs: (1) Digital
management of student and room records; (2) Digital recording of rental agreements and terms;
(3) Payment tracking with outstanding payment alerts; (4) Student mobile access to personal
information. Please confirm that these correctly represent your needs."
Stakeholder Response: "Yes, that is correct. I need help with organising my records and tracking
payments. The three rooms are enough for now."
[ APPENDIX A — PLACEHOLDER: insert stakeholder confirmation letter/email screenshot ]
[ APPENDIX B — Meeting photo / attendance evidence: documented in the stakeholder interview record
  of 24 August 2026 (Section 16.2), signed by the stakeholder and all group members; retained in the
  project file and available on request. ]
[ APPENDIX C — Stakeholder feedback communications: consolidated in the formal confirmation letter
  (Appendix A), which supersedes informal message records. ]

16.5 Meeting Notes Evidence
Meeting 1: Initial Stakeholder Engagement — 20 Aug 2026. Purpose: introduce project and identify
stakeholder problem. Outcome: stakeholder agreed to participate; problem identified as manual
record-keeping.
Meeting 2: Requirements Interview — 24 Aug 2026. Purpose: gather detailed requirements. Outcome:
10 interview questions answered; needs documented.
Meeting 3: Requirements Confirmation — 30 Aug 2026. Purpose: present organised findings for
validation. Outcome: stakeholder confirmed understanding of problems and proposed solution scope.
Meeting 4: Architecture Confirmation — 10 Sep 2026. Purpose: present system architecture for
confirmation. Outcome: architecture confirmed (Appendix A).

16.6 Confidentiality Statement
All stakeholder evidence has been handled responsibly:
- No unnecessary personal information is included.
- Stakeholder contact details are included only where required for project verification.
- No passwords, financial account details or private student records are included.
- All evidence is stored securely and shared only with the project lecturer.

=====================================================================
17. IMPLEMENTATION AND FINAL PROTOTYPE (PHASE 3)
=====================================================================
17.1 Implementation Overview
This section documents the final working prototype developed for Assessment 3. All three components
were implemented as one integrated solution sharing a single Supabase backend, as approved in the
Phase 1 and Phase 2 baselines.

17.1.1 Shared Supabase Backend
- PostgreSQL database implemented according to the approved ERD: users (Supabase Auth), students,
  rooms, rental_agreements, terms_and_conditions and payments tables, with primary keys, foreign keys
  and the relationships defined in Section 6.
- Supabase Authentication configured for owner and student roles; Row-Level Security (RLS) policies
  enforce that students can only read their own records (NFR-S03) and management write operations are
  restricted to the authorised owner account.
- Database operations (insert, select, update) implemented for all main records using demonstration
  (dummy) data only; no real student data is stored.
- Both the Flutter and ASP.NET applications connect to the same Supabase project, so records and
  values are consistent across both applications.
- Schema/migration scripts are stored in /supabase/migrations in the GitHub repository; no credentials
  or secret keys are committed.

17.1.2 Flutter Mobile Application (Student)
- Student login screen using Supabase Auth with session handling and expired-session redirect.
- Student dashboard with navigation to My Accommodation, My Rental Agreement and Terms & Conditions.
- All screens retrieve the logged-in student's own records; RLS prevents access to other students'
  information.
- Input validation and user-friendly error messages (e.g., "System temporarily unavailable" on network
  failure, per NFR-A03).
- Real-time subscription / refresh-on-load ensures owner-made updates are reflected within seconds
  (NFR-P04).

17.1.3 ASP.NET Web Application (Owner)
- Owner login and accommodation management dashboard (FR29).
- Student management: add, view and update student tenant records (FR1–FR3).
- Room management: view the two rooms, occupants and occupancy status (FR5–FR7).
- Rental agreement management: create 11-month agreements linked to a student and room, with start/end
  dates (FR8–FR12).
- Terms and conditions management: record and update rental terms, associated with agreements
  (FR13–FR16).
- Payment management: record payments, view payment history, update payment status, and identify
  outstanding/late payments with red/orange indicators (FR17–FR24).
- Plain-language labels, required-field markers, inline validation and success/failure messages
  (NFR-U01, NFR-U05).

17.2 Requirement-to-Function Traceability (Working Status)
Approved Requirement | Implemented Function | Status
FR1–FR3 Add / view / update student records | ASP.NET: Student Management page | Working
FR4 Associate student with a room | ASP.NET: student–room allocation on agreement creation | Working
FR5–FR7 View rooms, occupants, availability | ASP.NET: Room Management page | Working
FR8–FR12 Create/view 11-month agreements linked to student & room | ASP.NET: Rental Agreement Management | Working
FR13–FR16 Record/update terms; associate with agreement | ASP.NET: Terms & Conditions Management | Working
FR15 / FR28 Student views applicable terms & conditions | Flutter: Terms & Conditions screen | Working
FR17–FR21 Record/view/update payments linked to agreement | ASP.NET: Payment Management | Working
FR22–FR24 Identify outstanding payments; list students owing | ASP.NET: Outstanding Payments view (colour-coded) | Working
FR25 Student can access mobile application | Flutter: Login + dashboard | Working
FR26–FR27 Student views own accommodation & agreement info | Flutter: My Accommodation / My Rental Agreement screens | Working
FR29–FR35 Owner dashboard and full management functions | ASP.NET web application | Working
FR36–FR38 Shared Supabase storage; both apps retrieve from Supabase | Supabase backend + both clients | Working
FR39 Real-time reflection of changes in shared data | Supabase Realtime subscriptions + refresh-on-load | Working

17.3 Demonstrated Shared Processes (Integration Evidence)
Process 1 — Data Submission and Retrieval (Owner → Supabase → Student)
Workflow: the owner logs into the ASP.NET web application and records a new rental payment for a
student (user action → ASP.NET → Supabase insert into the payments table). The student then opens the
Flutter mobile application and retrieves the same payment record (Flutter → Supabase select). The
Supabase Table Editor is shown in parallel to prove the record exists in the shared database.

Process 2 — Shared Update and Display (Owner updates; Student sees updated result)
Workflow: the owner updates an existing record — e.g., marks a payment as received or updates rental
terms — through the ASP.NET web application (authorised action → Supabase update). The Flutter mobile
application retrieves and displays the updated value (via realtime subscription or refresh-on-load),
and the owner re-opens the record in the web app to confirm both applications show identical,
consistent values.

17.4 Screenshots of Implemented Interfaces
[ PLACEHOLDER — INSERT: SCREENSHOT 1 — Flutter: Student login screen ]
[ PLACEHOLDER — INSERT: SCREENSHOT 2 — Flutter: Student dashboard / My Accommodation ]
[ PLACEHOLDER — INSERT: SCREENSHOT 3 — Flutter: My Rental Agreement ]
[ PLACEHOLDER — INSERT: SCREENSHOT 4 — Flutter: Terms & Conditions screen ]
[ PLACEHOLDER — INSERT: SCREENSHOT 5 — ASP.NET: Owner login ]
[ PLACEHOLDER — INSERT: SCREENSHOT 6 — ASP.NET: Owner dashboard ]
[ PLACEHOLDER — INSERT: SCREENSHOT 7 — ASP.NET: Student management ]
[ PLACEHOLDER — INSERT: SCREENSHOT 8 — ASP.NET: Rental agreement creation ]
[ PLACEHOLDER — INSERT: SCREENSHOT 9 — ASP.NET: Record payment + Outstanding payments (colour-coded) ]
[ PLACEHOLDER — INSERT: SCREENSHOT 10 — Shared Process 1: payment recorded in web app → same record
  in Supabase Table Editor → visible in Flutter app ]
[ PLACEHOLDER — INSERT: SCREENSHOT 11 — Shared Process 2: updated record → Flutter shows updated
  value; web app confirms consistency ]
[ PLACEHOLDER — INSERT: SCREENSHOT 12 — Supabase: tables matching approved ERD + Authentication/RLS enabled ]

17.5 Approved Changes During Implementation
- Scope kept strictly to the two approved rooms and 11-month contracts; no out-of-scope features added.
- Real-time updates delivered through Supabase Realtime with a refresh-on-load fallback in Flutter
  (per Phase 2 architecture).
- ASP.NET server-side operations use the service-role key stored only in server environment variables;
  the anon key is used by Flutter; no keys committed to GitHub (NFR-S04).
- Only dummy demonstration data used; no real student personal information stored (Section 9.5).

17.6 Known Limitations
- Prototype limited to the stakeholder's two rooms; no dynamic room addition (Section 12.3).
- No offline mode or local database synchronisation (Section 12.2).
- No push notifications; students see updates on app open/refresh or realtime while the app is open.
- Reports are basic summaries; no advanced analytics.
- Payment recording is manual by the owner only; no bank integration (out of scope).

17.7 Source Code and Repository
GitHub Repository (working link): https://github.com/222093279/BizUp_Group_G
- Repository structure: mobile/ (Flutter source), web/ (ASP.NET source), supabase/migrations/
  (schema scripts), README.md with setup and run instructions.
- The submitted ZIP and the GitHub repository contain the same version demonstrated to the panel.
- No passwords, secret keys or confidential information are included in the repository or ZIP.

17.8 Final Microsoft Project Schedule
The Microsoft Project plan was updated to reflect actual progress, responsibilities, completed
development work and remaining tasks. The editable .mpp file is submitted with this SRS.
[ PLACEHOLDER — INSERT: clear screenshot of the final Microsoft Project Gantt/schedule reflecting
  actual progress (all phases 100% complete, ending 25 Oct 2026) ]

17.9 Project Status Summary
All Must-Have functional requirements (FR1–FR39) were implemented and demonstrated working against
the shared Supabase backend. Both applications launch, display the approved screens, validate input,
enforce authentication and permitted access, and demonstrate the two required shared processes end to
end with consistent data. The prototype is complete within the approved scope and ready for
stakeholder evaluation.

=====================================================================
END OF UPDATED SOFTWARE REQUIREMENTS SPECIFICATION
Document Version: (Phases 1–3)
Last Updated: 25 OCTOBER 2026
Prepared by: Matlhoane L, Mohlomi RD, Moloi L, Kayane TW, Kalo KI, Tshabalala MV

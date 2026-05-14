1. Difference Between App, Object, Record, and Field

| Term       | Explanation                                                                        | Example                  |
| ---------- | ---------------------------------------------------------------------------------- | ------------------------ |
| **App**    | A collection of tabs, objects, and tools designed for a specific business purpose. | College Management App   |
| **Object** | A database table used to store information in Salesforce.                          | Student Object           |
| **Record** | A single entry or row inside an object.                                            | One student’s details    |
| **Field**  | A column that stores specific information in an object.                            | Name, Roll Number, Email |


2. Standard vs Custom Objects

| Standard Objects                         | Custom Objects                                      |
| ---------------------------------------- | --------------------------------------------------- |
| Pre-built objects provided by Salesforce | User-created objects based on business requirements |
| Already available in Salesforce          | Created manually by developers or admins            |
| Used for common CRM processes            | Used for organization-specific processes            |
| Examples: Account, Contact, Opportunity  | Examples: Student, Faculty, Course                  |


3. College Data Model
Objects Used
1.Student
2.Faculty
3.Course
4.Department
5.Attendance

Relationships
| Object 1   | Relationship | Object 2   |
| ---------- | ------------ | ---------- |
| Department | Has Many     | Students   |
| Department | Has Many     | Faculty    |
| Faculty    | Teaches      | Course     |
| Student    | Enrolled In  | Course     |
| Student    | Has          | Attendance |

Simple Diagram
Department
   |
   |----< Student >---- Course
   |
   |----< Faculty >---- Course

Student ----< Attendance


Explanation
1.One department can contain many students and faculty members.
2.One faculty member can teach multiple courses.
3.Students can enroll in courses.
4.Attendance records are linked to students.


4. Formula Fields
What is a Formula Field?

A Formula Field automatically calculates values based on other fields.

Example 1 – Student Full Name
Formula
First_Name + " " + Last_Name
Explanation

This formula combines first name and last name automatically.

Example 2 – Attendance Percentage
Formula
(Classes_Attended / Total_Classes) * 100
Explanation

It calculates the attendance percentage automatically.

Example 3 – Pass or Fail
Formula
IF(Marks >= 35, "Pass", "Fail")
Explanation

If marks are greater than or equal to 35, the result will be “Pass”; otherwise “Fail”.


5. Validation Rules
What is a Validation Rule?

Validation Rules prevent users from entering invalid data into Salesforce.

Example 1 – Email Validation
Rule
Email should contain "@"
Explanation

The system shows an error if the email format is incorrect.

Example 2 – Attendance Limit
Rule
Attendance cannot exceed 100%
Explanation

Users cannot enter invalid attendance percentages.

Example 3 – Mandatory Phone Number
Rule
Phone number field cannot be empty
Explanation

The record cannot be saved without a phone number.


6. Reflection – Why Structured Enterprise Data Matters

Structured enterprise data is important because it helps organizations store, manage, and access information efficiently. In Salesforce, structured data improves accuracy, reduces duplicate records, and helps businesses make better decisions.

For a college management system:

Student details can be managed easily.
Faculty and course information remain organized.
Reports and analytics become faster.
Automation reduces manual work.
Data consistency improves communication between departments.

Structured data helps organizations increase productivity, improve decision-making, and maintain reliable records.

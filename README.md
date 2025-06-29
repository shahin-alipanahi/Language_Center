# Language Center – MySQL Database Project

This project defines the backend database structure for a language learning center using MySQL. It models real-world entities such as students, professors, classes, and exams, and is designed to support operations like enrollment tracking, placement testing, and payment processing.

---

## Tables Included

The database schema consists of the following tables:

- languages – Available languages offered by the center  
- course – Specific language courses (e.g., English A1)  
- professor – Teachers assigned to courses  
- student – Registered learners and their payment status  
- class – Class schedules and delivery method (online/in-person)  
- exam – Scheduled exams linked to courses and students  
- placement_exam – English placement tests before course enrollment

---

## File Contents

This repository contains:

- INSERT statements to populate the database with realistic test data
- SQL queries to analyze project functionality

---

## Sample Data Insertion and SQL Query 

Here’s an example:

```sql
/*INSERT statement for the student table*/
INSERT INTO student (course_id, s_name, s_age, payment_state, payment_type)
VALUES (2, 'Sam Toutounchi', 24, 'NOT_Confirmed', 'credit_cart');


/*Count of students where the payment_satate is "confirmed" and the class's type is "online"*/
SELECT COUNT(student_id)
FROM student st
JOIN class cl ON cl.course_id = st.course_id
WHERE payment_state = "Confirmed"
AND class_type = "online";




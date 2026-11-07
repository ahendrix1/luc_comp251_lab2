## School ER Business Rules

### Entities
**INSTRUCTOR** - An Instructor must teach at least one Course, but can teach multiple. Each Instructor is identified by an Instructor_no, and has an instructor_name and instructor_faculty status associated.

**STUDENT** - A Student fills exactly one Seat and each student can take multiple Courses. Students are identified by Student_id, and associated with Student_name and Student_address.

**SEAT** - Filled by exactly one Student. Identified by Seat_no and associated with Seat_position

**COURSE** - A Course is taught by exactly one Instructor, has at least one Section, and is taken by at least one Student. A course is identified by Course_name and Course_number.

**SECTION** - A Section is had by multiple Courses and is taught by exactly one Professor. Each section is identified by Section_number.

**PROFESSOR** - A professor may teach multiple Sections. They are identified by Professor_id, and associated with Professor_name and Professor_faculty status.


### Relationships
An **INSTRUCTOR** <ins>teaches</ins> one or multiple **COURSES**, each **COURSE** is <ins>taught</ins> by exactly one **INSTRUCTOR**.

A **STUDENT** <ins>takes</ins> one or multiple **COURSES**, each **COURSE** is <ins>taken</ins> by one or multiple **STUDENTS**.

A **STUDENT** <ins>fills</ins> exactly one **SEAT**, each **SEAT** is <ins>filled</ins> by exactly one **STUDENT**.

A **COURSE** <ins>has</ins> multiple **SECTIONS**, each **SECTION** is <ins>had</ins> by multiple **COURSES**.

A **PROFESSOR**<ins>teaches</ins> zero, one, or multiple **SECTIONS**, each **SECTION** is <ins>taught</ins> by exactly one **PROFESSOR**.

### Assumptions

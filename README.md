## School ER Business Rules

### Entities
**INSTRUCTOR** - An Instructor must teach at least one Course, but can teach multiple. Each Instructor is identified by an Instructor_no, and has an instructor_name and instructor_faculty status recorded.

**SEAT** - Filled by exactly one Student. Identified by Seat_no and recorded with Seat_position

**STUDENT** - A Student fills exactly one Seat and each student can take multiple Courses. Students are identified by Student_id, and Student_name and Student_address are recorded.

**COURSE** - A Course is taught by exactly one Instructor, has at least one Section, and is taken by at least one Student. A course is identified by Course_name and Course_number.

**SECTION** - A Section is had by multiple Courses and is taught by exactly one Professor. Each section is identified by Section_number.

**COURSE_SECTION_LIST** - A Course_Section has exactly one association with a Course, and exactly one association with a Section. They are weak entities, identified by the composite of the Course_number and Section_number.

**STUDENT_COURSE_LIST** - A Student_Course has exactly one association with a Student, and exactly one association with a Course. They are weak entities, identified by the Student_id.

**PROFESSOR** - A professor may teach multiple Sections. They are identified by Professor_id, and record the Professor_name and Professor_faculty status.

### Relationships
An **INSTRUCTOR** <ins>teaches</ins> one or multiple **COURSES**, each **COURSE** is <ins>taught</ins> by exactly one **INSTRUCTOR**.

A **STUDENT** <ins>takes</ins> one or multiple **COURSES**, each **COURSE** is <ins>taken</ins> by one or multiple **STUDENTS**. A **STUDENT_COURSE_LIST** <ins>takes</ins> exactly one **COURSE**, and is <ins>taken</ins> by exactly one **STUDENT**.

A **STUDENT** <ins>fills</ins> exactly one **SEAT**, each **SEAT** is <ins>filled</ins> by exactly one **STUDENT**.

A **COURSE** <ins>has</ins> multiple **SECTIONS**, each **SECTION** is <ins>had</ins> by multiple **COURSES**. A **COURSE_SECTION_LIST** <ins>has</ins> exactly one **COURSE**, and is <ins>had</ins> by exactly one **SECTION**.

A **PROFESSOR**<ins>teaches</ins> zero, one, or multiple **SECTIONS**, each **SECTION** is <ins>taught</ins> by exactly one **PROFESSOR**.

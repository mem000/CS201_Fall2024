# Java Programming Exercise: Student Grades Management System

## Objective:

In this exercise, you will create a Student Grades Management System in Java. The program will allow users to:

1. Enter the number of students and courses.
2. Input each student's full name, ID, and their grades in multiple courses.
3. Provide various options for displaying data, such as GPA calculation and grade breakdown.

## Concepts Covered:

- Elementary Programming
- Selection Statements
- Loops
- Methods (with static methods for better organization)
- 1D and 2D Arrays
- Strings and Characters

## Details:

1. **Input**: The user will enter the number of students, courses, student names, IDs, and their grades.
2. **Output**: The program will provide options to:
    - Display GPA for a specific student.
    - Display all grades for a specific student.
    - Display the grade for a specific student in a specific course.
    - Display all grades for a specific course.
    - End the program.
3. **Grading**: The system will assign a rating (e.g., Excellent, Very Good, Pass) for each grade.
4. **GPA Calculation**: GPA will be calculated based on the formula
   `(Sum of (course points * Credit Hours)) / Total Hours`. For simplicity, assume each course has 3 credit hours.

---

## Tips for Code Organization:

1. **Use Static Methods**: Break down the program into smaller, reusable static methods for better structure and
   readability.
    - **Example**: Separate methods for calculating GPA, displaying grades, and finding a student by ID.

2. **1D and 2D Arrays**:
    - Use 1D arrays for storing course codes and student names.
    - Use 2D arrays for storing student grades (students as rows and courses as columns).

3. **Loops and Input Validation**:
    - Use loops to iterate over students and courses, and ensure proper input validation when requesting IDs or course
      codes.

---

## Method Breakdown:

**1. Main Method**: This method will contain the main menu and user interaction.

```java
   public static void main(String[] args) {
    // Main program logic and menu options
}
 ```

**2. Helper Method: Finding a Student by ID:** This method searches for a student by their ID and returns their index.

```java
    public static int findStudentIndex(String[] studentIDs, String studentID) {
    // Search logic for student ID
}
 ```   

**3. Helper Method: Finding a Course by Code:** This method searches for a course by its code and returns the index.

```java
public static int findCourseIndex(String[] courseCodes, String courseCode) {
    // Search logic for course code
}
```

**4. Method to Display All Grades for a Specific Student:** This method displays all grades for a specific student in a
tabular format.

```java
public static void displayAllGradesForStudent(Scanner input, String[] studentNames, String[] studentIDs, double[][] grades, String[] courseCodes) {
    // Logic to display all grades for a given student
}
```

**5. Method to Display Grade for a Specific Student in a Specific Course:** This method displays a specific student's
grade for a specific course.

```java
public static void displayGradeForStudentInCourse(Scanner input, String[] studentNames, String[] studentIDs, double[][] grades, String[] courseCodes) {
    // Logic to display grade for a student in a specific course
}
```

**6. Method to Display All Grades for a Specific Course:** This method displays all student grades for a specific
course.

```java
public static void displayAllGradesForCourse(Scanner input, String[] studentNames, String[] courseCodes, double[][]
        grades) {
    // Logic to display all grades for a course
}
```

**7. Method to Calculate GPA:** This method calculates and returns the GPA for a student.

```java
public static double calculateGPA(double[] studentMarks, int numCourses) {
    // Logic to calculate GPA based on the marks
}
```

**8. Helper Method: Convert Marks to GPA Points:** This method converts a numerical marks into GPA points based on a
custom scale.

```java
public static double marksToPoints(double grade) {
// Logic to convert numerical Marks to points
}
```

**9. Helper Method: Assign Grade:** This method assigns a grade (e.g., Excellent, Pass) based on the marks.

```java
public static String assignGrade(double points) {
    // Logic to assign rating based on the points
}
```

### Sample Output:

```console
Enter number of students: 2
Enter number of courses: 3
Enter student 1 name: John Doe
Enter student 1 ID: 12345
Enter grade for course CS101: 95
Enter grade for course MATH101: 85
Enter grade for course ENG101: 75

Enter student 2 name: Jane Smith
Enter student 2 ID: 67890
Enter grade for course CS101: 88
Enter grade for course MATH101: 90
Enter grade for course ENG101: 60

Choose an option:
1. Display GPA for a student
2. Display all grades for a student
3. Display grade for a student in a specific course
4. Display all grades for a course
5. End program

Option 2 selected:
Enter student ID: 12345
------------------------------------------------
Course Code     Marks       Points       Grade
------------------------------------------------
CS101           95.00       4.50         Excellent
MATH101         85.00       3.50         Very Good
ENG101          75.00       2.50         Good
Number of failed courses: 0

Choose an option:
1. Display GPA for a student
2. Display all grades for a student
3. Display grade for a student in a specific course
4. Display all grades for a course
5. End program

Option 1 selected:
Enter student ID: 67890
------------------------------------
Student Name    GPA          Rating
------------------------------------
Jane Smith      3.33         Very Good
```

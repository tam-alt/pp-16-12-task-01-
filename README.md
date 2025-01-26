# pp-16-12-task-01
# 14_Student_marks_grade
### Introduction: Student Marks and Grades Management System
This program is a Python-based solution for managing and analyzing student marks and grades. It allows users to add, update, delete, and search student records while automatically calculating grades and total marks. With features like class performance analysis, data visualization, and a menu-driven interface, the system provides an efficient way to handle student data and gain meaningful insights. It is built using `pandas`, `matplotlib`, and `re` for seamless data management and presentation.

### Data Initialization: Storing Initial Student Data
This code initializes a student dataset with basic information, such as student IDs, names, and marks in various subjects (Math, English, and Science).
A placeholder is created for total marks (Marks) and grades (Grade).
The dataset is converted into a CSV file (students_data.csv), so the data can be reused later.
If the file already exists, the script will load the existing data instead of overwriting it.

### Student Record Management Functions
This section introduces functions to manage student records in the dataset efficiently. Below are the functions and their roles:
add_student(student_id, name, marks)
Adds a new student record to the dataset.
Parameters:
student_id: Unique identifier for the student.
name: Name of the student.
marks: List of marks in Math, English, and Science.
Automatically calculates the total marks and assigns a grade.
Updates the CSV file to include the new student.
update_student(student_id, marks)

Updates the marks of an existing student using their student_id.
Parameters:
student_id: Unique identifier for the student.
marks: Updated list of marks in Math, English, and Science.
Recalculates total marks and grade after updating.
Saves changes back to the CSV file.
If the student_id is not found, a message is displayed.
delete_student(student_id)

Deletes a student record from the dataset using their student_id.
Updates the CSV file to reflect the changes.
These functions ensure efficient addition, modification, and deletion of student records while keeping the data consistent.

Here’s the accompanying markdown explanation for this section in Colab:

### Grade Calculation Function

calculate_grade(marks)

This function determines a student's grade based on their total marks.
Grading criteria:
A: Marks 90 or above
B: Marks between 80 and 89
C: Marks between 70 and 79
F: Marks below 70
This function is used by the student management functions to assign or update grades automatically when marks are added or modified.
Class Performance Analysis
class_performance_analysis()

This function provides insights into the overall performance of the class by analyzing the dataset. Key features include:

Average Marks Per Subject

Computes the average marks for each subject (Math, English, and Science) across all students.
Top and Lowest Scorer

Identifies the student with the highest and lowest marks in the dataset for each subject.
Displays details like Student ID, Name, and marks in individual subjects.
Pass Percentage

### Visualizing Data

**`plot_data()`**

This function creates visualizations to analyze class performance:  
1. **Bar Chart**: Displays average marks per subject.  
2. **Pie Chart**: Shows the grade distribution among students.  
3. **Line Graph**: Plots individual student marks in Math for trend analysis.  

These visualizations provide a clear and interactive way to understand the data.

### Searching and Filtering

This section provides functions to retrieve specific student records or filter data based on conditions:

1. **`search_student(student_id=None, name=None)`**  
   - Searches for a student by their `Student ID` or `Name`.  
   - Displays the matching record(s).

2. **`filter_by_grade(grade)`**  
   - Filters and displays students with a specific grade (e.g., 'A', 'B').

3. **`failed_students()`**  
   - Identifies and displays students who failed in at least one subject (marks < 70).

These functions make it easy to query and analyze specific subsets of the dataset.

### Advanced Features: File Handling, Exception Handling, and RegEx

**`validate_student_id(student_id)`**

- **Purpose**: Validates the format of a given student ID using Regular Expressions (RegEx).  
- **Validation Rule**:  
  - The ID must follow the pattern: `ST-` followed by exactly **three digits** (e.g., `ST-001`, `ST-123`).  
- **Returns**:  
  - `True` if the student ID is valid.  
  - `False` if the format is incorrect.

This function ensures data integrity by enforcing consistent student ID formats.

### User Interaction: Menu-Driven Program

**`menu()`**

This function provides a user-friendly interface for managing student records. Users can interact with the program by selecting options from the menu:

1. **Add a Student**: Add a new student's details after validating the student ID.  
2. **Update Student Marks**: Modify marks for an existing student.  
3. **Delete Student Record**: Remove a student's record permanently.  
4. **View Class Performance**: Analyze overall class performance with key metrics.  
5. **Visualize Data**: Generate charts for better data insights.  
6. **Search Student**: Find a student by ID or name.  
7. **Filter Students by Grade**: Display all students with a specific grade.  
8. **Show Students Who Failed**: List students who failed in at least one subject.  
9. **Exit**: Exit the program.

**Key Features**:
- Input validation (e.g., student ID format).
- Dynamic interaction with the dataset.
- Easy navigation through a numbered menu.
This menu-driven approach ensures an intuitive and seamless experience for managing student records.

**Result:**
Here’s the content structured into 4 separate tables for each sector in the `README.md` format:

```markdown
# Class Performance Analysis

This program allows users to analyze the overall performance of students in multiple subjects. When the "Class Performance Analysis" option (Choice 4) is selected, the following key metrics are computed and displayed:

## 1. Average Marks Per Subject

| **Subject** | **Average Marks** |
|-------------|-------------------|
| Math        | 82.5              |
| English     | 84.75             |
| Science     | 81.75             |

## 2. Top Scorer

| **Metric**     | **Result**    |
|----------------|---------------|
| **Student ID** | ST-009        |
| **Name**       | Tamanna       |
| **Math**       | 90            |
| **English**    | 92            |
| **Science**    | 96            |

## 3. Lowest Scorer

| **Metric**     | **Result**    |
|----------------|---------------|
| **Student ID** | ST-001        |
| **Name**       | Alice         |
| **Math**       | 75            |
| **English**    | 70            |
| **Science**    | 67            |

## 4. Pass Percentage

| **Metric**     | **Result**    |
|----------------|---------------|
| **Pass Percentage** | 100%      |


These results offer valuable insights into class performance by:
- Identifying top performers.
- Highlighting students who may need additional support.
- Providing a comprehensive understanding of overall class performance.

This analysis helps educators focus on areas that need improvement, ensuring that all students are performing at their best.
```

This layout organizes the results into four distinct tables, each covering a different aspect of the performance analysis, making it more readable and easier to digest.
![download](https://github.com/user-attachments/assets/678691d0-c799-45de-a4a0-e4dc6451e69a)

### *Figure 1: Bar Chart - Average Marks Per Subject*
- *Title*: "Average Marks Per Subject"
- *X-Axis*: The subjects "Math," "English," and "Science."
- *Y-Axis*: Average marks, ranging from 0 to 90.
- *Observations*: 
  - The average marks for all three subjects are similar, hovering slightly above 80.
  - Math and English appear to have the same average, while Science is slightly lower but still very close.
![download](https://github.com/user-attachments/assets/fa42728b-7bca-44e1-b599-9145fb60b472)

### *Figure 2: Pie Chart - Grade Distribution*
- *Title*: "Grade Distribution"
- *Sectors*:
  - "A" occupies 75% of the chart.
  - "B" occupies 25% of the chart.
- *Observations*:
  - A majority of students (75%) received grade "A."
  - The remaining 25% received grade "B."

![download](https://github.com/user-attachments/assets/ee30ba76-6d6d-44df-b938-90562b4a2cb4)

### *Figure 3: Line Chart - Student Marks in Math*
- *Title*: "Student Marks in Math"
- *X-Axis*: The names of students: Alice, Bob, Charlie, and Tamanna.
- *Y-Axis*: Marks in Math, ranging from 76 to 90.
- *Observations*:
  - Bob scored the highest marks (90).
  - Charlie scored the lowest marks (76).
  - Alice and Tamanna scored in between, with Alice slightly higher than Tamanna.

### Conclusion

The **Student Marks and Grades Management System** provides a comprehensive solution for managing student records, calculating grades, and analyzing class performance. It allows for easy addition, updating, and deletion of student data while calculating grades based on predefined criteria. The system includes features for performance analysis, such as average marks per subject, identification of top and lowest scorers, and the calculation of pass percentages.

The visualizations offer a clear representation of class performance through bar charts, pie charts, and line graphs, helping educators and administrators to quickly assess the academic standing of students. The program also allows users to search, filter, and validate student data, ensuring efficient record management.

Overall, this system streamlines the management of student data and provides valuable insights into both individual and class-wide performance, making it a useful tool for educational settings.

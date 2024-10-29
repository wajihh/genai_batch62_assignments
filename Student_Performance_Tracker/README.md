
# Project: Student Performance Tracker

This project demonstrates a Student Performance Tracker built using Python.  It allows a teacher to input student scores, track performance across subjects, and calculate statistics such as averages and feedback on passing or failing.  The project utilizes Object-Oriented Programming (OOP), loops, conditionals, and data structures (lists and dictionaries).

## Project Structure

The project is built around a `Student` class which encapsulates the attributes and methods for a student object.

**1. Student Class:**

- **`__init__(self, name)`:**  Initializes a new `Student` object with a `name` and an empty dictionary `scores` to store subject scores.
- **`add_score(self, subject, score)`:**  Adds a subject and its corresponding score to the `scores` dictionary.  It validates that the score is between 0 and 100, printing an error message if it is not.
- **`get_average_score(self)`:** Calculates and returns the average score across all subjects. Includes a check to handle cases where no scores have been recorded, preventing a `ZeroDivisionError`. Returns 0 if there are no scores.
- **`get_feedback(self)`:** Returns a feedback string ("Passing" or "Failing") based on the average score. A passing score is defined as 70 or higher.
- **`get_subject_score(self, subject)`:** Retrieves score for a given subject. If score does not exist, a message "No score recorded for this subject." is returned.


**2. Main Function (`main`)**

- **Initialization:**  Creates an empty list `students` to store `Student` objects.
- **Main Loop:**  The core program loop that presents a menu to the user.
- **Menu Options:**
    - **1. Add Student:** Prompts for a student's name, creates a new `Student` object, and adds it to the `students` list.
    - **2. Add Score:** Prompts for a student's name, subject, and score. Then it finds the student in the list, validates the input, and adds the score using the `add_score` method.  Handles the case where no students have been added. It searches for the student by name.
    - **3. View Student Report:** Prompts for a student's name. If the student exists, it prints the subject scores, calculates and prints the average score, and gives overall feedback. If the student does not exist, it provides a "Student not found." message.  Handles the case where no scores have been recorded for the student. It searches for the student by name.
    - **4. Exit:**  Exits the program.
- **Error Handling:**  Provides feedback to the user for invalid choices and handles situations like no students added or student not found.

**3. Execution**
- **`if __name__ == "__main__":`** ensures that the `main()` function only executes when the script is run directly, not when imported as a module.


## How to Run the Code

1.  **Save:** Save the code as a Python file (e.g., `student_tracker.py`).
2.  **Run:** Execute the script from your terminal using `python student_tracker.py`.




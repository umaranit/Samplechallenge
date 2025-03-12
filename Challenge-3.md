# Coding Challenge: To-Do List Application

## Challenge Overview
Develop a simple to-do list application. This challenge involves handling user input, managing a list of tasks, saving and loading tasks from a file, and implementing comprehensive error handling.

## Tasks

### Task 1: Input Task Details
- Implement a function `get_task_details()` to accept user input for the task description and due date.
  - The function should validate that the task description is a non-empty string.
  - The function should validate that the due date is in the format `YYYY-MM-DD`. If not, display an error message and re-prompt the user.

### Task 2: Add Task to List
- Implement a function `add_task(task_list, task_description, due_date)` to add a new task to the task list.
  - Each task should be represented as a dictionary with keys `description` and `due_date`.

### Task 3: Display Tasks
- Implement a function `display_tasks(task_list)` to display all tasks in the list.
  - The output should be formatted in a clear and user-friendly format, showing the task description and due date.

### Task 4: Save Tasks to File
- Implement a function `save_tasks_to_file(task_list, filename)` to save the task list to a JSON file.
  - Handle potential `IOError` if the file cannot be written.
  - If an error occurs, display an appropriate error message and exit the program gracefully.

### Task 5: Load Tasks from File
- Implement a function `load_tasks_from_file(filename)` to load the task list from a JSON file.
  - Handle potential `FileNotFoundError` if the file does not exist.
  - Handle potential `JSONDecodeError` if the file is not a valid JSON.
  - If an error occurs, display an appropriate error message and return an empty list.

### Task 6: Error Handling
- Implement comprehensive error handling for all possible scenarios, including:
  - Invalid user input (empty task description, invalid due date format)
  - File not found (`tasks.json`)
  - Invalid JSON format
  - `IOError` when saving tasks
- Display informative error messages to the user.

### Task 7: Logging
- Implement basic logging to record any errors or exceptions that occur during the program execution.
  - Use the `logging` module in Python.
  - Log errors to a file named `todo_list.log`.

## Example Interaction:
Welcome to the To-Do List Application

Add Task
Display Tasks
Save Tasks
Load Tasks
Exit Choose an option: 1 Enter task description: Buy groceries Enter due date (YYYY-MM-DD): 2025-02-20 Task added successfully. Choose an option: 2 Tasks:
Buy groceries (Due: 2025-02-20) Choose an option: 5 Goodbye!


## Example JSON File (`tasks.json`):
```json
[
  {
    "description": "Buy groceries",
    "due_date": "2025-02-20"
  },
  {
    "description": "Complete coding challenge",
    "due_date": "2025-02-21"
  }
]

Submission Guidelines:
Ensure your code is well-documented and follows best practices.
Use GitHub Copilot to assist in the development process.
Include comprehensive error handling and logging.
Write Unit Tests
Provide clear instructions on how to run the application.
Good luck with your coding challenge! ```
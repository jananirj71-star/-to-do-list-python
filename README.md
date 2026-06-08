🎯 Objective
The objective of this project is to develop a simple To-Do List Application using Python that helps users manage their daily tasks efficiently by adding, viewing, updating, and deleting tasks.

✨ Key Features

Add new tasks
View all tasks
Update existing tasks
Delete tasks
Simple command-line interface

💻 Code

tasks = []

while True:
    print("\n===== TO-DO LIST =====")
    print("1. Add Task")
    print("2. View Tasks")
    print("3. Update Task")
    print("4. Delete Task")
    print("5. Exit")

   choice = input("Enter your choice: ")
    if choice == "1":
        task = input("Enter task: ")
        tasks.append(task)
        print("Task added successfully!")
    elif choice == "2":
        if not tasks:
            print("No tasks available.")
        else:
            print("\nTasks:")
            for i, task in enumerate(tasks, start=1):
                print(f"{i}. {task}")
    elif choice == "3":
        for i, task in enumerate(tasks, start=1):
            print(f"{i}. {task}")
        num = int(input("Enter task number to update: "))
        new_task = input("Enter new task: ")
        tasks[num-1]= new_task
        print("Task updated successfully!")
    elif choice == "4":
        for i, task in enumerate(tasks, start=1):
            print(f"{i}. {task}")
       num = int(input("Enter task number to delete: "))
        tasks.pop(num - 1)
        print("Task deleted successfully!")
    elif choice == "5":
        print("Thank you!")
        break
    else:
        print("Invalid choice. Try again.")

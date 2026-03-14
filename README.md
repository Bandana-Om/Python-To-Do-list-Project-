tasks = []

while True:
    print("\nTo-Do List Menu")
    print("1. Add Task")
    print("2. View Tasks")
    print("3. Remove Task")
    print("4. Exit")

    choice = input("Enter your choice: ")

    if choice == "1":
        task = input("Enter a new task: ")
        tasks.append(task)
        print("Task added successfully!")

    elif choice == "2":
        if tasks:
            print("\nYour Tasks:")
            for i, task in enumerate(tasks, start=1):
                print(i, "-", task)
        else:
            print("No tasks in the list.")

    elif choice == "3":
        task = input("Enter task to remove: ")
        if task in tasks:
            tasks.remove(task)
            print("Task removed.")
        else:
            print("Task not found.")

    elif choice == "4":
        print("Exiting program.")
        break

    else:
        print("Invalid choice. Try again.")

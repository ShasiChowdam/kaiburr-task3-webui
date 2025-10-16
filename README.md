# Kaiburr Task 3 – Web UI Frontend

This project implements a responsive and interactive web interface for the backend developed in **Task 1 (Java + Spring Boot)** and **Task 2 (Kubernetes)**.  
The application allows users to **create, view, search, delete, and run shell-command tasks**, displaying the corresponding execution output in real time.

---

## 🧩 Tech Stack

- **React 19** (with TypeScript)
- **Ant Design 5** (for responsive UI components)
- **Axios** (for API integration)
- **Spring Boot Backend** (connected via REST APIs at `http://localhost:8080/api`)
- **Node.js 18+**

---

## ⚙️ Setup Instructions

### 1️.Clone the Repository

git clone https://github.com/ShasiChowdam/kaiburr-task3-webui.git
cd kaiburr-task3-webui/task-ui

2.Install Dependencies
npm install

3️.Start the Backend (Spring Boot)

In a separate terminal, navigate to your backend project folder (Task 2) and run:

mvn spring-boot:run

This starts the backend server on port 8080.

4️.Start the Frontend
npm start


The React app runs at http://localhost:3000

Ensure the backend server is running before opening the UI.

Features

Create Task – Add new tasks with name, owner, and command.

View All Tasks – Display all existing tasks fetched from the backend.

Search Tasks – Find tasks by partial name match.

Delete Tasks – Remove tasks from MongoDB through the API.

Run Commands – Execute shell commands (locally or in Kubernetes pods).

View Command Output – Display the execution output in a modal window.


Outputs and Screenshots

All screenshots showing the UI and API interactions are stored in the screenshots/ folder:

CreateTask.png – Creating a new task

TaskTable.png – Viewing all tasks

SearchTask.png – Searching for a task

RunCommand.png – Running a command and displaying output


Building for Production
npm run build


This creates an optimized production build in the build/ directory.

To serve the built files locally:

npm install -g serve
serve -s build

# Kaiburr Task 3 – Web UI Frontend

This project implements a responsive web interface for the backend developed in **Task 1 (Java + Spring Boot)** and **Task 2 (Kubernetes)**.  
It enables users to **create, view, search, delete, and run shell-command tasks**, displaying execution output in real time.

---

## 🧩 Tech Stack
- **React 19** (with TypeScript)  
- **Ant Design 5** for UI components  
- **Axios** for API requests  
- **Spring Boot Backend** running on `http://localhost:8080/api`  
- **Node.js 18 or higher**

---

## ⚙️ Setup Instructions

### 1️.Clone the Repository
```bash
git clone https://github.com/ShasiChowdam/kaiburr-task3-webui.git
cd kaiburr-task3-webui/task-ui
2️.Install Dependencies
bash
Copy code
npm install
3️.Start the Backend (Spring Boot)
In a separate terminal, run from your backend directory (Task 2 project):

bash
Copy code
mvn spring-boot:run
This starts the backend on port 8080.

4.Start the Frontend
bash
Copy code
npm start
The React app runs at http://localhost:3000
Make sure the backend is already running before opening the UI.

Features
Create Task – Add a new task by providing name, owner, and command.

View All Tasks – Displays existing tasks from the backend.

Search Tasks – Find tasks by name.

Delete Task – Removes a task from MongoDB via backend API.

Run Command – Executes the task command in a Kubernetes pod or locally and shows output inline.

View Execution Output – Displays the latest command output in a modal dialog.

Project Structure
pgsql
Copy code
task-ui/
 ├── public/
 ├── src/
 │    ├── components/
 │    │    ├── TaskForm.tsx
 │    │    ├── TaskTable.tsx
 │    │    └── OutputModal.tsx
 │    ├── App.tsx
 │    ├── index.tsx
 │    └── styles/
 ├── package.json
 ├── tsconfig.json
 ├── README.md
 └── screenshots/
API Endpoints (Backend)
Method	Endpoint	Description
GET	/api/tasks	Fetch all tasks
GET	/api/tasks/find?name=	Search tasks by name
PUT	/api/tasks	Create or update a task
DELETE	/api/tasks/{id}	Delete a task
PUT	/api/tasks/{id}/execution	Execute task command

Outputs and Screenshots
All screenshots demonstrating the UI and API interactions are available inside the screenshots/ folder:

CreateTask.png – Creating a new task

TaskTable.png – Viewing all tasks

SearchTask.png – Searching for a task

RunCommand.png – Executing a command and showing output

How to Build for Production
bash
Copy code
npm run build
This creates an optimized production bundle in the build/ directory.

To serve the built files locally:

bash
Copy code
npm install -g serve
serve -s build

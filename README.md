Kaiburr Task 3 – Web UI Frontend
This project implements a responsive and interactive web interface for the backend developed in Task 1 (Java + Spring Boot) and Task 2 (Kubernetes). The application allows users to create, view, search, delete, and run shell-command tasks, and displays the corresponding execution output in real time.
Tech Stack
- React 19 (with TypeScript)
- Ant Design 5 (for responsive UI components)
- Axios (for API integration)
- Spring Boot Backend (connected via REST APIs on http://localhost:8080/api)
- Node.js 18 or higher
Setup Instructions
1.Clone the Repository
•	git clone https://github.com/ShasiChowdam/kaiburr-task3-webui.git
cd kaiburr-task3-webui/task-ui
2.Install Dependencies
•	npm install
3.Start the Backend (Spring Boot)
•	In a separate terminal, navigate to your backend project folder (Task 2 directory) and run:
mvn spring-boot:run
This will start the backend server on port 8080.
4.Start the Frontend
•	npm start
The React application runs at http://localhost:3000. Ensure that your backend server is running before starting the UI.
Features
- Create Task: Add new tasks with name, owner, and command.
- View All Tasks: Display all existing tasks fetched from the backend.
- Search Tasks: Find tasks based on a keyword in their name.
- Delete Tasks: Remove a specific task from MongoDB through the API.
- Run Commands: Execute shell commands locally or in a Kubernetes pod.
- View Command Output: Display the command output dynamically in a modal.
Project Structure
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
Backend API Endpoints
Method	Endpoint	Description
GET	/api/tasks	Retrieve all tasks
GET	/api/tasks/find?name=	Search tasks by name
PUT	/api/tasks	Create or update a task
DELETE	/api/tasks/{id}	Delete a specific task
PUT	/api/tasks/{id}/execution	Execute a task command
Outputs and Screenshots
All screenshots showing the UI and API interactions are located inside the screenshots/ folder:
- CreateTask.png – Demonstrates creating a new task
- TaskTable.png – Displays the list of all tasks
- SearchTask.png – Shows the search functionality
- RunCommand.png – Displays command execution and output modal
Building for Production
npm run build
This command generates an optimized production build in the build/ directory.

To preview the production build locally:
npm install -g serve
serve -s build
Accessibility & Usability
- Clean, modern UI with Ant Design components
- Responsive layout suitable for all screen sizes
- Intuitive form validation and error handling
- Keyboard and screen reader accessibility
- Modal-based command output display for improved readability

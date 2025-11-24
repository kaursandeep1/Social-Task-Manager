# 🔐 Social Task Manager

A full-stack web application that allows users to manage their tasks with Facebook authentication, file uploads, and a complete RESTful API.

## 🎯 Features

### 🔐 Authentication & Security
- Facebook OAuth 2.0 authentication with Passport.js
- Secure session management
- User isolation and data protection
- Input validation and sanitization

### 📋 Task Management
- Create, read, update, and delete tasks
- File uploads attached to tasks (stored as base64 in MongoDB)
- Due date tracking and task organization
- Clean, responsive user interface

### 🔗 RESTful API
- Complete CRUD operations via REST endpoints
- JSON-based API for external integrations
- Proper HTTP status codes and error handling

## 🛠️ Technology Stack

**Backend:** Node.js, Express.js, MongoDB
**Authentication:** Passport.js, Facebook OAuth 2.0
**Frontend:** EJS templates, HTML5, CSS3, JavaScript
**File Handling:** Express-formidable
**Deployment:** Render, MongoDB Atlas

## 🚀 Quick Start

```bash
# Clone the repository
git clone https://github.com/jyoti786J/Social-Task-Manager.git
cd Social-Task-Manager

# Install dependencies
npm install

# Configure environment variables
# Create .env file with:
MONGODB_URI=your_mongodb_connection_string
FACEBOOK_APP_ID=your_facebook_app_id
FACEBOOK_APP_SECRET=your_facebook_app_secret
SESSION_SECRET=your_session_secret

# Run the application
npm start

# Access at: http://localhost:8099

Social-Task-Manager/
├── server.js              # Main application file
├── package.json           # Dependencies and scripts
├── views/                 # EJS templates
│   ├── create.ejs        # Task creation form
│   ├── list.ejs          # Tasks listing page
│   ├── edit.ejs          # Task editing form
│   ├── details.ejs       # Task details view
│   ├── info.ejs          # Information/status messages
│   └── login.ejs         # Login page
└── (other configuration files)

🔧 API Usage Examples

Create a Task
curl -X POST http://localhost:8099/api/record \
  -H "Content-Type: application/json" \
  -d '{"task": "Buy groceries", "date": "2024-12-01"}'

Get All Tasks
curl http://localhost:8099/api/record

Update Tasks
curl -X PUT http://localhost:8099/api/record \
  -H "Content-Type: application/json" \
  -d '{"task": "Updated task", "date": "2024-12-05"}'

Delete a Task
curl -X DELETE http://localhost:8099/api/record/TaskNameToDelete

🔒 Security Features
- Facebook OAuth 2.0 - Secure third-party authentication
- Session-based authentication - Server-side session management
- User isolation - Users can only access their own tasks
- Input validation - Form data validation and sanitization

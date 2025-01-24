# User Management API

## Setup
1. Clone the repository
2. Run `npm install`
3. Start the server: `node index.js`
4. API will be available at `http://localhost:3000`

## API Endpoints

### Get All Users
- **URL**: `https://bug-free-invention-q75g4rq97752x7v6-3000.app.github.dev/api/users`
- **Method**: `GET`
- **Success Response**: 
  - Code: 200
  - Content: `[{ id: 1, name: "John", email: "john@example.com" }, { id: 2, name: "Jane", email: "jane@example.com" }]`
  
### Get User by ID
- **URL**: `/api/users/:id`
- **Method**: `GET`
- **URL Params**: `id=[integer]`
- **Success Response**: 
  - Code: 200
  - Content: `{ id: 1, name: "John", email: "john@example.com" }`
- **Error Response**:
  - Code: 404
  - Content: `{ message: "User  not found" }`

### Create a New User
- **URL**: https://bug-free-invention-q75g4rq97752x7v6-3000.app.github.dev/api/users`
- **Method**: `POST`
- **Request Body**: `{ "name": "New User", "email": "newuser@example.com" }`
- **Success Response**: 
  - Code: 201
  - Content: `{ id: 3, name: "New User", email: "newuser@example.com" }`
- **Error Response**:
  - Code: 400
  - Content: `{ message: "Name and email are required" }`

### Update an Existing User
- **URL**: `/api/users/:id`
- **Method**: `PUT`
- **URL Params**: `id=[integer]`
- **Request Body**: `{ "name": "Updated User", "email": "updateduser@example.com" }`
- **Success Response**: 
  - Code: 200
  - Content: `{ id: 1, name: "Updated User", email: "updateduser@example.com" }`
- **Error Response**:
  - Code: 404
  - Content: `{ message: "User  not found" }`
  - Code: 400
  - Content: `{ message: "Name
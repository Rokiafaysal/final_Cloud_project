# Menu Management NodeJS Backend Project

## Project Description
This project is a Node.js backend for managing menus in a restaurant application. It allows for the management of menu items, categories, and orders, providing a comprehensive solution for restaurant operations.

## Features
- Add, update, and delete menu items
- Organize menu items into categories
- Manage orders and track order history
- User authentication and authorization
- RESTful API for easy integration with front-end applications

## Setup Instructions
1. Clone the repository:
   ```bash
   git clone https://github.com/Rokiafaysal/MenuMangement-NodeJS-Backend-Project.git
   cd MenuMangement-NodeJS-Backend-Project
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Create a `.env` file in the root directory and add the necessary environment variables:
   ```env
   DB_URI=mongodb://<dbuser>:<dbpassword>@localhost:27017/mydatabase
   JWT_SECRET=<your_jwt_secret>
   PORT=3000
   ```
4. Start the server:
   ```bash
   npm start
   ```

## Technology Stack
- Node.js
- Express.js
- MongoDB
- Mongoose
- JWT for authentication
- dotenv for environment variable management

## Project Structure
```
MenuMangement-NodeJS-Backend-Project/
├── src/
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   ├── middleware/
│   └── config/
├── .env
├── package.json
└── server.js
```

## API Endpoints Overview
| Method | Endpoint                | Description                       |
|--------|-------------------------|-----------------------------------|
| GET    | /api/menu               | Get all menu items               |
| POST   | /api/menu               | Create a new menu item           |
| PUT    | /api/menu/:id          | Update a menu item               |
| DELETE | /api/menu/:id          | Delete a menu item               |
| GET    | /api/categories         | Get all menu categories           |
| POST   | /api/categories         | Create a new menu category        |

## Usage Examples
### Get All Menu Items
```bash
curl -X GET http://localhost:3000/api/menu
```

### Create a New Menu Item
```bash
curl -X POST http://localhost:3000/api/menu -H "Content-Type: application/json" -d '{"name":"Burger", "price":5.99}'
```

### Update a Menu Item
```bash
curl -X PUT http://localhost:3000/api/menu/1 -H "Content-Type: application/json" -d '{"price":6.99}'
```

### Delete a Menu Item
```bash
curl -X DELETE http://localhost:3000/api/menu/1
```
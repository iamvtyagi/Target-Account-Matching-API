# Target Account Matching

A web application for managing and tracking target company accounts with match scoring functionality. This application helps users identify and manage potential target accounts based on match scores.

![Target Account Matching Screenshot](https://via.placeholder.com/800x450.png?text=Target+Account+Matching)

## Features

- **User Authentication**: Secure login system with JWT token-based authentication
- **Account Management**: View, create, and manage company accounts
- **Match Scoring**: Each company account has a match score indicating its potential as a target
- **Status Tracking**: Mark accounts as "Target" or "Not Target" to track your sales pipeline
- **Responsive UI**: Modern, responsive interface built with React and Tailwind CSS

## Tech Stack

### Frontend
- React 18
- TypeScript
- React Router for navigation
- Tailwind CSS for styling
- Lucide React for icons
- Axios for API requests

### Backend
- Node.js
- Express.js
- MongoDB with Mongoose ODM
- JWT for authentication
- bcryptjs for password hashing

## Prerequisites

Before you begin, ensure you have the following installed:
- Node.js (v18.0.0 or higher)
- npm or yarn
- MongoDB (local instance or MongoDB Atlas account)

## Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd target-account-matching
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create a `.env` file in the root directory with the following variables:
   ```
   MONGODB_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret
   PORT=5002
   ```

4. Seed the database with demo data:
   ```bash
   node backend/scripts/seedDB.js
   ```

## Running the Application

### Development Mode

Run both frontend and backend concurrently:
```bash
npm run dev
```

Or run them separately:
```bash
# Frontend only
npm run dev:frontend

# Backend only
npm run dev:backend
```

### Production Build

Build the frontend:
```bash
npm run build:frontend
```

## API Endpoints

### Authentication
- `POST /api/login` - Authenticate user and get token
- `POST /api/register` - Register a new user (for development purposes)

### Accounts
- `GET /api/accounts` - Get all accounts
- `GET /api/accounts/:id` - Get account by ID
- `POST /api/accounts` - Create a new account
- `POST /api/accounts/:id/status` - Update account status

## Demo Credentials

Use these credentials to log in to the demo application:
- Username: `user1`
- Password: `pass123`

## Project Structure

```
project/
├── backend/
│   ├── controllers/       # Route controllers
│   ├── middleware/        # Express middleware
│   ├── models/            # Mongoose models
│   ├── routes/            # Express routes
│   ├── scripts/           # Database scripts
│   └── server.js          # Express app
├── src/
│   ├── components/        # React components
│   ├── context/           # React context providers
│   ├── services/          # API services
│   ├── App.tsx            # Main App component
│   └── main.tsx           # Entry point
├── .env                   # Environment variables
├── package.json           # Dependencies and scripts
└── vite.config.ts         # Vite configuration
```

## Account Model

Each account in the system has the following properties:
- `companyName`: Name of the company
- `matchScore`: A score from 0-100 indicating how well the company matches your target criteria
- `status`: Either "Target" or "Not Target"
- `createdAt`: Timestamp when the account was created
- `updatedAt`: Timestamp when the account was last updated

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- [React](https://reactjs.org/)
- [Express](https://expressjs.com/)
- [MongoDB](https://www.mongodb.com/)
- [Tailwind CSS](https://tailwindcss.com/)
- [Lucide Icons](https://lucide.dev/)

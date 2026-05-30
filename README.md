# CreatorHub

A backend-focused YouTube-inspired video streaming platform built with Node.js, Express.js, and MongoDB. Features secure authentication, comprehensive video management APIs, social features like likes and comments, subscriptions, and a scalable REST architecture.

## 🎯 Features

- **Secure Authentication**: User registration and login with JWT tokens
- **Video Management**: Upload, delete, and manage video content
- **Social Features**: 
  - Like/Unlike videos
  - Comment on videos
  - Subscribe/Unsubscribe to channels
- **User Profiles**: Create and manage creator profiles
- **Scalable Architecture**: Built with REST API principles for easy scaling
- **MongoDB Integration**: Persistent data storage with MongoDB

## 🛠️ Tech Stack

- **Runtime**: Node.js
- **Framework**: Express.js
- **Database**: MongoDB
- **Authentication**: JWT (JSON Web Tokens)
- **Language**: JavaScript

## 📋 Prerequisites

Before you begin, ensure you have the following installed:

- Node.js (v14 or higher)
- npm or yarn
- MongoDB (local or cloud instance)

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/SumitKumar-2004/CreatorHub.git
cd CreatorHub
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Environment Configuration

Create a `.env` file in the root directory and add your configuration:

```env
PORT=5000
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
NODE_ENV=development
```

### 4. Start the Server

```bash
npm start
```

The server will start on `http://localhost:5000`

## 📚 API Endpoints

### Authentication
- `POST /auth/register` - Register a new user
- `POST /auth/login` - Login user
- `POST /auth/logout` - Logout user

### Videos
- `GET /videos` - Get all videos
- `GET /videos/:id` - Get video by ID
- `POST /videos` - Upload a new video
- `PUT /videos/:id` - Update video details
- `DELETE /videos/:id` - Delete a video

### Likes
- `POST /videos/:id/like` - Like a video
- `DELETE /videos/:id/like` - Unlike a video

### Comments
- `GET /videos/:id/comments` - Get video comments
- `POST /videos/:id/comments` - Add a comment
- `DELETE /comments/:id` - Delete a comment

### Subscriptions
- `POST /channels/:id/subscribe` - Subscribe to a channel
- `DELETE /channels/:id/subscribe` - Unsubscribe from a channel
- `GET /channels/:id/subscribers` - Get channel subscribers

### User Profiles
- `GET /users/:id` - Get user profile
- `PUT /users/:id` - Update user profile
- `GET /users/:id/videos` - Get user's videos

## 📦 Project Structure

```
CreatorHub/
├── src/
│   ├── models/           # MongoDB schemas
│   ├── routes/           # API routes
│   ├── controllers/       # Route handlers
│   ├── middleware/        # Custom middleware
│   ├── config/           # Configuration files
│   └── utils/            # Utility functions
├── tests/                # Test files
├── .env                  # Environment variables
├── .gitignore            # Git ignore rules
├── app.js                # Express app setup
├── server.js             # Server entry point
├── package.json          # Dependencies
└── README.md             # This file
```

## 🔐 Authentication

The API uses JWT (JSON Web Tokens) for authentication. Include the token in the Authorization header:

```
Authorization: Bearer <your_jwt_token>
```

## 💾 Database Schema

### User
- username (String, unique)
- email (String, unique)
- password (String, hashed)
- profile information
- timestamps

### Video
- title (String)
- description (String)
- url (String)
- uploadedBy (Reference to User)
- likes count
- comments
- timestamps

### Comment
- content (String)
- createdBy (Reference to User)
- video (Reference to Video)
- timestamps

## 🧪 Testing

```bash
npm test
```

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 👨‍💻 Author

- **Sumit Kumar** - [@SumitKumar-2004](https://github.com/SumitKumar-2004)

## 🤝 Support

If you encounter any issues or have questions, please:

1. Check existing [issues](https://github.com/SumitKumar-2004/CreatorHub/issues)
2. Create a new issue with detailed information
3. Feel free to reach out through GitHub discussions

## 📞 Contact

For more information or inquiries, please open an issue on the repository.

---

**Happy Coding!** 🚀

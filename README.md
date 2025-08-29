# 🤖 IMBOT – Smart AI Assistant

[![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)](https://reactjs.org/)
[![Node.js](https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white)](https://nodejs.org/)
[![MongoDB](https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white)](https://mongodb.com/)
[![Express.js](https://img.shields.io/badge/Express.js-404D59?style=for-the-badge)](https://expressjs.com/)
[![Socket.io](https://img.shields.io/badge/Socket.io-black?style=for-the-badge&logo=socket.io&badgeColor=010101)](https://socket.io/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)

**IMBOT** is a **smart AI-powered chatbot builder** that empowers users to **train custom chatbots** using their own data (Text/PDF files) and interact with them in real-time. Built with the **MERN stack** and powered by **Google Gen AI**, IMBOT delivers a seamless, scalable, and intelligent chatbot creation experience.

## 🌟 Live Demo
🔗 **[Try IMBOT Now](https://your-imbot-demo.com)**

## 📸 Screenshots

<div align="center">
  <img src="./screenshots/dashboard.png" alt="IMBOT Dashboard" width="45%">
  <img src="./screenshots/chat-interface.png" alt="Chat Interface" width="45%">
</div>
<div align="center">
  <img src="./screenshots/bot-training.png" alt="Bot Training" width="45%">
  <img src="./screenshots/bot-sharing.png" alt="Bot Sharing" width="45%">
</div>

---

## 🚀 Features

### 🧠 **AI-Powered Intelligence**
- 📂 **Custom Data Training** – Upload Text/PDF files to train personalized chatbots
- 🤖 **Smart Context Understanding** – AI comprehends and responds based on your data
- 💡 **Intelligent Responses** – Generate accurate, context-aware answers
- 📚 **Multi-Document Processing** – Handle multiple files for comprehensive training

### 💬 **Real-Time Communication**
- ⚡ **Instant Messaging** – Real-time chat with Socket.IO integration
- 🔄 **Live Updates** – See responses as they're generated
- 💾 **Chat History** – Persistent conversation storage
- 📱 **Cross-Platform** – Works seamlessly across all devices

### 🔗 **Sharing & Collaboration**
- 🌐 **Bot Sharing** – Share custom chatbots via unique links
- 👥 **Multi-User Support** – Multiple users can interact with shared bots
- 🔒 **Access Control** – Manage bot visibility and permissions
- 📊 **Usage Analytics** – Track bot performance and interactions

### 🎨 **Modern User Experience**
- 🖼️ **Intuitive Interface** – Clean, modern design with Tailwind CSS
- 📱 **Responsive Design** – Perfect experience on desktop, tablet, and mobile
- 🌙 **Dark/Light Mode** – Toggle between themes for comfort
- ⚡ **Fast Performance** – Optimized for speed and efficiency

---

## 🛠️ Tech Stack

### **Frontend Technologies**
- **React.js** (18.x) - Modern component-based UI framework
- **Tailwind CSS** - Utility-first CSS framework for rapid styling
- **Socket.IO Client** - Real-time bidirectional event-based communication
- **Axios** - Promise-based HTTP client for API requests
- **React Router** - Declarative routing for React applications
- **React Icons** - Popular icon library for React
- **React Dropzone** - File upload component with drag-and-drop

### **Backend Technologies**
- **Node.js** (18.x) - JavaScript runtime environment
- **Express.js** - Fast, unopinionated web framework
- **Socket.IO** - Real-time communication library
- **MongoDB** - NoSQL document database
- **Mongoose** - Elegant MongoDB object modeling
- **Multer** - Middleware for handling file uploads
- **PDF-Parse** - Extract text from PDF files

### **AI & External Services**
- **Google Gen AI API** - Advanced generative AI for intelligent responses
- **Natural Language Processing** - Text processing and understanding
- **Vector Embeddings** - Semantic search and context matching

### **Development & Deployment**
- **Nodemon** - Development server with auto-restart
- **Concurrently** - Run multiple npm scripts simultaneously
- **Cors** - Cross-origin resource sharing middleware
- **Helmet** - Security middleware for Express
- **Morgan** - HTTP request logger middleware

---

## 📂 Detailed Project Structure

```bash
IMBOT/
├── client/                          # React frontend application
│   ├── public/
│   │   ├── index.html              # Main HTML template
│   │   ├── favicon.ico             # App favicon
│   │   └── manifest.json           # PWA manifest
│   ├── src/
│   │   ├── components/             # Reusable UI components
│   │   │   ├── common/             # Common components
│   │   │   │   ├── Header.jsx
│   │   │   │   ├── Footer.jsx
│   │   │   │   ├── LoadingSpinner.jsx
│   │   │   │   └── Modal.jsx
│   │   │   ├── bot/                # Bot-related components
│   │   │   │   ├── BotBuilder.jsx
│   │   │   │   ├── BotCard.jsx
│   │   │   │   ├── BotSettings.jsx
│   │   │   │   └── BotPreview.jsx
│   │   │   ├── chat/               # Chat interface components
│   │   │   │   ├── ChatInterface.jsx
│   │   │   │   ├── MessageBubble.jsx
│   │   │   │   ├── ChatInput.jsx
│   │   │   │   └── TypingIndicator.jsx
│   │   │   └── upload/             # File upload components
│   │   │       ├── FileUploader.jsx
│   │   │       ├── FilePreview.jsx
│   │   │       └── UploadProgress.jsx
│   │   ├── pages/                  # Main page components
│   │   │   ├── Home.jsx           # Landing page
│   │   │   ├── Dashboard.jsx      # User dashboard
│   │   │   ├── BotCreator.jsx     # Bot creation page
│   │   │   ├── ChatPage.jsx       # Individual chat page
│   │   │   ├── SharedBot.jsx      # Shared bot interface
│   │   │   ├── Profile.jsx        # User profile
│   │   │   └── NotFound.jsx       # 404 page
│   │   ├── hooks/                  # Custom React hooks
│   │   │   ├── useSocket.js       # Socket.IO connection hook
│   │   │   ├── useChat.js         # Chat functionality hook
│   │   │   ├── useBots.js         # Bot management hook
│   │   │   ├── useAuth.js         # Authentication hook
│   │   │   └── useFileUpload.js   # File upload hook
│   │   ├── services/              # API service functions
│   │   │   ├── api.js             # Main API configuration
│   │   │   ├── botService.js      # Bot-related API calls
│   │   │   ├── chatService.js     # Chat API calls
│   │   │   ├── authService.js     # Authentication API calls
│   │   │   └── uploadService.js   # File upload API calls
│   │   ├── context/               # React Context providers
│   │   │   ├── AuthContext.jsx    # Authentication context
│   │   │   ├── BotContext.jsx     # Bot management context
│   │   │   └── ThemeContext.jsx   # Theme management context
│   │   ├── utils/                 # Utility functions
│   │   │   ├── helpers.js         # General helper functions
│   │   │   ├── constants.js       # App constants
│   │   │   ├── formatters.js      # Data formatting functions
│   │   │   └── validators.js      # Input validation functions
│   │   ├── styles/                # Global styles
│   │   │   ├── globals.css        # Global CSS styles
│   │   │   └── components.css     # Component-specific styles
│   │   ├── assets/                # Static assets
│   │   │   ├── images/           # Image files
│   │   │   └── icons/            # Icon files
│   │   ├── App.js                 # Main App component
│   │   └── index.js               # React entry point
│   ├── package.json               # Client dependencies
│   └── tailwind.config.js         # Tailwind CSS configuration
├── server/                         # Express backend application
│   ├── controllers/               # Route controllers
│   │   ├── authController.js      # Authentication logic
│   │   ├── botController.js       # Bot management logic
│   │   ├── chatController.js      # Chat functionality logic
│   │   ├── uploadController.js    # File upload logic
│   │   └── userController.js      # User management logic
│   ├── models/                    # MongoDB schemas
│   │   ├── User.js               # User model
│   │   ├── Bot.js                # Bot model
│   │   ├── Chat.js               # Chat model
│   │   ├── Message.js            # Message model
│   │   └── Document.js           # Document model
│   ├── routes/                    # API route definitions
│   │   ├── auth.js               # Authentication routes
│   │   ├── bots.js               # Bot management routes
│   │   ├── chats.js              # Chat routes
│   │   ├── upload.js             # File upload routes
│   │   └── users.js              # User routes
│   ├── middleware/                # Express middleware
│   │   ├── auth.js               # Authentication middleware
│   │   ├── validation.js         # Input validation middleware
│   │   ├── upload.js             # File upload middleware
│   │   ├── rateLimiter.js        # Rate limiting middleware
│   │   └── errorHandler.js       # Error handling middleware
│   ├── services/                  # Business logic services
│   │   ├── aiService.js          # Google Gen AI integration
│   │   ├── documentProcessor.js  # PDF/Text processing
│   │   ├── botTrainer.js         # Bot training logic
│   │   ├── chatService.js        # Chat management
│   │   └── emailService.js       # Email notifications
│   ├── utils/                     # Utility functions
│   │   ├── database.js           # Database connection
│   │   ├── helpers.js            # General helpers
│   │   ├── constants.js          # Server constants
│   │   ├── logger.js             # Logging utility
│   │   └── security.js           # Security utilities
│   ├── config/                    # Configuration files
│   │   ├── database.js           # Database configuration
│   │   ├── cloudinary.js         # File storage config
│   │   └── socket.js             # Socket.IO configuration
│   ├── uploads/                   # Temporary file storage
│   ├── logs/                      # Application logs
│   ├── server.js                  # Main server file
│   └── package.json               # Server dependencies
├── shared/                         # Shared utilities (optional)
│   ├── types/                     # TypeScript type definitions
│   └── constants/                 # Shared constants
├── docs/                          # Project documentation
│   ├── api.md                    # API documentation
│   ├── deployment.md             # Deployment guide
│   └── contributing.md           # Contribution guidelines
├── tests/                         # Test files
│   ├── client/                   # Frontend tests
│   └── server/                   # Backend tests
├── screenshots/                   # Project screenshots
├── .env.example                  # Environment variables template
├── .gitignore                    # Git ignore file
├── package.json                  # Root package.json for scripts
└── README.md                     # Project documentation
```

---

## ⚙️ Installation & Setup

### Prerequisites
- **Node.js** (v18.0.0 or higher)
- **MongoDB** (v5.0 or higher) or MongoDB Atlas account
- **npm** or **yarn** package manager
- **Google Gen AI API Key** ([Get it here](https://makersuite.google.com/app/apikey))

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/imbot.git
cd imbot
```

### 2. Install Dependencies
```bash
# Install root dependencies
npm install

# Install client dependencies
cd client
npm install

# Install server dependencies
cd ../server
npm install
```

### 3. Environment Configuration

#### Server `.env`
```env
# Server Configuration
PORT=5000
NODE_ENV=development

# Database Configuration
MONGODB_URI=mongodb://localhost:27017/imbot
# Or for MongoDB Atlas:
# MONGODB_URI=mongodb+srv://username:password@cluster.mongodb.net/imbot

# Google Gen AI Configuration
GOOGLE_AI_API_KEY=your_google_gen_ai_api_key_here

# JWT Configuration
JWT_SECRET=your_super_secret_jwt_key_here
JWT_EXPIRE=7d

# CORS Configuration
CLIENT_URL=http://localhost:3000
ALLOWED_ORIGINS=http://localhost:3000,https://yourdomain.com

# File Upload Configuration
MAX_FILE_SIZE=10485760  # 10MB in bytes
UPLOAD_PATH=./uploads
ALLOWED_FILE_TYPES=.pdf,.txt,.doc,.docx

# Email Configuration (optional)
SMTP_HOST=your_smtp_host
SMTP_PORT=587
SMTP_USER=your_email@example.com
SMTP_PASS=your_email_password

# Rate Limiting
RATE_LIMIT_WINDOW=15  # minutes
RATE_LIMIT_MAX_REQUESTS=100

# Security
BCRYPT_SALT_ROUNDS=12
HELMET_ENABLED=true
```

#### Client `.env`
```env
# API Configuration
REACT_APP_API_BASE_URL=http://localhost:5000/api
REACT_APP_SOCKET_URL=http://localhost:5000

# App Configuration
REACT_APP_APP_NAME=IMBOT
REACT_APP_MAX_FILE_SIZE=10485760
REACT_APP_SUPPORTED_FILE_TYPES=.pdf,.txt,.doc,.docx

# Feature Flags
REACT_APP_ENABLE_DARK_MODE=true
REACT_APP_ENABLE_ANALYTICS=false
REACT_APP_ENABLE_PWA=true
```

### 4. Database Setup
```bash
# For local MongoDB
# Start MongoDB service
# macOS (Homebrew):
brew services start mongodb/brew/mongodb-community

# Windows:
net start MongoDB

# Linux (systemd):
sudo systemctl start mongod

# Create initial database (optional)
mongosh
use imbot
db.createCollection("users")
```

### 5. Start the Development Server
```bash
# Option 1: Start both client and server simultaneously (from root)
npm run dev

# Option 2: Start them separately
# Terminal 1 - Server
cd server
npm run dev

# Terminal 2 - Client
cd client
npm start
```

### 6. Access the Application
- **Frontend**: http://localhost:3000
- **Backend API**: http://localhost:5000
- **API Documentation**: http://localhost:5000/api/docs (if implemented)

---

## 🔧 API Documentation

### Authentication Endpoints
```http
POST   /api/auth/register         # Register new user
POST   /api/auth/login            # User login
POST   /api/auth/logout           # User logout
GET    /api/auth/profile          # Get user profile
PUT    /api/auth/profile          # Update user profile
POST   /api/auth/forgot-password  # Request password reset
POST   /api/auth/reset-password   # Reset password
```

### Bot Management Endpoints
```http
GET    /api/bots                  # Get user's bots
POST   /api/bots                  # Create new bot
GET    /api/bots/:id              # Get specific bot
PUT    /api/bots/:id              # Update bot
DELETE /api/bots/:id              # Delete bot
POST   /api/bots/:id/train        # Train bot with data
GET    /api/bots/:id/share        # Get shareable link
POST   /api/bots/:id/clone        # Clone existing bot
```

### Chat Endpoints
```http
GET    /api/chats/:botId          # Get chat history
POST   /api/chats/:botId/message  # Send message to bot
DELETE /api/chats/:chatId         # Delete chat session
GET    /api/chats/:botId/export   # Export chat history
```

### File Upload Endpoints
```http
POST   /api/upload/document       # Upload training document
GET    /api/upload/status/:id     # Check upload status
DELETE /api/upload/:id            # Delete uploaded file
GET    /api/upload/supported      # Get supported file types
```

### Public Bot Endpoints
```http
GET    /api/public/bot/:shareId   # Access shared bot
POST   /api/public/bot/:shareId/chat  # Chat with shared bot
```

### Example API Usage

#### Creating a New Bot
```javascript
const createBot = async (botData) => {
  try {
    const response = await fetch('/api/bots', {
      method: 'POST',
      headers: {
        'Content-Type': 'application/json',
        'Authorization': `Bearer ${token}`
      },
      body: JSON.stringify({
        name: 'My Custom Bot',
        description: 'A bot trained on my company data',
        isPublic: false
      })
    });
    
    const bot = await response.json();
    return bot;
  } catch (error) {
    console.error('Failed to create bot:', error);
  }
};
```

#### Training a Bot with Documents
```javascript
const trainBot = async (botId, files) => {
  const formData = new FormData();
  files.forEach(file => {
    formData.append('documents', file);
  });
  
  try {
    const response = await fetch(`/api/bots/${botId}/train`, {
      method: 'POST',
      headers: {
        'Authorization': `Bearer ${token}`
      },
      body: formData
    });
    
    const result = await response.json();
    return result;
  } catch (error) {
    console.error('Failed to train bot:', error);
  }
};
```

#### Real-time Chat with Socket.IO
```javascript
import io from 'socket.io-client';

const socket = io('http://localhost:5000');

// Join bot room
socket.emit('join-bot', { botId: 'bot123', userId: 'user456' });

// Send message
socket.emit('send-message', {
  botId: 'bot123',
  message: 'Hello, bot!',
  userId: 'user456'
});

// Listen for responses
socket.on('bot-response', (data) => {
  console.log('Bot replied:', data.message);
});

// Listen for typing indicators
socket.on('bot-typing', (data) => {
  console.log('Bot is typing...');
});
```

---

## 🎯 Usage Guide

### Creating Your First Bot

1. **Sign Up/Login**
   - Create an account or login to your existing account
   - Access your personal dashboard

2. **Create New Bot**
   - Click "Create New Bot" button
   - Enter bot name and description
   - Choose visibility settings (private/public)

3. **Train Your Bot**
   - Upload PDF/Text files containing your data
   - Wait for processing to complete
   - Review training summary and accuracy metrics

4. **Test Your Bot**
   - Use the built-in chat interface to test responses
   - Refine training data if needed
   - Adjust bot settings and personality

5. **Share Your Bot**
   - Generate a shareable link
   - Set access permissions
   - Monitor usage statistics

### Advanced Features

#### Bot Customization
- **Personality Settings**: Adjust tone, formality, and response style
- **Response Length**: Control how detailed responses should be
- **Context Memory**: Set how much conversation history to remember
- **Fallback Responses**: Define default responses for unknown queries

#### Training Data Management
- **Multi-format Support**: PDF, TXT, DOC, DOCX files
- **Batch Processing**: Upload multiple files simultaneously
- **Data Validation**: Automatic quality checks and suggestions
- **Version Control**: Track different training iterations

#### Analytics & Insights
- **Usage Statistics**: Track conversations, popular queries, and user engagement
- **Performance Metrics**: Response accuracy, speed, and user satisfaction
- **Training Effectiveness**: Identify gaps in knowledge base
- **Export Data**: Download chat logs and analytics reports

---

## 🧪 Testing

### Running Tests
```bash
# Run all tests
npm run test

# Run client tests only
cd client
npm test

# Run server tests only
cd server
npm test

# Run tests with coverage
npm run test:coverage

# Run specific test suite
npm test -- --grep "Bot Creation"
```

### Test Categories

#### Frontend Tests
- **Component Testing**: Individual component functionality
- **Integration Testing**: Component interactions
- **E2E Testing**: Complete user workflows
- **Accessibility Testing**: WCAG compliance checks

#### Backend Tests
- **Unit Tests**: Individual function testing
- **API Testing**: Endpoint functionality and security
- **Integration Tests**: Database and external service integration
- **Load Testing**: Performance under various loads

### API Testing with Postman
```bash
# Import Postman collection
# File: ./docs/IMBOT.postman_collection.json

# Set environment variables:
# - BASE_URL: http://localhost:5000
# - AUTH_TOKEN: Your JWT token
# - BOT_ID: Test bot ID
```

---

## 🚀 Deployment

### Frontend Deployment (Vercel/Netlify)

#### Vercel Deployment
```bash
# Install Vercel CLI
npm install -g vercel

# Build and deploy
cd client
npm run build
vercel --prod
```

#### Netlify Deployment
```bash
# Build the application
cd client
npm run build

# Deploy build folder to Netlify
# Or use Netlify CLI:
npm install -g netlify-cli
netlify deploy --prod --dir=build
```

### Backend Deployment (Railway/Heroku/DigitalOcean)

#### Railway Deployment
```bash
# Install Railway CLI
npm install -g @railway/cli

# Login and deploy
railway login
railway deploy
```

#### Heroku Deployment
```bash
# Create Heroku app
heroku create imbot-api

# Set environment variables
heroku config:set NODE_ENV=production
heroku config:set MONGODB_URI=your_production_mongodb_uri
heroku config:set GOOGLE_AI_API_KEY=your_production_api_key

# Deploy
git push heroku main
```

### Docker Deployment

#### Dockerfile (Root)
```dockerfile
# Multi-stage build for production
FROM node:18-alpine AS build

# Build client
WORKDIR /app/client
COPY client/package*.json ./
RUN npm ci --only=production
COPY client/ ./
RUN npm run build

# Build server
WORKDIR /app/server
COPY server/package*.json ./
RUN npm ci --only=production
COPY server/ ./

# Production stage
FROM node:18-alpine AS production
WORKDIR /app

# Copy built application
COPY --from=build /app/server ./server
COPY --from=build /app/client/build ./client/build

# Set environment
ENV NODE_ENV=production
EXPOSE 5000

# Start application
CMD ["node", "server/server.js"]
```

#### Docker Compose
```yaml
version: '3.8'
services:
  app:
    build: .
    ports:
      - "5000:5000"
    environment:
      - NODE_ENV=production
      - MONGODB_URI=mongodb://mongo:27017/imbot
      - GOOGLE_AI_API_KEY=${GOOGLE_AI_API_KEY}
    depends_on:
      - mongo
      - redis

  mongo:
    image: mongo:5
    volumes:
      - mongodb_data:/data/db
    ports:
      - "27017:27017"

  redis:
    image: redis:alpine
    ports:
      - "6379:6379"

volumes:
  mongodb_data:
```

### Environment Variables for Production
```env
# Production Environment
NODE_ENV=production

# Database
MONGODB_URI=mongodb+srv://user:password@cluster.mongodb.net/imbot

# AI Service
GOOGLE_AI_API_KEY=your_production_api_key

# Security
JWT_SECRET=your_super_secure_production_jwt_secret

# URLs
CLIENT_URL=https://your-frontend-domain.com
ALLOWED_ORIGINS=https://your-frontend-domain.com

# File Storage
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret

# Monitoring
SENTRY_DSN=your_sentry_dsn_for_error_tracking
```

---

## 🔒 Security Features

### Authentication & Authorization
- **JWT-based Authentication**: Secure token-based user sessions
- **Password Hashing**: bcrypt with configurable salt rounds
- **Role-based Access Control**: Different permissions for users and admins
- **Session Management**: Secure session handling and automatic expiry

### Data Security
- **Input Validation**: Comprehensive validation for all user inputs
- **SQL Injection Prevention**: Parameterized queries and input sanitization
- **XSS Protection**: Content Security Policy and input escaping
- **File Upload Security**: Type validation, size limits, and virus scanning

### API Security
- **Rate Limiting**: Prevent API abuse with configurable limits
- **CORS Configuration**: Controlled cross-origin resource sharing
- **Helmet.js**: Security headers for Express applications
- **Request Logging**: Comprehensive audit trail of API usage

### Infrastructure Security
- **Environment Variables**: Sensitive data protection
- **HTTPS Enforcement**: Secure data transmission
- **Database Security**: Connection encryption and access controls
- **Error Handling**: Secure error responses without sensitive data exposure

---

## 🤝 Contributing

We welcome contributions from the community! Please follow these guidelines:

### Getting Started
1. **Fork the Repository**
   ```bash
   git fork https://github.com/your-username/imbot.git
   ```

2. **Clone Your Fork**
   ```bash
   git clone https://github.com/your-username/imbot.git
   cd imbot
   ```

3. **Create Feature Branch**
   ```bash
   git checkout -b feature/amazing-new-feature
   ```

4. **Set Up Development Environment**
   ```bash
   npm install
   cp .env.example .env
   # Configure your environment variables
   ```

### Development Workflow

#### Code Standards
- **ESLint**: Follow established linting rules
- **Prettier**: Use consistent code formatting
- **Commit Messages**: Follow conventional commit format
- **Documentation**: Update docs for new features

#### Before Submitting
```bash
# Run tests
npm run test

# Check linting
npm run lint

# Format code
npm run format

# Build successfully
npm run build
```

### Pull Request Process
1. **Update Documentation** - Include relevant documentation updates
2. **Add Tests** - Ensure new features are properly tested
3. **Check CI/CD** - All automated tests must pass
4. **Request Review** - Tag maintainers for code review
5. **Address Feedback** - Make requested changes promptly

### Contribution Areas
- 🐛 **Bug Fixes** - Help identify and fix issues
- ✨ **New Features** - Implement requested functionality
- 📝 **Documentation** - Improve guides and API docs
- 🎨 **UI/UX** - Enhance user interface and experience
- 🔧 **Performance** - Optimize speed and efficiency
- 🧪 **Testing** - Add or improve test coverage

---

## 📝 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for complete details.

```
MIT License

Copyright (c) 2024 IMBOT

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## 👨‍💻 Authors & Contributors

### **Core Team**
- **[Your Name]** - *Project Creator & Lead Developer*
  - 🔗 GitHub: [@your-username](https://github.com/your-username)
  - 💼 LinkedIn: [Your Profile](https://linkedin.com/in/your-profile)
  - 📧 Email: your.email@example.com

### **Contributors**
We thank all our contributors who help make IMBOT better:
- [@contributor1](https://github.com/contributor1) - Feature development
- [@contributor2](https://github.com/contributor2) - Bug fixes and testing
- [@contributor3](https://github.com/contributor3) - Documentation improvements

*Want to see your name here? [Contribute to IMBOT](CONTRIBUTING.md)!*

---

## 🙏 Acknowledgments

### **Special Thanks**
- **Google AI Team** - For providing the powerful Gen AI API
- **MongoDB Team** - For the robust and scalable database solution
- **React Community** - For the amazing frontend framework and ecosystem
- **Node.js Contributors** - For the excellent JavaScript runtime
- **Open Source Community** - For countless packages and tools that make this possible

### **Inspiration & Resources**
- **ChatGPT & AI Assistants** - Inspiration for conversational AI
- **Modern Web Design** - UI/UX inspiration from leading applications
- **Open Source Projects** - Learning from successful community projects
- **Developer Community** - Stack Overflow, GitHub, and tech blogs for solutions

---

## 📞 Support & Contact

### **Getting Help**
1. **📋 Check Documentation** - Review this README and [API docs](docs/api.md)
2. **🔍 Search Issues** - Look through [existing issues](https://github.com/your-username/imbot/issues)
3. **❓ Ask Questions** - Create a new issue with the "question" label
4. **💬 Community Chat** - Join our [Discord/Slack community](#) (if available)

### **Report Bugs**
🐛 Found a bug? Please create an issue with:
- Detailed description of the problem
- Steps to reproduce the issue
- Expected vs actual behavior
- Screenshots or error messages
- Environment details (OS, browser, Node.js version)

### **Contact Information

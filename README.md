# AI Mock Interview App

A cutting-edge AI-powered mock interview platform designed to help job seekers improve their interview skills through personalized practice sessions and intelligent feedback.

## Features

### AI-Powered Interview Generation
- **Dynamic Question Generation**: Creates tailored interview questions based on job position, experience level, and tech stack
- **Realistic Interview Scenarios**: Simulates actual interview environments to build confidence
- **Customizable Parameters**: Adjust difficulty, focus areas, and interview duration

### Interactive Interview Experience
- **Video Recording**: Practice with webcam integration for realistic interview simulation
- **Speech-to-Text**: Advanced voice recognition to capture verbal responses
- **Real-time Question Display**: Clear, organized question presentation during interviews

### Intelligent Feedback System
- **AI-Powered Analysis**: Get detailed feedback on your answers using Google Generative AI
- **Performance Ratings**: Receive numerical scores and constructive criticism
- **Personalized Suggestions**: Targeted recommendations for improvement

### User Management & Authentication
- **Secure Authentication**: Built with Clerk for seamless sign-up/sign-in experience
- **Personal Dashboard**: Track all your interview sessions and progress
- **Data Persistence**: Firebase backend for reliable data storage

### Modern UI/UX
- **Responsive Design**: Fully responsive interface built with Tailwind CSS
- **Dark/Light Mode**: Theme switching for comfortable usage
- **Intuitive Navigation**: Clean, user-friendly interface with smooth transitions

## Tech Stack

### Frontend
- **React 19** - Modern React with latest features
- **TypeScript** - Type-safe development
- **Vite** - Fast build tool and dev server
- **Tailwind CSS** - Utility-first CSS framework
- **Radix UI** - Accessible component primitives
- **Lucide React** - Beautiful icon library
- **React Router** - Client-side routing

### Backend & Services
- **Firebase** - Database, authentication, and hosting
- **Clerk** - User authentication and management
- **Google Generative AI** - AI-powered question generation and feedback
- **React Webcam** - Video recording capabilities
- **React Hook Speech-to-Text** - Voice recognition

### Development Tools
- **ESLint** - Code linting and formatting
- **PostCSS** - CSS processing
- **TypeScript** - Static type checking

## Getting Started

### Prerequisites
- Node.js (v18 or higher)
- npm, yarn, or pnpm
- Firebase account
- Google AI Studio API key
- Clerk account

### Installation

1. **Clone the repository**
   ```bash
   git clone    git clone https://github.com/yourusername/mock-interview-app.git
   cd mock-interview-app
   ```

2. **Install dependencies**
   ```bash
   npm install
   # or
   yarn install
   # or
   pnpm install
   ```

3. **Environment Setup**
   
   Create a `.env` file in the root directory:
   ```env
   VITE_CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key
   VITE_FIREBASE_API_KEY=your_firebase_api_key
   VITE_FIREBASE_AUTH_DOMAIN=your_project.firebaseapp.com
   VITE_FIREBASE_PROJECT_ID=your_project_id
   VITE_FIREBASE_STORAGE_BUCKET=your_project.appspot.com
   VITE_FIREBASE_MESSAGING_SENDER_ID=your_sender_id
   VITE_FIREBASE_APP_ID=your_app_id
   VITE_GEMINI_API_KEY=your_gemini_api_key
   ```

4. **Firebase Configuration**
   
   - Create a new Firebase project at [Firebase Console](https://console.firebase.google.com/)
   - Enable Firestore Database
   - Set up Firebase Authentication
   - Configure Firebase Hosting (optional)
   - Update `firebase.json` with your project settings

5. **Clerk Setup**
   
   - Create a Clerk account at [Clerk Dashboard](https://dashboard.clerk.com/)
   - Create a new application
   - Configure your allowed redirect URLs
   - Copy your publishable key to the environment variables

6. **Google AI Studio Setup**
   
   - Get your API key from [Google AI Studio](https://aistudio.google.com/app/apikey)
   - Add the key to your environment variables

### Running the Application

1. **Development Server**
   ```bash
   npm run dev
   # or
   yarn dev
   # or
   pnpm dev
   ```

2. **Build for Production**
   ```bash
   npm run build
   # or
   yarn build
   # or
   pnpm build
   ```

3. **Preview Production Build**
   ```bash
   npm run preview
   # or
   yarn preview
   # or
   pnpm preview
   ```

## Project Structure

```
src/
├── components/          # Reusable UI components
│   ├── ui/             # Base UI components (shadcn/ui)
│   ├── form-mock-interview.tsx
│   ├── interview-pin.tsx
│   ├── question-section.tsx
│   └── record-answer.tsx
├── config/             # Configuration files
│   └── firebase.config.ts
├── handlers/           # API handlers and utilities
├── layouts/            # Page layout components
├── lib/                # Utility functions
├── provider/           # Context providers
├── routes/             # Page components
│   ├── home.tsx
│   ├── dashboard.tsx
│   ├── mock-interview-page.tsx
│   └── feedback.tsx
├── script/             # External scripts
├── types/              # TypeScript type definitions
└── assets/             # Static assets
```

## How It Works

1. **User Authentication**: Sign up or sign in using Clerk
2. **Create Interview**: Specify job position, experience, and tech stack
3. **AI Question Generation**: Google Gemini generates relevant interview questions
4. **Mock Interview**: Answer questions via video and voice recording
5. **AI Analysis**: Get instant feedback and performance ratings
6. **Review Progress**: Track improvement over time in your dashboard

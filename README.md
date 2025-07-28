# Prompt Manager

A modern, feature-rich prompt management website built with React and TypeScript. Organize, edit, and polish your AI prompts across different projects with intelligent analysis and suggestions.

## ✨ Features

### 🎯 Core Functionality
- **Prompt Management**: Create, edit, and organize prompts with rich metadata
- **Project Organization**: Group prompts by projects with custom colors
- **Category System**: Further organize prompts within projects
- **Tagging System**: Add custom tags for easy searching and filtering
- **Favorites**: Mark and filter your most important prompts

### 🔍 Smart Search & Filtering
- **Full-text Search**: Search across prompt titles, content, and tags
- **Project Filtering**: Filter prompts by specific projects
- **Category Filtering**: Filter prompts by categories within projects
- **Favorites Filter**: Show only your favorite prompts
- **Combined Filters**: Use multiple filters simultaneously

### 🧠 Intelligent Prompt Analysis
- **Real-time Analysis**: Get instant feedback as you write
- **Readability Scoring**: Flesch Reading Ease score for clarity
- **Word & Character Count**: Track prompt length and complexity
- **Token Estimation**: Estimate token usage for AI models
- **Smart Suggestions**: Get actionable tips to improve your prompts

### 💡 Prompt Improvement Suggestions
- **Clarity**: Replace vague pronouns and subjective terms
- **Specificity**: Add context and examples for better results
- **Structure**: Improve prompt formatting and organization
- **Context**: Add relevant background information
- **Tone**: Optimize language for professional communication

### 🎨 Modern UI/UX
- **Responsive Design**: Works perfectly on desktop, tablet, and mobile
- **Beautiful Interface**: Clean, modern design with smooth animations
- **Intuitive Navigation**: Easy-to-use sidebar and filtering system
- **Quick Actions**: Copy prompts with one click
- **Visual Feedback**: Clear status indicators and notifications

## 🚀 Getting Started

### Prerequisites
- Node.js (version 16 or higher)
- npm or yarn package manager

### Installation

1. **Clone or download the project**
   ```bash
   git clone <repository-url>
   cd prompt-manager
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up Firebase (Optional - for cloud storage)**
   
   The app works with localStorage by default, but you can set up Firebase for cloud storage:
   
   a. **Create a Firebase project**:
   - Go to [Firebase Console](https://console.firebase.google.com/)
   - Click "Add project"
   - Follow the setup wizard
   
   b. **Enable Firestore Database**:
   - In your Firebase project, go to "Firestore Database"
   - Click "Create database"
   - Choose "Start in test mode" for development
   
   c. **Get your Firebase config**:
   - Go to Project Settings (gear icon)
   - Scroll down to "Your apps"
   - Click the web app icon (</>)
   - Copy the config object
   
   d. **Create environment file**:
   ```bash
   cp .env.example .env.local
   ```
   
   e. **Add your Firebase config to .env.local**:
   ```
   REACT_APP_FIREBASE_API_KEY=your-api-key
   REACT_APP_FIREBASE_AUTH_DOMAIN=your-project.firebaseapp.com
   REACT_APP_FIREBASE_PROJECT_ID=your-project-id
   REACT_APP_FIREBASE_STORAGE_BUCKET=your-project.appspot.com
   REACT_APP_FIREBASE_MESSAGING_SENDER_ID=123456789
   REACT_APP_FIREBASE_APP_ID=your-app-id
   ```

4. **Start the development server**
   ```bash
   npm start
   ```

5. **Open your browser**
   Navigate to `http://localhost:3000` to see the application

### Building for Production

```bash
npm run build
```

This creates an optimized production build in the `build` folder.

## 📁 Project Structure

```
src/
├── components/          # React components
│   ├── PromptCard.tsx   # Individual prompt display
│   ├── PromptForm.tsx   # Add/edit prompt form
│   ├── ProjectForm.tsx  # Add/edit project form
│   └── Sidebar.tsx      # Navigation sidebar
├── types/               # TypeScript type definitions
│   └── index.ts
├── utils/               # Utility functions
│   ├── storage.ts       # Local storage management
│   └── promptAnalysis.ts # Prompt analysis and suggestions
├── App.tsx              # Main application component
├── index.tsx            # Application entry point
└── index.css            # Global styles
```

## 🎯 How to Use

### Creating Your First Prompt

1. Click the "New Prompt" button in the header
2. Fill in the prompt title and content
3. Select a project (or create a new one)
4. Optionally add categories and tags
5. Use the "Analysis" feature to get improvement suggestions
6. Save your prompt

### Organizing with Projects

1. Click the "+" button next to "Projects" in the sidebar
2. Enter a project name and description
3. Choose a color to distinguish it visually
4. Create prompts within that project

### Using the Analysis Feature

1. While editing a prompt, click the "Analysis" button
2. Review the metrics (word count, readability, etc.)
3. Read through the improvement suggestions
4. Apply the suggestions to make your prompt better

### Searching and Filtering

1. Use the search bar to find specific prompts
2. Click on projects in the sidebar to filter by project
3. Select categories to further narrow down results
4. Toggle "Favorites" to see only your starred prompts

## 💾 Data Storage

The application supports two storage options:

### 🔄 Hybrid Storage System
- **Primary**: Firebase Firestore (when configured)
- **Fallback**: Browser localStorage (always available)
- **Automatic**: Seamlessly switches between storage methods

### 🌐 Firebase Firestore (Cloud Storage)
When Firebase is configured, you get:
- **Cloud Sync**: Access your prompts from any device
- **Real-time Updates**: Changes sync instantly across devices
- **Backup**: Your data is safely stored in the cloud
- **Collaboration**: Share projects with team members (future feature)

### 💻 Local Storage (Default)
When Firebase is not configured:
- **Privacy**: Your prompts stay on your device
- **Speed**: Instant access without network requests
- **Offline Access**: Work without an internet connection
- **No Account Required**: Start using immediately

## 🛠️ Technology Stack

- **React 18**: Modern React with hooks and functional components
- **TypeScript**: Type-safe development experience
- **Tailwind CSS**: Utility-first CSS framework for styling
- **Lucide React**: Beautiful, customizable icons
- **Local Storage**: Client-side data persistence

## 🎨 Customization

### Styling
The application uses Tailwind CSS for styling. You can customize:
- Colors in `tailwind.config.js`
- Component styles in `src/index.css`
- Individual component styling

### Adding Features
The modular architecture makes it easy to add new features:
- New components in `src/components/`
- Utility functions in `src/utils/`
- Type definitions in `src/types/`

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

## 🆘 Support

If you encounter any issues or have questions:
1. Check the browser console for error messages
2. Ensure you're using a modern browser
3. Try clearing your browser's localStorage if data seems corrupted
4. Create an issue in the repository

---

**Happy Prompt Engineering! 🚀** 
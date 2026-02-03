# CodeSaathi - AI-Powered Learning Companion

CodeSaathi is an AI-powered learning and debugging companion designed for students and beginner developers. It helps users understand source code, debug errors, and learn programming concepts using simple explanations in Hinglish (Hindi + English).

## 🎯 Problem Statement

Students and beginner developers often struggle with:

- Understanding complex codebases
- Deciphering cryptic error messages
- Navigating lengthy documentation
- Learning programming concepts effectively

CodeSaathi solves these problems by providing AI-powered explanations in beginner-friendly language.

## ✨ Features

### 🔍 Code Explanation

- **Line-by-line code analysis** - Understand what each line does
- **Beginner-friendly explanations** - Simple language with Hinglish support
- **Concept highlighting** - Learn programming concepts as you go
- **Support for JavaScript and Python**

### 🐛 Error Debugging Assistant

- **Simplified error explanations** - Convert technical errors into plain language
- **Suggested fixes** - Get actionable solutions to fix your code
- **Learning tips** - Understand why errors happen and how to prevent them
- **Common error patterns** - Learn from typical beginner mistakes

### 📚 Documentation Summarization

- **Quick summaries** - Get the gist of long documentation
- **Key concept extraction** - Focus on what matters for beginners
- **Technology explanations** - Understand what tools and libraries do
- **Getting started guides** - Know how to begin using new technologies

### 🎓 Learning Mode

- **Enhanced explanations** - More detailed educational content
- **Concept recommendations** - Discover related topics to learn
- **Progressive difficulty** - Explanations adapted to your level
- **Educational context** - Understand the "why" behind the code

## 🚀 Getting Started

### Prerequisites

- Node.js (v14 or higher)
- npm or yarn
- OpenAI API key

### Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/yourusername/codesaathi.git
   cd codesaathi
   ```

2. **Install backend dependencies**

   ```bash
   cd backend
   npm install
   ```

3. **Install frontend dependencies**

   ```bash
   cd ../frontend
   npm install
   ```

4. **Set up environment variables**

   Create a `.env` file in the backend directory:

   ```env
   OPENAI_API_KEY=your_openai_api_key_here
   PORT=3001
   NODE_ENV=development
   ```

### Running the Application

1. **Start the backend server**

   ```bash
   cd backend
   npm start
   ```

   The backend will run on `http://localhost:3001`

2. **Start the frontend (in a new terminal)**

   ```bash
   cd frontend
   npm start
   ```

   The frontend will run on `http://localhost:3000`

3. **Open your browser** and navigate to `http://localhost:3000`

## 📖 Usage Examples

### Code Explanation

```javascript
// Paste this code into CodeSaathi
function calculateSum(numbers) {
  let total = 0;
  for (let i = 0; i < numbers.length; i++) {
    total += numbers[i];
  }
  return total;
}
```

**CodeSaathi explains:**

- Line 1: Function definition - yeh function numbers ka array leta hai
- Line 2: Variable initialization - total ko 0 se start karte hain
- Line 3-5: Loop through array - har number ko total mein add karte hain
- Line 6: Return result - final sum return karte hain

### Error Debugging

```
Error: Cannot read property 'length' of undefined
```

**CodeSaathi explains:**

- **What went wrong:** Aapka variable undefined hai, uska length nahi mil sakta
- **Possible cause:** Array properly initialize nahi kiya gaya
- **Fix:** Check if variable exists before using: `if (array && array.length)`
- **Learning tip:** Always validate inputs before using them

### Documentation Summary

**Input:** React.js documentation
**CodeSaathi summary:**

- **What it does:** React ek JavaScript library hai for building user interfaces
- **Key features:** Components, Virtual DOM, State management
- **Getting started:** `npx create-react-app my-app`
- **Main concepts:** JSX, Props, State, Hooks

## 🛠️ Development

### Project Structure

```
codesaathi/
├── frontend/                 # React frontend
│   ├── src/
│   │   ├── components/      # React components
│   │   ├── services/        # API services
│   │   └── styles/          # CSS modules
│   └── package.json
├── backend/                 # Node.js backend
│   ├── src/
│   │   ├── routes/          # API routes
│   │   ├── services/        # Business logic
│   │   └── utils/           # Utility functions
│   └── package.json
└── README.md
```

### API Endpoints

#### Code Explanation

```http
POST /api/explain-code
Content-Type: application/json

{
  "code": "console.log('Hello World');",
  "language": "javascript",
  "isLearningMode": true
}
```

#### Error Debugging

```http
POST /api/debug-error
Content-Type: application/json

{
  "errorMessage": "SyntaxError: Unexpected token",
  "language": "javascript",
  "isLearningMode": false
}
```

#### Documentation Summary

```http
POST /api/summarize-docs
Content-Type: application/json

{
  "content": "# React Documentation...",
  "isLearningMode": true
}
```

### Running Tests

**Backend tests:**

```bash
cd backend
npm test
```

**Frontend tests:**

```bash
cd frontend
npm test
```

## 🔧 Configuration

### Environment Variables

| Variable         | Description                  | Default     |
| ---------------- | ---------------------------- | ----------- |
| `OPENAI_API_KEY` | Your OpenAI API key          | Required    |
| `PORT`           | Backend server port          | 3001        |
| `NODE_ENV`       | Environment mode             | development |
| `CACHE_TTL`      | Cache time-to-live (seconds) | 300         |

### Customizing AI Responses

You can modify the prompt templates in `backend/src/services/promptTemplates.js` to customize how CodeSaathi explains code and errors.

## 🤝 Contributing

We welcome contributions! Here's how you can help:

1. **Fork the repository**
2. **Create a feature branch** (`git checkout -b feature/amazing-feature`)
3. **Make your changes**
4. **Add tests** for new functionality
5. **Commit your changes** (`git commit -m 'Add amazing feature'`)
6. **Push to the branch** (`git push origin feature/amazing-feature`)
7. **Open a Pull Request**

### Development Guidelines

- Write clear, commented code
- Add tests for new features
- Follow existing code style
- Update documentation as needed
- Test with both JavaScript and Python examples

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- OpenAI for providing the GPT API
- The open-source community for inspiration
- Students and educators who provided feedback

## 📞 Support

If you have questions or need help:

1. **Check the documentation** in this README
2. **Search existing issues** on GitHub
3. **Create a new issue** with detailed information
4. **Join our community** discussions

## 🗺️ Roadmap

### Current Version (v1.0)

- ✅ Code explanation for JavaScript and Python
- ✅ Error debugging assistance
- ✅ Documentation summarization
- ✅ Learning mode toggle
- ✅ Hinglish support

### Future Versions

- 🔄 Support for more programming languages (Java, C++, Go)
- 🔄 Code quality suggestions and best practices
- 🔄 Interactive coding exercises
- 🔄 Progress tracking and learning analytics
- 🔄 Mobile app version
- 🔄 Offline mode with cached explanations

## 🎓 Educational Use

CodeSaathi is designed specifically for educational purposes:

- **For Students:** Learn programming concepts through practical examples
- **For Educators:** Use as a teaching aid to explain complex code
- **For Bootcamps:** Help students debug and understand assignments
- **For Self-learners:** Get instant help when stuck on coding problems

---

**Made with ❤️ for the programming community**

_CodeSaathi - Your friendly neighborhood coding companion!_

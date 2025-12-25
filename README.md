# 🧠 **VortexMind AI - Adaptive E-Learning Platform**

<div align="center">

![VortexMind](https://img.shields.io/badge/VortexMind-AI%20Education-a855f7?style=for-the-badge&logo=brain&logoColor=white)
![Python](https://img.shields.io/badge/Python-3.x-3776ab?style=for-the-badge&logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-2.x-000000?style=for-the-badge&logo=flask&logoColor=white)
![Google Gemini](https://img.shields.io/badge/Google-Gemini%202.5-4285f4?style=for-the-badge&logo=google&logoColor=white)

**An AI-powered e-learning platform that transforms static documents into interactive learning experiences**

</div>

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [Project Structure](#-project-structure)
- [Tech Stack](#️-tech-stack)
- [Installation](#-installation)
- [Configuration](#-configuration)
- [Usage](#-usage)
- [Screenshots](#-screenshots)
- [API Endpoints](#-api-endpoints)
- [Contributing](#-contributing)

---

## 🌟 Overview

VortexMind AI is a sophisticated web application designed to revolutionize the way students interact with learning materials. By leveraging Google's Gemini AI, this platform transforms static PDFs into dynamic, interactive learning experiences.

### Problem Statement

Traditional e-learning platforms often fail to adapt to individual learners:
- 📚 Students spend hours going through long PDFs without personalized assistance
- 🔍 Extracting key insights and summaries requires significant effort
- 💻 Converting concepts into executable code is challenging
- 🎥 Lacking contextual multimedia support for different learning styles
- ❌ Limited annotation and adaptive learning feedback

### Our Solution

VortexMind AI addresses these challenges by providing:
- **AI-Driven Conversations** - Chat with your documents naturally
- **Smart Summarization** - Generate structured summaries instantly
- **Interactive Tools** - Whiteboard, Graph Plotter, Quiz Generator
- **Code Generation** - Convert technical content to executable code
- **Study Assistance** - Wikipedia lookup, Code Helper, and more

---

## ✨ Features

### 📄 **PDF Summarizer**
Upload PDFs up to 50MB and interact with AI-powered analysis:
- Text extraction using PyPDF2
- AI conversation about document content
- Structured HTML summaries
- Mind map generation
- Quiz creation from content
- YouTube video suggestions
- Page-specific queries ("What's on page 10?")
- Pomodoro timer for focused study

### 🌐 **Wikipedia Lookup**
Search any topic and get AI-powered summaries:
- Real-time Wikipedia API integration
- AI-enhanced summaries with key insights
- Clean, structured presentation

### 💻 **Code Helper**
Get AI assistance for all your coding needs:
- **Explain Code** - Understand complex code snippets
- **Debug Errors** - Find and fix bugs
- **Error Explainer** - Understand error messages
- **Optimize Code** - Improve performance
- **Ask Questions** - General coding queries
- Syntax highlighting with Fira Code font

### ✍️ **AI Humanizer**
Transform AI-generated text into natural, human-like writing:
- Multiple style options: Natural, Casual, Professional, Academic, Creative
- Character count tracking
- One-click copy functionality

### 🎨 **Whiteboard**
A full-featured digital whiteboard:
- 8 preset pen colors + custom color picker
- Adjustable brush sizes (1-50px)
- Highlighter with opacity control
- Eraser tool
- Shape tools: Line, Rectangle, Circle, Triangle, Arrow, Star
- Text input
- Undo/Redo functionality (50 steps)
- Clear canvas option
- Save as PNG
- Light/Dark canvas toggle
- Touch support for tablets

### 📈 **Graph Plotter**
Visualize mathematical equations interactively:
- Multiple equation support with color coding
- Explicit equations (y = f(x))
- Implicit equations (x² + y² = 25)
- Vertical lines (x = 5)
- Quick example equations
- Customizable axis ranges
- Grid toggle
- Real-time coordinate display
- Zoom and pan functionality
- Download as PNG

---

## 📂 Project Structure

```
VortexMind_AI/
├── main.py                 # Flask application entry point
├── reader.py               # PDF reading utilities
├── requirements.txt        # Python dependencies
├── readme.md               # This file
│
├── static/                 # Static assets
│   ├── input.css           # Base styles & design system
│   ├── viewer.css          # PDF viewer styles
│   ├── portal.css          # Homepage/portal styles
│   ├── tools.css           # Tool pages (Code Helper, Humanizer, Wikipedia)
│   ├── whiteboard.css      # Whiteboard styles
│   ├── grapher.css         # Graph plotter styles
│   └── favico.ico          # Favicon
│
├── templates/              # Jinja2 HTML templates
│   ├── index.html          # Homepage portal
│   ├── pdfinput.html       # PDF upload page
│   ├── viewer.html         # PDF viewer with AI chat
│   ├── analyzer.html       # PDF analysis page
│   ├── wikipedia.html      # Wikipedia lookup
│   ├── codehelper.html     # Code helper tool
│   ├── humanizer.html      # AI humanizer tool
│   ├── whiteboard.html     # Digital whiteboard
│   └── grapher.html        # Equation graph plotter
│
├── uploads/                # Uploaded PDF storage
└── venv/                   # Python virtual environment
```

---

## 🛠️ Tech Stack

### Backend
| Technology | Purpose |
|------------|---------|
| **Python 3.x** | Core programming language |
| **Flask 2.x** | Web framework |
| **Google Gemini 2.5 Flash** | AI model for text generation |
| **PyPDF2** | PDF text extraction |
| **Requests** | HTTP client for APIs |

### Frontend
| Technology | Purpose |
|------------|---------|
| **HTML5** | Structure & semantics |
| **CSS3** | Styling with modern features |
| **Vanilla JavaScript** | Interactivity |
| **Poppins & Inter** | Typography (Google Fonts) |
| **Fira Code** | Monospace font for code |
| **function-plot** | Mathematical graphing library |
| **D3.js** | Data visualization support |

### Design System
| Feature | Implementation |
|---------|----------------|
| **Glassmorphism** | Backdrop blur effects |
| **Neon Accents** | Vibrant purple/cyan/green highlights |
| **Dark Mode First** | Deep navy backgrounds |
| **Responsive Design** | Mobile-friendly layouts |
| **Micro-animations** | Smooth transitions & hover effects |

---

## 📦 Installation

### Prerequisites
- Python 3.8 or higher
- pip (Python package manager)
- A Google Gemini API key

### Step-by-Step Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/VortexMind_AI.git
   cd VortexMind_AI
   ```

2. **Create a virtual environment** (Recommended)
   ```bash
   python -m venv venv
   
   # Activate on Linux/macOS
   source venv/bin/activate
   
   # Activate on Windows
   venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up environment variable**
   ```bash
   # Linux/macOS
   export GEMINI_API_KEY="your_api_key_here"
   
   # Windows (Command Prompt)
   set GEMINI_API_KEY=your_api_key_here
   
   # Windows (PowerShell)
   $env:GEMINI_API_KEY="your_api_key_here"
   ```

5. **Run the application**
   ```bash
   python main.py
   ```

6. **Open in browser**
   ```
   http://127.0.0.1:5000
   ```

---

## ⚙️ Configuration

### Environment Variables

| Variable | Required | Description |
|----------|----------|-------------|
| `GEMINI_API_KEY` | ✅ Yes | Your Google Gemini API key |

### Getting a Gemini API Key

1. Visit [Google AI Studio](https://aistudio.google.com/)
2. Sign in with your Google account
3. Navigate to "Get API Key"
4. Create a new API key
5. Copy and set as `GEMINI_API_KEY` environment variable

### Application Settings

In `main.py`, you can configure:

```python
app.config['MAX_CONTENT_LENGTH'] = 50 * 1024 * 1024  # Max upload size (50MB)
ALLOWED_EXTENSIONS = {'pdf'}  # Allowed file types
```

---

## 🚀 Usage

### PDF Summarizer

1. From the portal, click **"PDF Summarizer"**
2. Upload a PDF file (max 50MB, OCR-scanned recommended)
3. Use the chat interface to ask questions about the content
4. Click **"Summarize"** for a structured overview
5. Generate **Mind Maps** for visual learning
6. Create **Quizzes** to test your knowledge
7. Search related **YouTube videos**

### Wikipedia Lookup

1. Select **"Wikipedia"** from the portal
2. Enter any topic in the search field
3. Get an AI-enhanced summary with key insights

### Code Helper

1. Open **"Code Helper"** from the portal
2. Select a mode (Explain, Debug, Error, Optimize, Question)
3. Paste your code or ask a question
4. Receive AI-powered assistance

### AI Humanizer

1. Access **"AI Humanizer"** from the portal
2. Choose your desired writing style
3. Paste AI-generated text
4. Get humanized, natural-sounding output

### Whiteboard

1. Click **"Whiteboard"** from the portal
2. Select tools: Pen, Highlighter, Eraser, Shapes, Text
3. Choose colors and brush sizes
4. Draw, annotate, and create diagrams
5. Save your work as PNG

### Graph Plotter

1. Open **"Graph Plotter"** from the portal
2. Enter equations (e.g., `x^2`, `sin(x)`, `x^2 + y^2 - 25`)
3. Customize axis ranges and colors
4. Add multiple equations for comparison
5. Download the graph as PNG

---

## 📸 Screenshots

### Homepage Portal
*Modern card-based navigation to all features*

### PDF Viewer with AI Chat
*Interactive PDF reading with AI conversation*

### Equation Graph Plotter
*Mathematical visualization with multiple equations*

### Digital Whiteboard
*Full-featured drawing canvas with tools*

### Code Helper
*AI-powered coding assistance*

---

## 🔌 API Endpoints

### Core Routes

| Method | Endpoint | Description |
|--------|----------|-------------|
| `GET` | `/` | Homepage portal |
| `GET` | `/pdfinput` | PDF upload page |
| `GET` | `/wikipedia` | Wikipedia lookup page |
| `GET` | `/codehelper` | Code helper page |
| `GET` | `/humanizer` | AI humanizer page |
| `GET` | `/whiteboard` | Whiteboard page |
| `GET` | `/grapher` | Graph plotter page |
| `GET` | `/viewer` | PDF viewer page |

### API Routes

| Method | Endpoint | Description |
|--------|----------|-------------|
| `POST` | `/chat` | AI chat with PDF content |
| `POST` | `/summarize` | Generate PDF summary |
| `POST` | `/start_quiz` | Start a quiz session |
| `POST` | `/quiz_answer` | Submit quiz answer |
| `POST` | `/mindmap` | Generate mind map |
| `POST` | `/wikipedia/search` | Wikipedia search & summarize |
| `POST` | `/codehelper/ask` | Code assistance request |
| `POST` | `/humanizer/convert` | Humanize text |

---

## 📝 Requirements

```
Flask>=2.0.0
google-generativeai>=0.3.0
PyPDF2>=3.0.0
requests>=2.28.0
Werkzeug>=2.0.0
```

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

---

## 🙏 Acknowledgments

- **Google Gemini AI** - Powering our intelligent features
- **Flask** - Lightweight and powerful web framework
- **function-plot** - Beautiful mathematical graphing
- **Open Source Community** - For the amazing tools and libraries

---

<div align="center">

**Made with ❤️ for learners everywhere**

✨ *Transforming the way you learn, one document at a time* ✨

</div>

# 🚀 PagePilot - AI-Powered Website Builder

![PagePilot](https://img.shields.io/badge/Built%20with-React%20%2B%20TypeScript-blue?style=for-the-badge)
![Vite](https://img.shields.io/badge/Bundler-Vite-646CFF?style=for-the-badge)
![Tailwind CSS](https://img.shields.io/badge/CSS-Tailwind-38B2AC?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

> **Create professional, production-ready websites in seconds using AI.** Just describe your vision, and PagePilot generates clean HTML, CSS, and JavaScript code instantly.

## 📋 Table of Contents

- [Features](#features)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
- [Project Structure](#project-structure)
- [How It Works](#how-it-works)
- [Configuration](#configuration)
- [Usage](#usage)
- [Components](#components)
- [API Integration](#api-integration)
- [Contributing](#contributing)
- [License](#license)

---

## ✨ Features

✅ **AI-Powered Code Generation** — Describe your website idea in plain English; Gemini AI generates complete code  
✅ **Live Preview** — See your website rendered in real-time as you generate  
✅ **Code Tabs** — View and copy HTML, CSS, and JavaScript separately  
✅ **Download HTML** — Get production-ready single HTML file  
✅ **Chat History** — Save and manage up to 10 past generations  
✅ **Responsive Design** — Mobile-first approach with Tailwind CSS  
✅ **Fullscreen Preview** — Expand preview to full screen for better viewing  
✅ **Image Integration** — Pexels API auto-fetches relevant images  
✅ **Copy to Clipboard** — One-click code copying  
✅ **Dark Theme** — Beautiful, modern UI with gradient backgrounds  

---

## 🛠️ Tech Stack

| Technology | Purpose |
|------------|---------|
| **React 18** | UI library |
| **TypeScript** | Type safety |
| **Vite** | Fast build tool |
| **Tailwind CSS** | Utility-first CSS |
| **Lucide React** | Icon library |
| **Google Generative AI** | AI code generation (Gemini 2.5 Flash) |
| **Pexels API** | Image fetching |
| **localStorage** | Session persistence |

---

## 🚀 Getting Started

### Prerequisites

- **Node.js** (v16+)
- **npm** (v7+)
- **Google Generative AI API Key** ([Get it here](https://makersuite.google.com/app/apikey))
- **Pexels API Key** ([Get it here](https://www.pexels.com/api/))

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/pagepilot.git
   cd pagepilot
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Create `.env` file**
   ```bash
   cp .env.example .env
   ```

4. **Add your API keys** to `.env`
   ```env
   VITE_GEMINI_API_KEY=your_gemini_api_key_here
   ```
   
   > **Note:** Pexels API key is currently hardcoded. Move it to `.env` for production:
   ```env
   VITE_PEXELS_API_KEY=your_pexels_api_key_here
   ```

5. **Start development server**
   ```bash
   npm run dev
   ```

6. **Open in browser**
   ```
   http://localhost:5173
   ```

---

## 📁 Project Structure

```
pagepilot/
├── src/
│   ├── App.tsx                    # Landing page & main component
│   ├── main.tsx                   # React entry point
│   ├── index.css                  # Global styles
│   ├── components/
│   │   ├── CodeGenerator.tsx       # AI builder with preview (main feature)
│   │   └── ChatHistory.tsx         # Session history sidebar
│   └── vite-env.d.ts              # TypeScript declarations
├── public/
│   └── screenshots/               # "How it Works" carousel images
├── .env                           # Environment variables (git ignored)
├── .env.example                   # Environment template
├── .gitignore                     # Git ignore rules
├── package.json                   # Dependencies & scripts
├── vite.config.ts                 # Vite configuration
├── tailwind.config.js             # Tailwind setup
├── postcss.config.js              # PostCSS config
├── tsconfig.json                  # TypeScript config
├── eslint.config.js               # ESLint rules
└── README.md                      # This file
```

---

## 🔄 How It Works

### User Journey

```
1. User lands on homepage
   ↓
2. Clicks "Start Building Now"
   ↓
3. Enters website description (or picks example)
   ↓
4. Clicks "Generate Website"
   ↓
5. AI generates HTML, CSS, JavaScript
   ↓
6. Live preview renders in iframe
   ↓
7. User can:
   ├─ View code in tabs
   ├─ Copy code to clipboard
   ├─ Download as single HTML file
   ├─ View fullscreen preview
   └─ Save to chat history
   ↓
8. Session saved to localStorage
   ↓
9. User can load past sessions anytime
```

### Code Generation Flow

```
User Prompt
    ↓
Fetch Image (Pexels API)
    ↓
Build System Prompt with Image URL
    ↓
Stream from Gemini API
    ↓
Parse Response (HTML/CSS/JS blocks)
    ↓
Create Session Object
    ↓
Save to localStorage
    ↓
Combine into Full HTML
    ↓
Render in iframe Preview
    ↓
Display to User ✅
```

---

## ⚙️ Configuration

### Environment Variables

Create `.env` file with:

```env
# Google Generative AI (Required)
VITE_GEMINI_API_KEY=your_api_key_here

# Pexels API (Optional - currently hardcoded)
VITE_PEXELS_API_KEY=your_pexels_key_here
```

### Tailwind CSS

Custom configuration in `tailwind.config.js`:

```javascript
export default {
  content: ['./index.html', './src/**/*.{js,ts,jsx,tsx}'],
  theme: {
    extend: {
      colors: {
        // Custom colors
      },
    },
  },
  plugins: [],
}
```

---

## 💻 Usage

### Development

```bash
# Start dev server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview

# Run linter
npm run lint
```

### Generating a Website

1. **Describe your idea:**
   ```
   "Create a modern landing page for a SaaS product with hero section, features, pricing, and CTA buttons"
   ```

2. **Or pick an example:**
   - Coffee shop landing page
   - Portfolio website
   - Calculator app
   - Todo list app
   - Weather dashboard

3. **View live preview** as code generates

4. **Copy or download** the code

5. **Deploy** to Netlify, Vercel, or your host

---

## 🧩 Components

### App.tsx
**Landing page** with:
- Fixed navigation bar
- Hero section with headline
- Feature cards (scrolling marquee)
- "How it Works" carousel
- Call-to-action section
- Footer with copyright

**Key Features:**
- Responsive grid layouts
- Auto-rotating carousel
- Smooth scroll navigation
- Mobile menu toggle

### CodeGenerator.tsx
**Core AI builder** with:
- Prompt input textarea
- Example prompt buttons
- Real-time streaming display
- Code generation with Gemini
- Tab-based code viewer
- Live iframe preview
- Download & copy buttons
- Fullscreen mode
- Chat history sidebar

**Key Features:**
- Streaming response updates
- Error handling
- Session persistence
- Image fallbacks

### ChatHistory.tsx
**Session management** with:
- Scrollable session list
- Delete functionality
- Time formatting
- Session status badge
- Search/filter ready

**Key Features:**
- Relative timestamps ("2h ago")
- Visual indicators
- One-click loading
- Hover delete

---

## 🔌 API Integration

### Google Generative AI (Gemini)

**Endpoint:** `generativeai.googleapis.com`  
**Model:** `gemini-2.5-flash`  
**Method:** Streaming

```typescript
const genAI = new GoogleGenerativeAI(apiKey);
const model = genAI.getGenerativeModel({ model: "gemini-2.5-flash" });
const result = await model.generateContentStream(systemPrompt);

for await (const chunk of result.stream) {
  console.log(chunk.text()); // Real-time response
}
```

### Pexels API

**Endpoint:** `api.pexels.com/v1/search`  
**Method:** GET  
**Rate Limit:** 200 requests/hour (free tier)

```typescript
const res = await fetch(
  `https://api.pexels.com/v1/search?query=${query}&per_page=1`,
  { headers: { Authorization: PEXELS_API_KEY } }
);
const data = await res.json();
const imageURL = data.photos[0].src.large;
```

---

## 📊 State Management

The app uses **React Hooks** for state:

```typescript
// Code generation
const [prompt, setPrompt] = useState('');
const [generatedCode, setGeneratedCode] = useState({ html: '', css: '', js: '' });
const [isGenerating, setIsGenerating] = useState(false);

// Preview
const [showPreview, setShowPreview] = useState(true);
const [activeTab, setActiveTab] = useState('html');
const [isFullscreen, setIsFullscreen] = useState(false);

// Chat history
const [chatSessions, setChatSessions] = useState([]);
const [showChatHistory, setShowChatHistory] = useState(false);

// DOM references
const iframeRef = useRef<HTMLIFrameElement>(null);
const scrollContainerRef = useRef<HTMLDivElement>(null);
```

---

## 💾 localStorage Persistence

Sessions are automatically saved:

```typescript
// Save to localStorage
useEffect(() => {
  if (chatSessions.length > 0) {
    localStorage.setItem('chatSessions', JSON.stringify(chatSessions.slice(0, 10)));
  }
}, [chatSessions]);

// Load from localStorage
useEffect(() => {
  const saved = localStorage.getItem('chatSessions');
  if (saved) {
    setChatSessions(JSON.parse(saved));
  }
}, []);
```

**Limits:**
- Max 10 sessions stored
- ~5-10MB storage limit per domain
- Cleared when browser cache is cleared

---

## 🐛 Error Handling

The app handles multiple error scenarios:

```typescript
// API Key validation
if (!apiKey) {
  setError('Please add your Google Generative AI API key to the .env file.');
}

// Quota exceeded
if (err?.message?.includes('quota') || err?.message?.includes('429')) {
  setError('⚠️ API quota exceeded! Please wait a few minutes...');
}

// Invalid API key
if (err?.message?.includes('API key')) {
  setError('Invalid API key. Please check your VITE_GEMINI_API_KEY...');
}

// Network error
if (err?.message?.includes('network')) {
  setError('Network error. Please check your connection...');
}
```

---

## 🚀 Deployment

### Deploy to Netlify

1. **Build the project**
   ```bash
   npm run build
   ```

2. **Connect to Netlify**
   ```bash
   npm i -g netlify-cli
   netlify deploy --prod
   ```

3. **Set environment variables**
   - Go to Netlify → Site settings → Build & deploy
   - Add `VITE_GEMINI_API_KEY`

### Deploy to Vercel

1. **Push to GitHub**
2. **Connect GitHub repo to Vercel**
3. **Add environment variables**
4. **Deploy** (auto on push)

### Deploy to GitHub Pages

```bash
npm run build
npm i -g gh-pages
gh-pages -d dist
```

---

## 🔐 Security Considerations

⚠️ **Important:** 
- Never commit `.env` with real API keys
- Add API keys to `.gitignore`
- Use environment variable protection on hosting platforms
- Consider backend proxy for production

```gitignore
.env
.env.local
node_modules/
dist/
```

---

## 📝 Contributing

Contributions are welcome! 

1. **Fork the repository**
2. **Create a feature branch** (`git checkout -b feature/AmazingFeature`)
3. **Commit changes** (`git commit -m 'Add some AmazingFeature'`)
4. **Push to branch** (`git push origin feature/AmazingFeature`)
5. **Open a Pull Request**

---

## 🗺️ Roadmap

- [ ] Code editor with syntax highlighting
- [ ] Real-time code editing with live preview
- [ ] Multiple website designs per generation
- [ ] SEO optimization suggestions
- [ ] Cloud sync across devices
- [ ] User authentication
- [ ] Project collaboration
- [ ] Mobile app (React Native)
- [ ] Template library
- [ ] Export to React/Vue/Svelte

---

## 📊 Performance

- **Build Time:** ~2-3 seconds (Vite)
- **First Load:** ~500ms
- **Code Generation:** ~1-2 minutes
- **Preview Render:** Instant (<100ms)
- **Bundle Size:** ~200KB (gzipped)

---

## 🎨 Design System

- **Color Scheme:** Purple & Pink gradients with dark theme
- **Typography:** Bold headlines with readable body text
- **Spacing:** 8px base unit grid
- **Icons:** Lucide React (24px default)
- **Responsive:** Mobile-first with breakpoints at 640px, 1024px

---

## 📚 Learn More

- [React Documentation](https://react.dev/)
- [TypeScript Handbook](https://www.typescriptlang.org/docs/)
- [Vite Guide](https://vitejs.dev/guide/)
- [Tailwind CSS](https://tailwindcss.com/docs)
- [Google Generative AI](https://ai.google.dev/)

---

## 👨‍💻 Author

**Yogesh Goat**  
Built for the future of GenAI and web development.

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- Google Generative AI (Gemini)
- Pexels for free images
- React & TypeScript communities
- Tailwind CSS for styling

---

<div align="center">

**Made with ❤️ by Yogesh Goat**

[⭐ Star this project](https://github.com/yourusername/pagepilot) if you find it helpful!

</div>

# 🚀 Quick Start Guide

## Installation (5 minutes)

```bash
# 1. Clone the repo
git clone https://github.com/yourusername/pagepilot.git
cd pagepilot

# 2. Install dependencies
npm install

# 3. Create .env file
cp .env.example .env

# 4. Add your API keys to .env
# VITE_GEMINI_API_KEY=your_key_here
# VITE_PEXELS_API_KEY=your_key_here

# 5. Start dev server
npm run dev

# 6. Open browser
# http://localhost:5173
```

## Get API Keys

### Google Gemini API
1. Go to [Google AI Studio](https://makersuite.google.com/app/apikey)
2. Click "Create API Key"
3. Copy the key to `.env`

### Pexels API
1. Go to [Pexels API](https://www.pexels.com/api/)
2. Sign up for free account
3. Create API key
4. Copy to `.env`

## Available Commands

```bash
npm run dev      # Start development server
npm run build    # Build for production
npm run preview  # Preview production build
npm run lint     # Run ESLint
```

## Project Tour

### Landing Page (App.tsx)
- Hero section
- Features showcase
- How it works carousel
- Footer

### AI Builder (CodeGenerator.tsx)
- Prompt input
- Code generation
- Live preview
- Code tabs
- Download & copy

### Chat History (ChatHistory.tsx)
- Session management
- Past generations
- Delete sessions

## Key Features to Try

1. **Generate a website** from a text description
2. **View code** in HTML/CSS/JS tabs
3. **Copy code** to clipboard
4. **Download** as HTML file
5. **View fullscreen** preview
6. **Save sessions** to chat history
7. **Load past** projects

## Troubleshooting

**"API key not found"**
- Check `.env` file exists
- Verify `VITE_GEMINI_API_KEY` is set
- Restart dev server

**"Preview not loading"**
- Check browser console for errors
- Verify Gemini API quota
- Try with different prompt

**"localStorage full"**
- Old sessions limit is 10
- Delete old sessions to free space
- Clear browser cache if needed

## Need Help?

- 📖 [Read README](README.md)
- 🤔 [Check FAQ](docs/FAQ.md)
- 💬 [Open an issue](https://github.com/yourusername/pagepilot/issues)

---

Happy building! 🎉

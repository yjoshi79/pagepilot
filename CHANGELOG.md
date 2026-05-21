# Changelog

All notable changes to PagePilot will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0] - 2026-05-21

### Added
- ✨ **AI-Powered Code Generation** — Generate websites from text descriptions using Gemini AI
- 🎯 **Live Preview** — Real-time iframe preview of generated code
- 💾 **Chat History** — Save and manage up to 10 past generations
- 📋 **Code Tabs** — View HTML, CSS, and JavaScript separately
- ⬇️ **Download HTML** — Export as single HTML file
- 📋 **Copy Code** — One-click copy to clipboard
- 🖼️ **Image Integration** — Pexels API for auto-fetching relevant images
- 🎨 **Responsive Design** — Mobile-first design with Tailwind CSS
- 🎬 **Fullscreen Preview** — Expand preview to full viewport
- 🌙 **Dark Theme** — Beautiful UI with purple & pink gradients
- 📱 **Mobile Navigation** — Hamburger menu for mobile devices
- 🎡 **How It Works Carousel** — 3-step feature showcase
- ⚡ **Fast Build** — Vite bundler for quick development

### Features
- Real-time streaming response from AI
- Error handling for API quotas and invalid keys
- Image fallback system for broken URLs
- localStorage persistence
- Example prompts for quick testing
- Code syntax highlighting in tabs
- Smooth animations and transitions
- Accessibility-friendly UI

### Tech Stack
- React 18
- TypeScript
- Vite
- Tailwind CSS
- Google Generative AI (Gemini 2.5 Flash)
- Pexels API
- Lucide React Icons

### Documentation
- Comprehensive README
- Quick Start Guide
- Contributing Guidelines
- Issue Templates
- MIT License

---

## Planned Features (Roadmap)

### [1.1.0] - Code Editor
- [ ] Real-time code editor
- [ ] Syntax highlighting (Prism.js)
- [ ] Live preview while editing
- [ ] Auto-complete suggestions
- [ ] Code formatting

### [1.2.0] - Enhanced History
- [ ] Search/filter chat history
- [ ] Export sessions as JSON
- [ ] Import sessions
- [ ] Rename custom titles
- [ ] Tags/categories

### [1.3.0] - Cloud Features
- [ ] User authentication
- [ ] Cloud sync across devices
- [ ] Auto-backup
- [ ] Export to GitHub Gist
- [ ] Share project links

### [1.4.0] - Advanced Generation
- [ ] Multiple design options
- [ ] Template library
- [ ] Component marketplace
- [ ] Custom system prompts
- [ ] Generate variations

### [2.0.0] - Platform Expansion
- [ ] Mobile app (React Native)
- [ ] VS Code Extension
- [ ] CLI tool
- [ ] API for third-party integration
- [ ] Collaborative editing

---

## Known Issues

- API calls limited by Gemini quota
- localStorage cleared when browser cache is cleared
- No cross-device sync (frontend only)
- Pexels API key hardcoded (security concern for production)

---

## Fixed in Previous Versions

### Security
- ✅ Removed "ChatBot India" button
- ✅ Added .env.example for API key guidance

### UI/UX
- ✅ Removed duplicate code generation button
- ✅ Improved error messages
- ✅ Better mobile responsiveness

---

## Contributors

- 👨‍💻 **Yogesh Goat** — Founder & Lead Developer

---

## Migration Guide

### From v0.9.0 to v1.0.0

No breaking changes. All localStorage sessions are compatible.

---

## How to Report Bugs

1. Check existing [GitHub Issues](https://github.com/yourusername/pagepilot/issues)
2. Create new issue with:
   - Clear title
   - Detailed description
   - Steps to reproduce
   - Expected vs actual behavior
   - Environment info (OS, browser, node version)

---

## Support

- 📖 [Documentation](README.md)
- 🚀 [Quick Start](QUICKSTART.md)
- 🤝 [Contributing](CONTRIBUTING.md)
- 💬 [GitHub Discussions](https://github.com/yourusername/pagepilot/discussions)

---

**Made with ❤️ for the future of GenAI and web development**

# Frequently Asked Questions (FAQ)

## 🤔 General Questions

### Q: What is PagePilot?
**A:** PagePilot is an AI-powered website builder that generates clean, production-ready HTML, CSS, and JavaScript code from plain English descriptions.

### Q: Is PagePilot free?
**A:** PagePilot itself is free (open-source MIT license). You need your own free API keys:
- Google Generative AI (free tier available)
- Pexels API (free tier available)

### Q: Can I use it commercially?
**A:** Yes! MIT license allows commercial use. Just include attribution.

### Q: Do I need coding experience?
**A:** No! Just describe what you want in plain English.

---

## 🚀 Getting Started

### Q: How do I get started?
**A:** 
1. Clone the repo
2. Run `npm install`
3. Create `.env` with API keys
4. Run `npm run dev`
5. Open http://localhost:5173

### Q: Where do I get API keys?
**A:** 
- **Gemini:** https://makersuite.google.com/app/apikey
- **Pexels:** https://www.pexels.com/api/

### Q: What if I don't have API keys yet?
**A:** You'll get an error message. Follow the instructions in the error to create free API keys.

---

## 💻 Development

### Q: How do I run the development server?
**A:**
```bash
npm run dev
```

### Q: How do I build for production?
**A:**
```bash
npm run build
```

### Q: How do I check for errors?
**A:**
```bash
npm run lint
```

### Q: What Node version do I need?
**A:** Node.js v16 or higher (v18+ recommended)

---

## 🎯 Features

### Q: How long does code generation take?
**A:** Typically 1-2 minutes depending on:
- Code complexity
- API response time
- Network speed

### Q: Can I edit the generated code?
**A:** 
- Currently: View only (read-only display)
- Future: Add real-time code editor

### Q: How many websites can I generate?
**A:** Limited by API quotas. Gemini free tier has generous limits (~100 generations/month)

### Q: Can I download the code?
**A:** Yes! Click download button to get single HTML file.

### Q: How many sessions can I save?
**A:** Maximum 10 (to keep localStorage manageable)

### Q: Can I export all my sessions?
**A:** Not yet, but you can:
1. Download individual HTML files
2. Copy code from tabs
3. Save to cloud storage

---

## 🖥️ Deployment

### Q: Can I deploy generated websites?
**A:** Yes! Upload the downloaded HTML file to:
- Netlify
- Vercel
- GitHub Pages
- Any static hosting

### Q: How do I deploy PagePilot itself?
**A:** Deploy to:
- Netlify (recommended)
- Vercel
- GitHub Pages
- Any static host

### Q: Do I need a backend?
**A:** No! PagePilot is frontend-only.

### Q: How do I set environment variables on production?
**A:**
- **Netlify:** Site settings → Build & deploy → Environment
- **Vercel:** Project settings → Environment Variables

---

## 🐛 Troubleshooting

### Q: "API key not found" error
**A:**
1. Check `.env` file exists
2. Verify `VITE_GEMINI_API_KEY` is set
3. Restart dev server
4. Check key is valid

### Q: Preview not loading
**A:**
1. Check browser console for errors (F12)
2. Verify API quota isn't exceeded
3. Check internet connection
4. Try different prompt

### Q: Code generation is slow
**A:**
- Normal for complex requests (up to 2 min)
- Check internet connection
- Try simpler prompt
- Check API quota

### Q: Sessions not saving
**A:**
1. Check browser localStorage isn't full
2. Try clearing some old sessions
3. Check browser privacy settings
4. Try different browser

### Q: Downloaded HTML doesn't work
**A:**
1. Open in browser (double-click)
2. Check image URLs are correct
3. Try uploading to server
4. Check console for JavaScript errors

### Q: Mobile preview looks weird
**A:**
1. Zoom to 100% (Cmd/Ctrl + 0)
2. Try fullscreen preview
3. Refresh page (Cmd/Ctrl + R)
4. Check responsive design

---

## 🔐 Security

### Q: Is my API key secure?
**A:** 
- Frontend only: Keep key safe, never commit to git
- Use .gitignore to exclude .env
- For production: Use backend proxy

### Q: Is my generated code safe?
**A:** Code comes from Google Gemini AI. Always review before deploying.

### Q: Are my sessions backed up?
**A:** Only locally in browser (localStorage). Not synced to cloud.

### Q: What happens if I clear browser cache?
**A:** All localStorage data is deleted. Save important projects!

---

## 🎨 Customization

### Q: Can I change the UI theme?
**A:** Not in UI yet, but you can:
1. Edit `tailwind.config.js`
2. Modify colors in CSS
3. Fork and customize

### Q: Can I add custom CSS?
**A:** Generated HTML has its own CSS. For global styles:
1. Edit `src/index.css`
2. Modify Tailwind config

### Q: Can I remove branding?
**A:** Yes, it's open-source! Modify as needed.

---

## 🤝 Contributing

### Q: How can I contribute?
**A:** 
1. Fork repo
2. Create feature branch
3. Make changes
4. Submit PR

See [CONTRIBUTING.md](CONTRIBUTING.md) for details.

### Q: What are good first contributions?
**A:**
- Fix typos in docs
- Add example prompts
- Improve error messages
- Add comments to code

### Q: Can I suggest features?
**A:** Yes! Open GitHub issue with:
- Feature description
- Use case
- Expected behavior

---

## 📊 Performance

### Q: How big is the app?
**A:** ~200KB gzipped (very lightweight)

### Q: How fast is it?
**A:**
- Load: ~500ms
- Preview: ~100ms
- Generation: 1-2 min (API dependent)

### Q: Does it work offline?
**A:** No, needs internet for Gemini API

### Q: Does it work on mobile?
**A:** Yes, responsive design works on all devices

---

## 💡 Tips & Tricks

### Q: How do I get better code?
**A:** 
- Be specific: "modern dark theme" vs "nice design"
- Include layout details: "hero section, features, footer"
- Mention frameworks: "HTML + vanilla JS"
- Add styling: "purple and white colors"

### Q: Example of good prompt:
```
Create a modern SaaS landing page with:
- Dark purple hero section with gradient
- Animated features section with 6 cards
- Pricing table with 3 tiers
- CTA button and footer
- Mobile responsive
```

### Q: How do I test the generated code?
**A:**
1. View in preview
2. Check on mobile
3. Download and test locally
4. Deploy to test server

### Q: Can I combine multiple generations?
**A:** Yes, copy/paste code from multiple sessions

---

## 🚀 Advanced

### Q: Can I modify the system prompt?
**A:** Not in UI, but you can:
1. Fork the repo
2. Edit `generateCode()` function
3. Modify system prompt in CodeGenerator.tsx

### Q: Can I use different AI model?
**A:** Yes! Edit:
```typescript
const model = genAI.getGenerativeModel({ model: "your-model" });
```

### Q: Can I integrate with other services?
**A:** Yes! Open a discussion or PR with your idea.

---

## 📞 Still Need Help?

- 📖 [Read README](README.md)
- 🚀 [Quick Start](QUICKSTART.md)
- 🤝 [Contributing Guide](CONTRIBUTING.md)
- 💬 [Open GitHub Issue](https://github.com/yourusername/pagepilot/issues)

---

**Last Updated:** May 21, 2026  
**Version:** 1.0.0


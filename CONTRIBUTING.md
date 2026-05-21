# Contributing to PagePilot

Thank you for your interest in contributing to PagePilot! 🎉

We welcome all types of contributions: bug reports, feature requests, documentation improvements, and code contributions.

## 📋 Guidelines

### Getting Started

1. **Fork the repository**
   ```bash
   git clone https://github.com/yourusername/pagepilot.git
   cd pagepilot
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Create a feature branch**
   ```bash
   git checkout -b feature/YourFeatureName
   ```

4. **Start development server**
   ```bash
   npm run dev
   ```

### Before You Commit

1. **Run linter**
   ```bash
   npm run lint
   ```

2. **Test your changes**
   - Test in multiple browsers (Chrome, Firefox, Safari)
   - Test on mobile (responsive design)
   - Verify localStorage works

3. **Follow code style**
   - Use TypeScript for all code
   - Follow existing naming conventions
   - Keep components small and focused
   - Add comments for complex logic

### Commit Messages

Use clear, descriptive commit messages:

```bash
# Good ✅
git commit -m "feat: Add code editor with syntax highlighting"
git commit -m "fix: Handle API quota exceeded error gracefully"
git commit -m "docs: Update README with deployment guide"
git commit -m "refactor: Simplify preview update logic"

# Avoid ❌
git commit -m "fix stuff"
git commit -m "wip"
git commit -m "asdf"
```

**Commit types:**
- `feat:` - New feature
- `fix:` - Bug fix
- `docs:` - Documentation
- `refactor:` - Code refactor
- `style:` - Formatting
- `test:` - Tests
- `chore:` - Dependencies, config

### Pull Request Process

1. **Update documentation** if needed
2. **Add descriptive PR title** (e.g., "Add real-time code editing")
3. **Provide description** of changes
4. **Reference related issues** (e.g., "Fixes #123")
5. **Wait for review** and address feedback

**PR Template:**
```markdown
## Description
Brief description of changes

## Type of Change
- [ ] Bug fix
- [ ] New feature
- [ ] Documentation update
- [ ] Refactoring

## Testing
How to test this change?

## Screenshots (if applicable)
Before/after screenshots

## Checklist
- [ ] Code follows project style
- [ ] Tests pass
- [ ] No console errors
- [ ] Documentation updated
```

### Feature Ideas

Looking for ideas? Check these areas:

**Easy (Good for Beginners)**
- [ ] Add keyboard shortcuts
- [ ] Improve error messages
- [ ] Add more example prompts
- [ ] Improve mobile responsiveness
- [ ] Add loading animations

**Medium**
- [ ] Code editor with syntax highlighting
- [ ] Search/filter chat history
- [ ] Session export as JSON
- [ ] Code preview side-by-side mode

**Hard**
- [ ] Real-time code editing
- [ ] Cloud sync with Firebase
- [ ] User authentication
- [ ] Collaborative editing

### Bug Reports

Found a bug? Please report it! Include:

1. **Description:** What's the problem?
2. **Steps to reproduce:** How to trigger the bug?
3. **Expected behavior:** What should happen?
4. **Actual behavior:** What actually happened?
5. **Environment:** OS, browser, Node version
6. **Screenshots:** If applicable

**Example:**
```
Title: Preview doesn't update when copying HTML to clipboard

Description:
After generating a website and copying the HTML code, the preview doesn't refresh.

Steps to reproduce:
1. Generate a website
2. Click the copy button on HTML tab
3. Observe preview

Expected:
Preview should show the generated website

Actual:
Preview remains blank

Environment:
- OS: macOS 13.2
- Browser: Chrome 120.0
- Node: v18.17.0
```

## 🏗️ Development Setup

### Environment Variables

Create `.env`:
```env
VITE_GEMINI_API_KEY=your_key_here
VITE_PEXELS_API_KEY=your_key_here
```

### Project Structure

```
src/
├── App.tsx                # Main landing page
├── components/
│   ├── CodeGenerator.tsx   # AI builder (main feature)
│   └── ChatHistory.tsx     # History sidebar
└── main.tsx               # Entry point
```

### Testing

```bash
# Build
npm run build

# Preview production build
npm run preview

# Lint
npm run lint
```

## 📚 Code Style Guide

### TypeScript

```typescript
// ✅ Good
interface User {
  id: string;
  name: string;
  email: string;
}

const handleClick = (userId: string): void => {
  // Implementation
};

// ❌ Avoid
interface User {
  id,
  name,
  email
}

const handleClick = (userId) => {
  // No types
};
```

### React Components

```typescript
// ✅ Good
export const MyComponent: React.FC<MyProps> = ({ prop1, prop2 }) => {
  const [state, setState] = useState('');

  useEffect(() => {
    // Side effect
  }, [state]);

  return <div>{state}</div>;
};

// ❌ Avoid
export const MyComponent = (props) => {
  return <div>{props.name}</div>;
};
```

### CSS (Tailwind)

```tsx
// ✅ Good
<button className="bg-purple-500 hover:bg-purple-600 text-white px-4 py-2 rounded-lg transition-colors">
  Click me
</button>

// ❌ Avoid
<button style={{ background: 'purple', padding: '10px' }}>
  Click me
</button>
```

## 🤝 Community

- **Questions?** Open a discussion on GitHub
- **Chat?** Check out our Discord community
- **Need help?** Tag maintainers in issues

## ✨ Thank You

Your contributions make PagePilot better! Every PR, issue, and idea helps.

**Contributors:**
- 🙏 Yogesh Goat (Founder)

---

Happy coding! 🚀

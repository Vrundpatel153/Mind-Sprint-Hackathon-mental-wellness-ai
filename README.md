# MindMate Chatbot Frontend

A complete, production-ready mental health companion built with React, TypeScript, and Tailwind CSS. Features AI-powered conversations, guided wellness exercises, mood tracking, and personal insights.
### VIDEO LINK
https://drive.google.com/drive/folders/1YOUqBGvC3bJ2PnqZY5x2YrOwoQIk5F-T?usp=sharing

## 🚀 Quick Start

### Demo Login
- **Email:** `demo@mindmate.test`
- **Password:** `Password123!`

### Installation & Setup

```bash
# Clone the repository
git clone <repository-url>
cd mindmate-chatbot-frontend

# Install dependencies
npm install

# Start development server
npm run dev
```

The app will be available at `http://localhost:8080`

## 🌟 Features

### Core Features
- **Daily Check-ins** - Conversational mood tracking with adaptive questions
- **AI Chat Support** - Empathetic AI companion with crisis detection
- **Guided Exercises** - Breathing, meditation, and mindfulness exercises
- **Mood Journal** - Personal reflection space with tagging and search
- **Progress Insights** - Visual analytics and AI-generated insights
- **Crisis Support** - Immediate help resources and calming exercises

### Technical Features
- **Mock Service Worker** - Fully functional offline-first experience
- **LocalStorage Persistence** - Data survives page refreshes
- **Responsive Design** - Mobile-first, works on all devices
- **Accessibility** - WCAG compliant, keyboard navigation
- **Theme Support** - Light/dark mode with system preference detection
- **PWA Ready** - Installable with offline support

## 🏗️ Architecture

### Tech Stack
- **Frontend:** React 18, TypeScript, Tailwind CSS
- **Routing:** React Router v6
- **State:** React Context + Local State
- **Animations:** Framer Motion
- **Charts:** Custom SVG components
- **API Mocking:** MSW (Mock Service Worker)
- **Build:** Vite

### Project Structure
```
src/
├── components/          # Reusable UI components
│   ├── auth/           # Authentication components
│   ├── charts/         # Chart components
│   ├── exercises/      # Exercise player components
│   └── ui/             # shadcn/ui components
├── contexts/           # React contexts (Auth, Theme)
├── hooks/              # Custom React hooks
├── mocks/              # MSW handlers and seed data
├── pages/              # Page components
└── lib/                # Utilities and helpers
```

## 🎯 Demo Features

### Seeded Demo Data
- User profile with 7-day streak
- 5 recent check-ins with varying moods
- 6 wellness exercises (breathing, meditation, etc.)
- 4 journal entries
- 2 AI chat conversation threads
- Mood analytics and insights

### Demo Tools (Hidden Features)
Access demo tools at `/demo-tools` for:
- Data seeding and reset
- Crisis flow simulation
- Export sample JSON data
- Device preview modes

## 🔧 Configuration

### Environment Variables (Optional)
```bash
NEXT_PUBLIC_OPENAI_KEY=your_openai_key  # Optional: For enhanced AI responses
```

### Customization
- **Colors:** Edit `src/index.css` for theme colors
- **Data:** Modify `src/mocks/seed.ts` for different demo data
- **API:** Replace MSW handlers with real API calls in production

## 🧪 Testing

```bash
# Run tests
npm test

# Run tests with coverage
npm run test:coverage

# Run e2e tests (if configured)
npm run test:e2e
```

## 📦 Build & Deploy

```bash
# Build for production
npm run build

# Preview production build
npm run preview

# Deploy to Vercel (one-click)
# Connect your GitHub repo to Vercel for automatic deployments
```

## 🔒 Privacy & Security

### Demo Environment
- All data stored in browser's localStorage
- No real personal data transmitted
- MSW intercepts all API calls locally

### Production Considerations
- Replace localStorage with secure backend
- Implement proper authentication
- Add encryption for sensitive data
- Follow HIPAA guidelines for health data

## 🆘 Crisis Support Resources

The app includes built-in crisis detection and support resources:

- **Crisis Text Line:** Text HOME to 741741
- **National Suicide Prevention Lifeline:** 988
- **Emergency Services:** 911

## 🎨 Design System

### Color Palette
- **Primary:** `#4C7BF3` (Calming blue)
- **Accent:** `#7AE7C7` (Soothing mint)
- **Secondary:** `#9AA6FF` (Soft periwinkle)
- **Background:** `#F6F8FB` (Light neutral)

### Typography
- **Font:** Inter (Google Fonts)
- **Scale:** Harmonious type scale for readability

## 🚀 Deployment Options

### Vercel (Recommended)
1. Connect GitHub repo to Vercel
2. Auto-deploys on push to main
3. Preview deployments for PRs

### Other Platforms
- Netlify
- GitHub Pages
- AWS S3 + CloudFront
- Docker container

## 🔄 Replacing Mock API

To connect to a real backend:

1. Remove MSW initialization in `src/App.tsx`
2. Update API endpoints in components
3. Add authentication middleware
4. Implement proper error handling

## 📝 License

MIT License - see LICENSE file for details.

## 🤝 Contributing

1. Fork the repository
2. Create feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open Pull Request

## 📞 Support

For questions about this demo:
- Open an issue on GitHub
- Contact: vrundpatel153@gmail.com

---


**Important:** This is a demonstration app. For real mental health support, please consult qualified professionals.


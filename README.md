# 🤖 AI Policy Compliance Checker
**with CrewAI Multi-Agent System**

🌐 **See the Live Application**: [https://ai-policy-compliance-checker.vercel.app/](https://ai-policy-compliance-checker.vercel.app/)

> **Transform opaque policies into clear, AI-audited compliance reports. Use multi-agent CrewAI systems with RAG over internal documents to surface risks, missing controls, and actionable remediation plans—instantly and accurately.** ⚡

---

## ✨ Features

### 🎯 **Core Functionality**
- 🤖 **Multi-Agent Analysis** - Three specialized CrewAI agents work together:
  - **Auditor Agent**: Identifies compliance gaps and risk areas with severity assessment (Critical, High, Medium, Low)
  - **Researcher Agent**: Retrieves relevant policy documents using RAG (Retrieval-Augmented Generation) with semantic search
  - **Editor Agent**: Compiles findings into structured, executive-ready compliance reports
- 🔍 **RAG-Powered Document Search** - Semantic search over internal policy documents with full citations
- 📊 **Structured Compliance Reports** - Findings grouped by severity with actionable recommendations
- 📝 **Evidence Tracking** - Complete citation support with document IDs, paths, and content snippets
- 🔬 **Agent Transparency** - View execution traces for each agent's reasoning process
- 🎚️ **Multiple Analysis Modes** - Question answering, policy review, and standard compliance checks

### 🎨 **Beautiful UI/UX**
- ✨ **Modern 2025 Design** - Glassmorphic effects, video backgrounds, micro-animations
- 🌙 **Dark Mode** - Full theme support with smooth transitions (light mode default)
- 📱 **Fully Responsive** - Optimized for desktop, tablet, and mobile (360px - 1440px+)
- ♿ **Accessible** - WCAG AA compliant with keyboard navigation and screen reader support
- 🎯 **Intuitive Interface** - Clean, user-friendly design with clear visual hierarchy
- 📱 **Mobile Optimized** - Bottom navigation, collapsible panels, touch-friendly targets (44px minimum)

### 📊 **Dashboard Features**
- 📈 **Real-Time Statistics** - Total jobs, completed jobs, open risks, critical risks from Supabase
- 📝 **Job History** - Latest compliance checks with status, severity badges, and timestamps
- 🔍 **Direct Supabase Connection** - Real data from database, no mock data
- 📊 **Loading States** - Smooth skeletons and progress indicators
- ⚠️ **Error Handling** - Graceful error messages with configuration guidance

### 🚀 **Advanced Features**
- 📋 **Copy Report to Clipboard** - One-click copy with formatted content and toast notifications
- 🎬 **Real-Time Agent Activity** - Animated indicator showing which CrewAI agent is currently active
- 📚 **Job History (LocalStorage)** - Client-side persistence to view and reload past compliance checks
- 💾 **Export Report as Markdown** - Download formatted reports as `.md` files
- ⚡ **Quick Action Templates** - Pre-filled compliance queries to speed up workflow
- 🔍 **Interactive Report Viewer** - Search functionality with highlighting and expandable/collapsible sections
- ⌨️ **Typing Indicator Animation** - Character-by-character animation for assistant messages
- 🎉 **Success Celebration Animations** - Confetti animations when jobs complete successfully
- 🔗 **Report Sharing via URL** - Generate shareable URLs for compliance reports (30-day expiration)
- 🔄 **Report Comparison View** - Side-by-side comparison of two reports with difference highlighting

---

## 🏗️ Tech Stack

### **Backend** 🐍
- **FastAPI** - Modern Python web framework for REST API
- **CrewAI 1.6.1** - Multi-agent orchestration framework
- **OpenAI API** - GPT-4.1-mini for LLM and text-embedding-3-small for embeddings
- **Python 3.11+** - Latest features and performance

### **Frontend** ⚛️
- **Next.js 15** - React 19.2 with App Router
- **TypeScript** - Full type safety throughout
- **Tailwind CSS** - Utility-first styling with custom design system
- **shadcn/ui** - Beautiful, accessible component library
- **Lucide Icons** - Modern icon set
- **next-themes** - Theme management with persistence

### **Database & Cache** 💾
- **Supabase** - PostgreSQL with pgvector for vector similarity search
- **Upstash Redis** - Serverless caching and ephemeral job state
- **Row Level Security (RLS)** - Secure data access policies

### **Deployment** 🚀
- **Railway** - Backend API service deployment
- **Vercel** - Frontend web service deployment
- **Monorepo Structure** - Single repository with `/api` and `/web` directories

---

## 📸 Screenshots

### 🏠 Landing Page
![Landing Page Light Mode](./web/public/Screenshot-light.jpg)
*Modern landing page with video background and glassmorphic hero section (light mode)*

![Landing Page Dark Mode](./web/public/Screenshot-dark.jpg)
*Dark mode variant with enhanced readability overlays*

### 🎮 Playground
*Interactive compliance check interface with two-column layout (conversation + report), real-time agent activity, and comprehensive report viewer*

### 📊 Dashboard
*Compliance jobs dashboard with real-time statistics from Supabase, job history, and severity indicators*

---

## 📖 User Guide

### 🎮 Using the Playground

1. **Navigate to Playground**
   - Click "Playground" in navigation or "Launch compliance console" on homepage
   - You'll see a two-column interface (conversation on left, report on right)

2. **Select Analysis Mode**
   - **Question Mode**: Ask natural-language compliance questions
   - **Policy Review Mode**: Comprehensive policy document review
   - **Standard Check Mode**: Evaluate against compliance frameworks (ISO 27001, GDPR, SOC 2, etc.)

3. **Enter Your Query**
   - Type your compliance question or paste policy text to review
   - Use **Quick Action Templates** for common compliance queries (GDPR, ISO 27001, etc.)
   - Or write a custom question

4. **Run Compliance Check**
   - Click "Run Compliance Check" button
   - Watch real-time agent activity as Auditor, Researcher, and Editor work
   - View progress as job status updates (queued → running → done)

5. **View Results**
   - **Summary Tab**: Executive summary of compliance findings
   - **Findings Tab**: Findings grouped by severity (Critical, High, Medium, Low)
   - **Evidence Tab**: All citations with document IDs and paths
   - **Agent Traces Tab**: Detailed reasoning from each agent

6. **Interact with Report**
   - **Search**: Use search bar to find specific content (with highlighting)
   - **Expand/Collapse**: Click sections to expand or collapse details
   - **Copy Report**: Click "Copy Report" to copy formatted content to clipboard
   - **Export Markdown**: Click "Export Markdown" to download report as `.md` file
   - **Share Report**: Click "Share Report" to generate a shareable URL (30-day expiration)

### 📊 Using the Dashboard

1. **Navigate to Dashboard**
   - Click "Dashboard" in navigation
   - View real-time statistics from Supabase

2. **View Statistics**
   - **Total Jobs**: Count of all compliance checks
   - **Completed Jobs**: Successfully finished checks
   - **Open Risks**: Total findings across all jobs
   - **Critical Risks**: Critical severity findings count

3. **Browse Job History**
   - View latest 20 compliance jobs
   - See job input, status, timestamp, and severity
   - Click arrow icon to view full job in playground

4. **Filter & Search** *(Coming Soon)*
   - Filter by project, status, or date
   - Search job history
   - Export compliance reports

### 🎨 Customization

#### Theme Options
- ☀️ **Light Mode** - Clean, bright interface (default)
- 🌙 **Dark Mode** - Easy on the eyes with enhanced readability
- 🖥️ **System** - Automatically follows OS preference

#### Mobile Experience
- 📱 **Bottom Navigation** - Quick access to main pages on mobile
- 🍔 **Hamburger Menu** - Top navigation menu for mobile devices
- 📄 **Collapsible Panels** - Report panel can be hidden on mobile for better focus
- 📱 **Job History Drawer** - Bottom sheet drawer for accessing job history on mobile

---


---

## 🛣️ Roadmap

### Current (MVP) ✅
- ✅ Multi-agent CrewAI orchestration
- ✅ RAG document retrieval
- ✅ Structured compliance reports
- ✅ Playground UI with real-time agent activity
- ✅ Dashboard with direct Supabase connection
- ✅ Job tracking and history
- ✅ 10 enhancement features (copy, export, share, compare, etc.)

### Planned
- 📝 Document ingestion UI/CLI
- 🔍 Enhanced dashboard with filters and search
- ⚡ Rate limiting implementation
- 📊 Agent trace visualization improvements
- 👥 Multi-tenant RBAC support
- 🌐 Multi-language support

### Known Limitations

- Document ingestion currently requires manual setup (CLI or direct API calls)
- Rate limiting is stubbed (needs Redis implementation)
- Agent trace extraction is basic (needs CrewAI result parsing enhancement)
- No user authentication yet (projectId is placeholder)
- Structured output parsing (findings/citations extraction) is placeholder

---


## 👨‍💻 Creator

**Created by Derril Filemon**

- 🌐 **GitHub**: [@derril-tech](https://github.com/derril-tech)
- 💼 **LinkedIn**: [Your LinkedIn Profile]
- 📧 **Email**: [Your Email]

---

## 🙏 Acknowledgments

- **CrewAI** - For the multi-agent orchestration framework
- **OpenAI** - For GPT-4.1-mini and embedding models
- **Supabase** - For PostgreSQL database with pgvector support
- **Upstash** - For serverless Redis caching
- **Railway** - For backend deployment platform
- **Vercel** - For frontend deployment platform
- **shadcn/ui** - For beautiful, accessible components
- **Next.js** - For the amazing React framework
- **Tailwind CSS** - For utility-first styling

---

## 📞 Support

- 🐛 **Issues**: [GitHub Issues](https://github.com/derril-tech/ai-policy-compliance-checker/issues)
- 💬 **Discussions**: [GitHub Discussions](https://github.com/derril-tech/ai-policy-compliance-checker/discussions)
- 📧 **Email**: [Your Support Email]

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

<div align="center">



Made with ❤️ and ☕ by [Derril Filemon](https://github.com/derril-tech)

</div>

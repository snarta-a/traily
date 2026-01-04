# Traily - Research Knowledge Graph Chrome Extension

Traily is a powerful Chrome extension that automatically captures, processes, and visualizes your browsing data as an interactive knowledge graph using Google Gemini 2.0 Flash API.

## ✨ Features

### Core Features
- **Automatic Content Capture**: Intelligently captures relevant web content as you browse
- **AI-Powered Analysis**: Uses Google Gemini 2.0 Flash API to extract key concepts and relationships
- **Interactive Knowledge Graph**: Visualize your research as an interconnected graph using ReactFlow
- **Accurate Visit Tracking**: Perfect tracking of page visits with detailed statistics
- **Modern Light Mode UI**: Professional, clean design optimized for productivity

### New Features
- **🤖 AI Chat Interface**: Chat with your browsing context - ask questions about your research, find connections, and explore topics conversationally
- **👁️ Live Preview**: View websites directly in the extension with an integrated live preview panel
- **📊 Enhanced Statistics**: Real-time stats showing total pages, visits, and unique domains
- **🎨 Modern Design**: Completely revamped UI with clean light mode theme
- **🔐 Environment Variables**: Secure API key management using .env files

### Advanced Features
- **Semantic Search**: Find content using natural language queries
- **Smart Filtering**: Advanced filtering by content type, date, domain, and more
- **Visit Counter**: See exactly how many times you've visited each page
- **Concept Extraction**: AI-powered extraction of key concepts from every page
- **Relationship Mapping**: Automatic detection of connections between pages based on shared concepts
- **Local-First Storage**: All data stored locally in Chrome extension storage
- **Privacy-Focused**: Only processes content you explicitly visit

## 🛠 Technology Stack

- **Frontend**: React 18 with TypeScript
- **Graph Visualization**: ReactFlow
- **AI Processing**: Google Gemini 2.0 Flash Exp API
- **Storage**: Chrome Extension Storage API
- **Styling**: Tailwind CSS
- **Build Tool**: Webpack 5
- **Environment**: dotenv-webpack for secure configuration
- **Manifest**: Chrome Extension Manifest V3

## 📦 Installation

### Development Setup

1. **Clone the repository**:
   ```bash
   git clone <repository-url>
   cd traily-chrome-extension
   ```

2. **Install dependencies**:
   ```bash
   npm install
   ```

3. **Configure API Key**:
   - Copy `.env.example` to `.env`
   ```bash
   cp .env.example .env
   ```
   - Add your Gemini API key to `.env`:
   ```
   GEMINI_API_KEY=your_api_key_here
   ```
   - Get a free API key from [Google AI Studio](https://makersuite.google.com/app/apikey)

4. **Build the extension**:
   ```bash
   npm run build
   ```

5. **Load in Chrome**:
   - Open Chrome and navigate to `chrome://extensions/`
   - Enable "Developer mode" in the top right
   - Click "Load unpacked" and select the `dist` folder

### Production Build

```bash
npm run build
```

## ⚙️ Configuration

### Environment Variables

Create a `.env` file in the root directory:

```env
# Google Gemini API Key
GEMINI_API_KEY=your_api_key_here

# Optional: Custom API endpoint
GEMINI_API_ENDPOINT=https://generativelanguage.googleapis.com/v1beta/models/gemini-2.0-flash-exp:generateContent
```

### Google Gemini API Key

1. Get a free API key from [Google AI Studio](https://makersuite.google.com/app/apikey)
2. Add it to your `.env` file
3. Rebuild the extension: `npm run build`
4. Alternatively, set it in the extension settings (opens in popup)

### Settings

Configure in the extension popup:
- **Auto-capture**: Toggle automatic page analysis
- **Minimum content length**: Set threshold for content capture
- **Skip domains**: Configure domains to ignore
- **Capture frequency**: Adjust processing intervals

## 🚀 Usage

### Getting Started

1. **Install and configure** the extension with your Gemini API key in `.env`
2. **Browse the web** - Traily automatically captures relevant content
3. **Open the side panel** by clicking the extension icon
4. **Explore your knowledge graph** and see connections between pages

📖 **See [QUICK_START.md](QUICK_START.md) for detailed usage guide**

### Knowledge Graph Tab

- **View Interactive Graph**: See all your browsing as connected nodes
- **Click Nodes**: View details including:
  - Page title and URL
  - Visit count
  - Extracted concepts
  - Related pages
- **Live Preview**: Click "Open Live Preview" on any node to see the page

### Chat Tab

Ask questions about your research:
- "What topics have I been researching?"
- "Find pages about machine learning"
- "Show me connections between my recent visits"
- "Summarize what I learned about TypeScript"

The AI chat has full context of your browsing history and can help you:
- Find connections between topics
- Summarize your research
- Discover patterns in your browsing
- Answer questions about specific pages

### Live Preview Tab

- Opens automatically when you click on a node
- View pages without leaving the extension
- Respects X-Frame-Options (some sites can't be embedded)
- Quick "Open in New Tab" option for unsupported sites

## 📁 Project Structure

```
src/
├── background/          # Background service worker
│   └── background.ts    # Main background script with visit tracking
├── content/             # Content scripts
│   └── content.ts       # Page content extraction
├── popup/               # Extension popup
│   ├── popup.html       # Popup HTML
│   ├── popup.tsx        # Popup entry point
│   └── PopupApp.tsx     # Main popup component
├── sidepanel/           # Side panel interface
│   ├── sidepanel.html   # Side panel HTML
│   ├── sidepanel.tsx    # Side panel entry point
│   └── ModernSidePanel.tsx # Main side panel with tabs
├── components/          # Shared React components
│   ├── SearchInterface.tsx   # Modern search bar
│   ├── ChatInterface.tsx     # AI chat component
│   ├── LivePreview.tsx       # Live preview component
│   ├── NodeDetailPanel.tsx   # Node details
│   └── KnowledgeGraphSidebar.tsx # Graph sidebar
├── services/            # Core services
│   ├── geminiProcessor.ts    # Gemini API with chat
│   ├── storageManager.ts     # Storage with visit tracking
│   └── contentProcessor.ts   # Content processing utilities
├── config/              # Configuration
│   └── configManager.ts      # Config with .env support
├── styles/              # CSS styles
│   └── globals.css      # Modern light theme styles
├── types/               # TypeScript type definitions
│   └── index.ts         # Common interfaces
└── manifest.json        # Chrome extension manifest
```

## 🎨 UI Features

### Modern Light Mode Design
- Clean, professional color scheme
- Smooth animations and transitions
- Optimized for productivity
- Consistent design language throughout

### Tab Navigation
- **Graph Tab**: Interactive knowledge graph visualization
- **Chat Tab**: AI-powered conversational interface
- **Preview Tab**: Live website preview panel

### Visual Feedback
- Visit count badges on nodes
- Animated connections between related pages
- Smooth hover effects
- Loading states and error handling

## 🎓 Technical Details

### Build Process
- Webpack bundles with Dotenv plugin
- Environment variables injected at build time
- TypeScript compilation with ts-loader
- CSS extraction with MiniCssExtractPlugin
- Tailwind CSS processing

### API Integration
- Gemini 2.0 Flash Exp model
- Context-aware chat prompts
- Rate limiting
- Error handling
- Response parsing

### Storage Architecture
- Chrome Storage API (local and sync)
- PageNode interface for visit tracking
- GraphNode interface for visualization
- Efficient querying and updates
- Automatic cleanup

## 📚 Documentation

- **[README.md](README.md)** - Main documentation (you are here)
- **[QUICK_START.md](QUICK_START.md)** - 5-minute setup guide
- **[REVAMP_SUMMARY.md](REVAMP_SUMMARY.md)** - Complete list of changes
- **[DELIVERY_SUMMARY.md](DELIVERY_SUMMARY.md)** - Feature delivery overview

## Privacy & Security

- **Local Storage**: All data stored locally in Chrome extension storage
- **API Key Security**: Gemini API key stored securely in Chrome sync storage
- **No Data Collection**: Extension doesn't collect or transmit personal data
- **Permission Minimal**: Only requests necessary Chrome permissions

## Performance

- **Lazy Loading**: Graph nodes loaded on demand
- **Memory Management**: Automatic cleanup of old data
- **Storage Limits**: Configurable storage size limits
- **Background Processing**: Non-blocking content analysis

## Troubleshooting

### Common Issues

1. **Extension not loading**:
   - Check Chrome Developer mode is enabled
   - Verify manifest.json is valid
   - Check console for errors

2. **API not working**:
   - Verify Gemini API key is correct
   - Check internet connection
   - Monitor browser console for API errors

3. **Graph not showing**:
   - Ensure content has been captured
   - Check if filters are too restrictive
   - Verify ReactFlow dependencies are loaded

### Debug Mode

Enable debug logging by setting `console.log` statements in the background script. Logs can be viewed in Chrome extension inspector.

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## License

[Specify license here]

## Roadmap

- [ ] Enhanced AI analysis with multiple models
- [ ] Export to common formats (JSON, CSV, GraphML)
- [ ] Collaborative knowledge graphs
- [ ] Mobile companion app
- [ ] Integration with research tools
- [ ] Advanced visualization layouts
- [ ] Machine learning for content relevance

## Support

For support, please:
1. Check the troubleshooting section
2. Search existing issues
3. Create a new issue with detailed description

---

**Note**: This extension requires a Google Gemini API key for full functionality. The free tier provides generous limits for personal research use.

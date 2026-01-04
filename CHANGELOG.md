# Changelog

All notable changes to Traily Chrome Extension.

## [2.0.0] - 2024-12-26 - Complete Professional Revamp

### 🎉 Major Features

#### Added
- **Environment Variable Configuration**: Secure API key management with `.env` files
- **AI Chat Interface**: Conversational AI assistant with full browsing context
- **Live Preview**: Embedded website preview panel with iframe
- **Visit Tracking**: Accurate counting of page visits with timestamps
- **Modern Light Mode UI**: Complete redesign with professional color scheme
- **Tab Navigation**: Organized interface with Graph, Chat, and Preview tabs
- **Real-time Statistics**: Display of pages, visits, and domains

#### Components
- `ChatInterface.tsx` - AI chat with context awareness
- `LivePreview.tsx` - Embedded website preview
- `ModernSidePanel.tsx` - Tab-based main interface

#### Services
- Enhanced `storageManager.ts` with visit tracking methods:
  - `recordPageVisit()`
  - `getPageVisits()`
  - `getAllNodes()`
  - `getTopVisitedPages()`
- Enhanced `geminiProcessor.ts` with `chatWithContext()` method

#### Configuration
- `.env` file support for API keys
- `.env.example` template
- Updated `.gitignore` for security
- `dotenv-webpack` integration

### 🎨 UI/UX Improvements

#### Changed
- Complete rewrite of `globals.css` with modern light theme
- Professional color palette (Sky blue primary, warm grays)
- New CSS custom properties for theming
- Modern button styles
- Clean input fields with focus states
- Beautiful badge components
- Smooth animations and transitions
- Custom scrollbars
- Card-based layouts

#### Simplified
- `SearchInterface.tsx` - Streamlined search component
- Header statistics display
- Node detail panels

### 🔐 Security

#### Added
- Environment variable support for API keys
- `.gitignore` entries for `.env` files
- No hardcoded secrets in codebase

#### Changed
- `ConfigManager` now reads from `process.env.GEMINI_API_KEY`
- Webpack configured with Dotenv plugin

### 🐛 Bug Fixes

#### Fixed
- Visit counting now accurate (was not tracking correctly)
- Page navigation tracking improved
- Better error handling in all components
- Graceful fallbacks for iframe restrictions

### 📝 Documentation

#### Added
- `QUICK_START.md` - 5-minute setup guide
- `REVAMP_SUMMARY.md` - Complete list of changes
- `DELIVERY_SUMMARY.md` - Feature delivery overview
- Enhanced README.md with new features

#### Updated
- Installation instructions
- Usage examples
- Configuration guide
- Project structure
- Feature list

### 🔧 Technical

#### Dependencies
- Added `dotenv-webpack@^8.0.1`

#### Build
- Updated webpack configuration with Dotenv plugin
- Added newtab entry point
- Enhanced HTML plugin configuration

#### API
- Updated to Gemini 2.0 Flash Exp model
- Improved error handling
- Better rate limiting

### 🎯 Improvements

#### Performance
- Optimized React components
- Efficient storage queries
- Minimal re-renders
- CSS transitions instead of JS animations

#### Developer Experience
- Better TypeScript typing
- Cleaner code structure
- Comprehensive comments
- Modular components

### 📊 Statistics Features

#### Added
- Total pages count in header
- Total visits count in header
- Unique domains count in header
- Per-page visit badges
- First and last visit timestamps

---

## [1.0.0] - Previous Version

### Features
- Basic knowledge graph visualization
- Content capture from web pages
- Gemini API integration
- ReactFlow graph rendering
- Chrome storage management
- Search interface
- Node and edge management

### UI
- Dark space theme
- Basic popup interface
- Side panel with graph
- Simple node details

---

## Version Comparison

| Feature | v1.0.0 | v2.0.0 |
|---------|--------|--------|
| UI Theme | Dark | Light |
| API Key Storage | Hardcoded | Environment Variable |
| Visit Tracking | No | Yes |
| Chat Interface | No | Yes |
| Live Preview | No | Yes |
| Tab Navigation | No | Yes |
| Statistics | No | Yes |
| Visit Badges | No | Yes |
| Modern Design | No | Yes |
| Context-Aware AI | No | Yes |

---

## Upgrade Notes

### Breaking Changes
None - this is backward compatible

### Migration Steps
1. Copy `.env.example` to `.env`
2. Add your Gemini API key to `.env`
3. Run `npm install` to get new dependencies
4. Run `npm run build`
5. Reload extension in Chrome

### What to Expect
- New modern light UI
- All your data preserved
- New tabs for Chat and Preview
- Visit counts start from zero (historical data not available)

---

## Future Releases

### Planned for v2.1.0
- Export functionality for chat history
- Advanced filtering in graph view
- Bookmark management
- Collections/folders

### Planned for v3.0.0
- Shared knowledge graphs
- Browser sync
- Mobile companion app
- Machine learning for content relevance

---

## Notes

### API Changes
- Now using Gemini 2.0 Flash Exp model
- Endpoint configurable via environment variable
- Better error handling and rate limiting

### Storage Changes
- Added PAGE_VISITS storage key
- New PageNode interface
- Visit tracking data structure
- Backward compatible with existing data

### UI Changes
- Complete redesign - no old theme available
- All new components
- Modern interaction patterns
- Improved accessibility

---

**For detailed information about any release, see the documentation files in the project root.**

# Quick Start Guide - Traily Chrome Extension

## 🚀 Installation & Setup (5 minutes)

### Step 1: Get Your API Key
1. Visit [Google AI Studio](https://makersuite.google.com/app/apikey)
2. Sign in with your Google account
3. Click "Create API Key"
4. Copy your API key

### Step 2: Configure the Extension
1. Navigate to the project folder:
   ```bash
   cd d:/trail
   ```

2. Copy the environment file:
   ```bash
   cp .env.example .env
   ```

3. Open `.env` and add your API key:
   ```env
   GEMINI_API_KEY=your_api_key_here
   ```

### Step 3: Build the Extension
```bash
npm install
npm run build
```

### Step 4: Load in Chrome
1. Open Chrome and go to `chrome://extensions/`
2. Enable "Developer mode" (toggle in top right)
3. Click "Load unpacked"
4. Select the `d:/trail/dist` folder
5. Done! 🎉

## 📖 How to Use

### First Time Usage

1. **Browse Normally**: Visit any website - Traily will automatically:
   - Capture page content
   - Extract key concepts
   - Build your knowledge graph
   - Track visits

2. **Open the Extension**:
   - Click the Traily icon in your Chrome toolbar
   - Or use keyboard shortcut (if configured)
   - Side panel will open

### Main Features

#### 📊 Knowledge Graph (Default Tab)
```
What you'll see:
- Interactive graph of all pages you've visited
- Nodes represent pages
- Lines represent connections (shared concepts)
- Click any node to see details
```

**Actions:**
- Click nodes to see details
- View visit counts
- See extracted concepts
- Open live preview

#### 💬 Chat (Chat Tab)
```
Example questions:
- "What have I been researching this week?"
- "Find pages about React"
- "Show connections between my TypeScript and JavaScript pages"
- "Summarize what I learned about Chrome extensions"
```

**Features:**
- Full context of your browsing history
- Natural language understanding
- Smart insights and connections
- Real-time responses

#### 👁️ Preview (Preview Tab)
```
Opens when you click "Open Live Preview" on any node
```

**Features:**
- View websites in the extension
- No need to open new tabs
- Quick access to full site
- Respects security restrictions

### Tips & Tricks

#### 1. **Best Results**
- Visit research-heavy sites (documentation, articles, papers)
- Skip social media (already filtered)
- Let AI process (takes a few seconds per page)

#### 2. **Finding Connections**
- Look for thick lines in the graph (many shared concepts)
- Check visit counts (hover over nodes)
- Use chat to find patterns

#### 3. **Search**
- Use the search bar to filter nodes
- Real-time filtering
- Search by title, URL, or concept

#### 4. **Chat Effectively**
- Be specific: "pages about React hooks"
- Ask for summaries: "summarize my research on TypeScript"
- Request connections: "how are my ML pages connected?"

## ⚙️ Configuration

### API Settings
The extension uses the API key from `.env` file. To change it:
1. Edit `d:/trail/.env`
2. Update `GEMINI_API_KEY`
3. Rebuild: `npm run build`
4. Reload extension in Chrome

### Extension Settings
Click the Traily icon → Settings:
- Enable/disable auto-capture
- Adjust content length threshold
- Add domains to skip
- Configure capture frequency

## 🔍 Troubleshooting

### Issue: Extension not capturing pages
**Solution:**
- Check if API key is set correctly in `.env`
- Rebuild the extension
- Check console for errors (F12 in extension popup)

### Issue: Chat not responding
**Solution:**
- Verify API key is valid
- Check internet connection
- Look for API quota limits

### Issue: Preview not loading
**Solution:**
- Some sites block embedding (X-Frame-Options)
- Use "Open in New Tab" button instead
- This is a security feature, not a bug

### Issue: Graph is empty
**Solution:**
- Visit some research pages first
- Wait a few seconds for processing
- Check if auto-capture is enabled
- Verify API is working

## 📊 Understanding the UI

### Statistics Bar
```
[42 pages] [156 visits] [12 domains]
```
- **Pages**: Total unique URLs captured
- **Visits**: Total number of visits across all pages
- **Domains**: Number of unique domains

### Visit Badges
```
👁️ Visited 5 times
```
Shows how many times you've visited a specific page

### Node Colors
- **Blue**: Regular web pages
- **Green**: Concept nodes (future feature)
- **Yellow**: Author nodes (future feature)
- **Purple**: Domain nodes (future feature)

## 🎯 Use Cases

### 1. **Research Projects**
- Track papers and articles
- Find connections between topics
- Ask AI to summarize findings
- Export graph (future feature)

### 2. **Learning New Technology**
- Documentation pages
- Tutorial sites
- Stack Overflow threads
- See how concepts connect

### 3. **Job Search**
- Company research
- Industry analysis
- Connection mapping
- Interview prep

### 4. **Content Creation**
- Source tracking
- Topic research
- Connection finding
- Content planning

## 🔄 Daily Workflow

### Morning Routine
1. Open extension
2. Review yesterday's research
3. Check top visited pages
4. Ask AI for insights

### During Research
1. Browse normally
2. Extension captures automatically
3. Occasionally check graph
4. Use chat for quick questions

### End of Day
1. Review knowledge graph
2. Ask AI to summarize the day
3. Note important connections
4. Plan next day's research

## 🎨 Keyboard Shortcuts (Future)

Currently not implemented, but planned:
- `Ctrl/Cmd + K`: Open search
- `Ctrl/Cmd + /`: Open chat
- `Ctrl/Cmd + P`: Open preview
- `Ctrl/Cmd + G`: Focus graph

## 📈 Maximizing Value

### Best Practices
1. **Be Consistent**: Browse regularly for better patterns
2. **Use Chat**: Don't just look at the graph - ask questions
3. **Review Often**: Check your knowledge graph weekly
4. **Curate**: Use search to filter noise
5. **Preview**: Use live preview to revisit pages quickly

### Power User Tips
1. Open extension in new window (right-click → "Open in new window")
2. Use two monitors (extension on one, browsing on other)
3. Regular chat sessions to find insights
4. Export data for backup (future feature)

## 🆘 Getting Help

### Check Console
1. Open extension
2. Right-click → Inspect
3. Check Console tab for errors

### Common Solutions
- Clear extension storage
- Rebuild extension
- Check API key
- Restart Chrome

## 🎉 You're Ready!

Start browsing and building your knowledge graph. The extension works best with time - the more you browse, the more insights you'll get!

Happy researching! 📚✨

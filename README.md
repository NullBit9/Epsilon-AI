# Epsilon

OpenClaw agent with a simple web interface.

## Quick Start

```bash
# Install dependencies
npm install

# Start the server
npm start
```

Then open http://localhost:3000 in your browser.

**That's it!** OpenClaw is bundled with the repo - no external installation needed.

## What's Inside

- `index.html` - Chat interface (dark mode supported)
- `server.js` - Express server that bridges the UI to OpenClaw
- `package.json` - Dependencies and scripts
- `openclaw.mjs` - Bundled OpenClaw CLI
- `openclaw-dist/` - Bundled OpenClaw runtime
- `openclaw-skills/` - Bundled OpenClaw skills
- OpenClaw workspace files (SOUL.md, AGENTS.md, etc.)

## How It Works

1. User types a message in the web UI
2. Server receives it via `/chat` POST endpoint
3. Server calls the bundled OpenClaw: `node openclaw.mjs run --message "..." --session epsilon`
4. OpenClaw processes the message and returns a response
5. Server sends the response back to the UI

## Requirements

- Node.js 18+

That's it! OpenClaw is fully bundled - no external dependencies or setup required.

## Customization

Edit the workspace files to change agent behavior:

- `SOUL.md` - Agent personality and guidelines
- `USER.md` - User preferences
- `IDENTITY.md` - Agent identity
- `TOOLS.md` - Environment-specific notes

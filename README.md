# Travel Assistant based on CloudFlareLLM Chat Application Template

This project is a Travel Assistant chatbot built using Cloudflare Workers and the LLM Chat App template. It leverages the Cloudflare Worker AI framework and provides a conversational travel assistant experience.

Features

- Conversational AI: Handles chat requests using a large language model (LLM).
- Session Memory: Remembers past messages within the same chat session for contextual conversations.
- Custom System Prompt: Modified the system prompt to behave as a travel assistant.
- UI Template: Retains the same user interface template provided by the Cloudflare Worker AI Chat App.
- Updated Fetch Requests: Modified the way fetch requests are handled in the code to better suit the Travel Assistant functionality.

Implementation

-Built directly in Cloudflare Workers using the LLM Chat App template.
   Code modifications include:
      -Adjusted system prompt to align with travel assistant behavior.
      -Enhanced chat handling to maintain context across messages in a session.
      -Integrated session-based memory to provide better, continuous conversation.
      -Changed the fetch request implementation to improve data handling and interaction with the LLM API.

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v18 or newer)
- [Wrangler CLI](https://developers.cloudflare.com/workers/wrangler/install-and-update/)
- A Cloudflare account with Workers AI access

### Installation

1. Clone this repository:

   ```bash
   git clone https://github.com/cloudflare/templates.git
   cd templates/llm-chat-app
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Generate Worker type definitions:
   ```bash
   npm run cf-typegen
   ```

### Development

Start a local development server:

```bash
npm run dev
```

This will start a local server at http://localhost:8787.

Note: Using Workers AI accesses your Cloudflare account even during local development, which will incur usage charges.

### Deployment

Deploy to Cloudflare Workers:

```bash
npm run deploy
```

### Monitor

View real-time logs associated with any deployed Worker:

```bash
npm wrangler tail
```

## Project Structure

```
/
├── public/             # Static assets
│   ├── index.html      # Chat UI HTML
│   └── chat.js         # Chat UI frontend script
├── src/
│   ├── index.ts        # Main Worker entry point
│   └── types.ts        # TypeScript type definitions
├── test/               # Test files
├── wrangler.jsonc      # Cloudflare Worker configuration
├── tsconfig.json       # TypeScript configuration
└── README.md           # This documentation
```
(Same as that of LLM Chat Application)

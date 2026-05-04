# Awesome MCP Apps [![Awesome](https://awesome.re/badge.svg)](https://awesome.re) [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT) [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)

A curated list of awesome applications, UI components, and resources for the **Model Context Protocol (MCP) APPS **.

> **The centralized directory of top MCPApps.** Maintaining the standard for Model Context Protocol applications and ecosystem.

## What are MCPApps?

**MCPApps** are the applications and interfaces that bring the Model Context Protocol to life for end-users. 

While **MCP Servers** act as the backend "plugins" that expose data and tools, **MCPApps** are the frontend experiences—such as Desktop Agents, IDEs, and specialized workflows—that consume these servers to provide context-aware intelligence.

This list captures both the **Applications** and the **UI Components** (MCPApps UI) used to build them.

MCP-UI now standardized as MCPAPPS- Read more about MCP-UI here- https://mcpui.dev/

The Model Context Protocol (MCP) is an open standard that enables AI models to interact with your data and tools. It provides a universal way to connect AI assistants to systems like databases, tailored APIs, and business applications.

> 🚀 **New to MCP?** Check out the [official documentation](https://modelcontextprotocol.io/introduction) to get started!

https://github.com/user-attachments/assets/7180c822-2dd9-4f38-9d3e-b67679509483

## 📂 Categories

Explore MCPApps by category:

| Category | Description |
| :--- | :--- |
| [🔗 Aggregators](categories/aggregators.md) | Tools that collect and organize data from multiple sources. |
| [🎨 Art & Culture](categories/art-culture.md) | Apps for creativity, design, and cultural exploration. |
| [📐 Architecture & Design](categories/architecture-design.md) | CAD, blueprint, and structural design tools. |
| [🧬 Biology & Medicine](categories/biology-medicine.md) | Bioinformatics, medical research, and healthcare apps. |
| [📂 Browser Automation](categories/browser-automation.md) | Tools to automate web tasks and interactions. |
| [☁️ Cloud Platforms](categories/cloud-platforms.md) | Integrations for AWS, Azure, GCP, and other cloud services. |
| [👨‍💻 Code Execution](categories/code-execution.md) | Sandboxes and environments for running code safely. |
| [🤖 Coding Agents](categories/coding-agents.md) | Autonomous agents that help write, review, and fix code. |
| [🖥️ Command Line](categories/command-line.md) | CLI tools and terminal enhancements. |
| [💬 Communication](categories/communication.md) | Chat, email, and messaging integrations. |
| [👤 Customer Data](categories/customer-data.md) | CDPs, CRM, and user profile management. |
| [📊 Data Platforms](categories/data-platforms.md) | Big data processing, pipelines, and storage. |
| [🧮 Data Science](categories/data-science.md) | Notebooks, analysis, and visualization tools. |
| [🗄️ Databases](categories/databases.md) | SQL, NoSQL, and vector database connectors. |
| [🚚 Delivery](categories/delivery.md) | Logistics, shipping, and tracking integrations. |
| [🛠️ Developer Tools](categories/developer-tools.md) | Utilities for software development workflows. |
| [📟 Embedded Systems](categories/embedded-systems.md) | IoT, hardware control, and firmware tools. |
| [📂 File Systems](categories/file-systems.md) | Local and remote file management. |
| [💰 Finance & Fintech](categories/finance-fintech.md) | Banking, trading, and financial analysis. |
| [🎮 Gaming](categories/gaming.md) | Game development, analysis, and playing agents. |
| [🧠 Knowledge & Memory](categories/knowledge-memory.md) | Second brains, notes, and vector memory systems. |
| [🗺️ Location Services](categories/location-services.md) | Maps, geolocation, and routing. |
| [🎯 Marketing](categories/marketing.md) | Adtech, SEO, and campaign management. |
| [📊 Monitoring](categories/monitoring.md) | Observability, logging, and performance tracking. |
| [🎥 Multimedia](categories/multimedia.md) | Video, audio, and image processing. |
| [🔎 Search & Extraction](categories/search-extraction.md) | Web scraping, crawling, and search engines. |
| [🔒 Security](categories/security.md) | Auth, penetration testing, and vulnerability scanning. |
| [🌐 Social Media](categories/social-media.md) | Integrations for Twitter, LinkedIn, Reddit, etc. |
| [🏃 Sports](categories/sports.md) | Analytics and tracking for sports and fitness. |
| [🎧 Support & Service](categories/support-service.md) | Helpdesk, ticketing, and customer service. |
| [🗣️ Text-to-Speech](categories/text-to-speech.md) | TTS and voice synthesis. |
| [🌎 Translation](categories/translation.md) | Language translation and localization. |
| [🚆 Travel](categories/travel-transportation.md) | Booking, flights, and transportation logistics. |
| [🔄 Version Control](categories/version-control.md) | Git, SVN, and repo management. |
| [🏢 Productivity](categories/productivity.md) | Office tools, task management, and collaboration. |
| [🛠️ Other Tools](categories/other-tools.md) | Integrations that don't fit elsewhere. |

## 🌟 Featured MCPApps

Applications that showcase the power of MCP APPS in production or creative environments.

- Post in r/MCPservers (https://www.reddit.com/r/MCPservers/) your APP and based of popularity within Community - we will feature your APP here.
  

## 🧩 MCPApps (UI/Components)

Standardized **MCPApps** UI components and frontend libraries.

- *[Add a component here]*

## ⚡ Quick Example (will be updated shortly!)

**Server Side** - Create interactive resources to return in your MCP tool results:

### TypeScript

```typescript
import { createUIResource } from '@mcp-ui/server';

const interactiveForm = createUIResource({
  uri: 'ui://user-form/1',
  content: {
    type: 'externalUrl',
    iframeUrl: 'https://yourapp.com'
  },
  encoding: 'text',
});
```

### Python

```python
from mcp_ui_server import create_ui_resource

interactive_form = create_ui_resource({
    "uri": "ui://user-form/1",
    "content": {
        "type": "externalUrl",
        "iframeUrl": "https://yourapp.com"
    },
    "encoding": "text"
})
```

**Client Side** - Render on the host with a single component:

### React

```jsx
import { UIResourceRenderer } from '@mcp-ui/client';

// `mcpResource` would come from your MCP response
function MyApp({ mcpResource }) {
  return (
    <UIResourceRenderer
      resource={mcpResource.resource}
      onUIAction={(action) => {
        console.log('User action:', action);
      }}
    />
  );
}
```

### Web Component / HTML

```html
<!-- index.html -->
<ui-resource-renderer id="resource-renderer"></ui-resource-renderer>

<!-- main.js -->
<script type="module">
  // 1. Import the script to register the component
  import '@mcp-ui/client/ui-resource-renderer.wc.js';

  // 2. This object would come from your MCP response
  const mcpResource = {
    resource: {
      uri: 'ui://user-form/1',
      mimeType: 'text/uri-list',
      text: 'https://example.com'
    }
  };

  // 3. Get the element and pass data
  const renderer = document.getElementById('resource-renderer');
  renderer.setAttribute('resource', JSON.stringify(mcpResource.resource));

  // 4. Listen for events
  renderer.addEventListener('onUIAction', (event) => {
    console.log('User action:', event.detail);
  });
</script>
```

## 📚 Resources

- [Official Documentation](https://github.com/MCP-UI-Org/mcp-ui)
- [MCP APPS List]  https://TopMCPApps.com

## 🤝 Contributing

Contributions are welcome! Please read the [contribution guidelines](CONTRIBUTING.md) first.

## 📜 License

Distributed under the MIT License. See `LICENSE` for more information.

- [EventTrader MCP Server](https://github.com/eventtrader/event-trader-mcp) — AI prediction market trading: place bets, TGE token price predictions, real-time orderbooks, AI agent cloning, due diligence scoring. Remote endpoint at `cymetica.com/.well-known/mcp.json`. [Platform](https://cymetica.com?utm_source=github&utm_medium=pr&utm_campaign=mcp-outreach) | [TGE Markets](https://cymetica.com/tge-launch?utm_source=github&utm_medium=pr&utm_campaign=mcp-outreach)

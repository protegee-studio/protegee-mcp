# Protegee MCP

Plan, write, render and schedule videos, carousels and threads for your brand from your AI app. Every step shows up in your [Protegee](https://protegee.studio) studio.

This repository holds the public listing and setup guide for the hosted Protegee MCP server. The server runs at the URL below, and its source code is private, so there is nothing to install or self-host.

```text
https://app.protegee.studio/mcp
```

## What you can ask for

- "Pitch five reel ideas for my brand this week and add the best two to my board."
- "Write a storyboard for my newest idea and show me the shots."
- "Make a 20 second explainer clip that charts how our signups grew this month."
- "What is on my board?"
- "Schedule my approved video for Thursday morning."

Protegee keeps your brand consistent. Your characters, locations, products, styles, voices and logos live in your library, and new work reuses them.

## Connect

You need a [Protegee account](https://protegee.studio). The first time you connect, your AI app opens a Protegee sign-in page and asks you to approve access.

### Claude

Open Customize > Connectors, choose Add, then Add custom connector, and paste the URL. On Team and Enterprise, an owner adds it first in Organization settings > Connectors.

### Claude Code

```bash
claude mcp add --transport http protegee https://app.protegee.studio/mcp
```

### ChatGPT

At [chatgpt.com/plugins](https://chatgpt.com/plugins), choose +, then Add custom MCP server. Paste the URL, choose OAuth and install it. On Business, Enterprise and Edu, an admin adds it. Custom servers on Pro are limited to read and fetch, so ChatGPT can view your work there but can't make changes.

### Gemini

At [gemini.google.com](https://gemini.google.com), open Settings > Connected Apps > Custom apps, choose Add a custom app and paste the URL. Google currently limits this to personal accounts in the US, in English.

For Gemini CLI:

```bash
gemini mcp add --transport http protegee https://app.protegee.studio/mcp
```

Then run `/mcp auth protegee` inside Gemini CLI to sign in.

### Grok

On Grok Business or Enterprise, an admin opens Connectors, chooses Add Connector, then Other, and pastes the URL. Members then connect at [grok.com/connectors](https://grok.com/connectors).

### Cursor

Add this to `~/.cursor/mcp.json`:

```json
{
  "mcpServers": {
    "protegee": {
      "url": "https://app.protegee.studio/mcp"
    }
  }
}
```

### GitHub Copilot in VS Code

Run **MCP: Add Server** from the Command Palette, choose HTTP and paste the URL. On Copilot Business and Enterprise, your organization must turn on the "MCP servers in Copilot" policy.

### Other apps

Other apps that support remote MCP servers over Streamable HTTP with OAuth can connect with the same URL.

## Scheduling only

If you only want to schedule finished posts, use this narrower connection:

```text
https://app.protegee.studio/mcp/schedule
```

It has five tools: `list_ready_posts`, `list_schedule`, `schedule_post`, `reschedule_post` and `unschedule_post`. It can't create or edit content, and it only schedules posts already approved in Protegee.

## You stay in control

- Your AI app acts as you, and only on the brands you can open.
- Approving, posting and sending DMs are off for connected AI apps by default. A brand owner can turn them on in Settings > Brands, and each action then needs your own words.
- Billing and plan changes stay in the Protegee app.
- Renders count against your Protegee plan.
- You can revoke an app at any time in Settings > Connect an AI app.

## Support

- Website: [protegee.studio](https://protegee.studio)
- Privacy: [protegee.studio/privacy](https://protegee.studio/privacy)
- Terms: [protegee.studio/terms](https://protegee.studio/terms)
- Contact, including security reports: [contact@protegee.studio](mailto:contact@protegee.studio)

Copyright Protegee. All rights reserved.

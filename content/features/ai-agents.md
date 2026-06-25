---
title: "AI Agents"
weight: 40
description: "Set up the local AI assistant and understand what it can and cannot do."
---

HoneyBear Folio includes a built-in AI assistant that can answer questions about your data using a local Ollama model. The assistant appears in the sidebar as **AI Assistant**.

## Before You Start

The AI assistant depends on [Ollama](https://ollama.com) running on your machine or on a reachable server.

You need all of the following before chat is available:

- A running Ollama server. The default URL is `http://localhost:11434`.
- At least one downloaded Ollama model.
- A saved model selection in HoneyBear Folio.

If the connection succeeds but no models are installed, the setup flow will stop until you download one.

## Initial Setup

The first time you open **AI Assistant**, HoneyBear Folio walks you through a three-step setup:

1. **Connect**: Enter the Ollama server URL and test the connection.
2. **Model**: Choose one of the models returned by Ollama.
3. **Ready**: Save the configuration and open the chat view.

The Ollama URL must be a plain `http://` or `https://` base URL. URLs with authentication info, query strings, fragments, or extra paths are rejected.

## What the Assistant Can Do

The assistant can inspect your stored finance data and answer questions about it in natural language. Today it has read-only access to:

- Accounts
- Transactions
- Categories
- Payees
- Scheduled transactions
- Rules
- Exchange rates
- Asset tracking
- Investment portfolios
- Net worth

Typical questions include:

- "What are my largest expenses this month?"
- "Which payees appear most often?"
- "Do I have any scheduled transactions due soon?"
- "What rules are currently configured?"
- "What is my current net worth?"
- "How is my investment portfolio performing?"
- "What are my tracked assets worth?"

Responses can include tool call badges so you can see which internal data source was used. Some models also support a reasoning block, which HoneyBear Folio can display inline.

## Working with Conversations

The chat view supports multiple conversations. You can:

- Start a new conversation.
- Rename an existing conversation.
- Delete old conversations.
- Switch between available Ollama models after setup.
- Stop a response while it is streaming.

Conversation messages are stored locally with the rest of your app data.

## Current Limits

The assistant is intentionally scoped.

- It does not edit your data for you.
- It only works after Ollama is reachable.
- It only sees the tools wired into the app, not every screen or database table.

If you want the best results, ask focused questions and mention a time range, account, category, or payee when relevant.
# OpenAI Agents SDK - Multi-Agent Sales

Hands-on example of building a **multi-agent sales workflow** using the **OpenAI Agents SDK** with **Claude** as the LLM provider.

## What This Covers

* Creating specialized AI agents
* Running multiple agents in parallel
* Streaming agent responses
* Using one agent as a tool for another agent
* Tool calling with `@function_tool`
* Requiring an agent to use a tool
* Automated email sending with SMTP
* Agent tracing with `trace`
* Multi-agent orchestration and workflow design

## Workflow

```text
Sales Writer 1 ──┐
Sales Writer 2 ──┼──> Sales Manager ──> Select Best Email ──> Send Email
Sales Writer 3 ──┘
```

The workflow uses three sales agents with different writing styles:

* Professional
* Humorous
* Executive

A sales manager agent uses these agents as tools, evaluates their generated emails, selects one, and uses the email tool to send the final message.

## Tech Stack

* Python
* OpenAI Agents SDK
* Anthropic Claude
* OpenAI SDK
* SMTP
* SQLite
* uv

## Setup

Install the dependencies:

```bash
uv sync
```

Create a `.env` file with your credentials:

```env
ANTHROPIC_API_KEY=your_anthropic_api_key
EMAIL_ADDRESS=your_email
EMAIL_SMTP_SERVER=your_smtp_server
EMAIL_APP_PASSWORD=your_app_password
EMAIL_ADDRESS_TO=recipient_email
```

Then run the project using your preferred Python environment.

## Purpose

A practical example of **multi-agent orchestration** using the OpenAI Agents SDK, demonstrating how specialized agents can work together, use tools, and complete an end-to-end task.

<h1 align="center">Gmail AI Assistant with n8n</h1>

An AI-powered email assistant built with **n8n**, **OpenRouter**, **Gmail**, and **Telegram**.

The workflow automatically monitors incoming Gmail messages, analyzes them using a Large Language Model (LLM), and sends an AI-generated summary, priority assessment, and suggested reply directly to Telegram.

## Demo

<p align="center">
  <img src="assets/workflow.gif" alt="Workflow Demo" width="500">
</p>

## Features

- Monitors incoming Gmail messages automatically
- Uses an LLM through OpenRouter to analyze emails
- Generates:
  - Email summary
  - Priority assessment
  - Suggested reply
- Sends the analysis to a Telegram bot
- Fully automated using n8n

## Workflow

1. Gmail Trigger Detects new incoming emails 

2. Edit Fields Extracts sender, subject, and email content 

3. AI Agent Analyzes the email and generates a structured response 

4. OpenRouter LLM Provides the language model inference 

5. Telegram Bot Sends the AI-generated summary, priority, and suggested reply

## Technologies

- n8n
- Gmail Trigger
- OpenRouter
- Large Language Models (LLMs)
- Telegram Bot API


## How It Works

1. A new email arrives in Gmail.
2. The Gmail Trigger detects the new message.
3. Relevant fields (sender, subject, and email content) are extracted.
4. The AI Agent analyzes the email using an OpenRouter language model.
5. The AI generates:
   - A concise summary
   - A priority level
   - A suggested reply
6. The analysis is delivered to the configured Telegram chat.


## AI Prompt

The workflow instructs the model to analyze each email and return:

```text
1. Summary
2. Priority
3. Suggested reply
```

This makes the assistant useful for quickly triaging incoming emails without opening Gmail.


## Example Output

```text
From:
Daniyal Iran Mehr

Subject:
Project Meeting

🤖 AI Analysis

Summary:
Daniyal requests moving tomorrow's meeting to 3 PM.

Priority:
Medium

Suggested Reply:
Hi Daniyal,
3 PM works well for me. Thanks for letting me know.
Looking forward to our meeting.
```

## Setup

### Prerequisites

- n8n
- Gmail account
- OpenRouter account
- Telegram Bot

### Configuration

1. Clone this repository.

```bash
git clone https://github.com/<your-username>/gmail-ai-assistant.git
```

2. Import the workflow into n8n.

3. Configure the following credentials:

- Gmail OAuth2
- OpenRouter API
- Telegram Bot API

4. Update the Telegram Chat ID.

5. Activate the workflow.

## Future Improvements

- [ ] Read the full email body instead of using the Gmail snippet.
- [ ] Improve email content extraction and generate better summaries from Gmail data.
- [ ] Support one-click AI-generated replies directly from Telegram.
- [ ] Classify emails into categories (work, personal, promotions, etc.).
- [ ] Add calendar event creation for meeting requests.
- [ ] Use a paid LLM API to improve response quality and reliability.
- [ ] Add memory to maintain context from previous email conversations.


## License

This project is licensed under the MIT License.
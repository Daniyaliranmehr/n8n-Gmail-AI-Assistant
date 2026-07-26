<h1 align="center">Gmail AI Assistant with n8n</h1>

An AI-powered email assistant built with **n8n**.

The workflow automatically monitors incoming Gmail messages, analyzes them using a Large Language Model (LLM), and sends an AI-generated summary, priority assessment, and suggested reply directly to Telegram.

## Demo

<p align="center">
  <img src="assets/workflow.gif" alt="Workflow Demo" width="500">
</p>

## Features

- Automatically monitor incoming Gmail messages.
- Retrieve the complete email body for accurate analysis.
- Generate AI-powered summaries and identify key information.
- Classify email priority and detect spam.
- Deliver structured email insights directly to Telegram.

## Workflow

1. Gmail Trigger detects a new email.

2. Gmail API fetches the complete email.

3. Email content is cleaned and extracted.

4. AI Agent analyzes the email.

5. Telegram receives the analysis.

## Technologies

- n8n
- Gmail Trigger
- OpenRouter
- Large Language Models (LLMs)
- Telegram Bot API


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

- [x] Read the full email body instead of using the Gmail snippet.
- [ ] Improve HTML parsing and email content cleaning.
- [ ] Support one-click AI-generated replies directly from Telegram.
- [ ] Classify emails into categories (work, personal, promotions, etc.).
- [ ] Add calendar event creation for meeting requests.
- [ ] Use a paid LLM API to improve response quality and reliability.
- [ ] Add memory to maintain context from previous email conversations.


## Changelog

### v0.2.0
- Read the full Gmail email body instead of using only the snippet.
- Improved email content extraction and cleaning.
- Enhanced AI prompt for more structured email analysis.

### v0.1.0
- Gmail Trigger integration.
- AI email analysis.
- Telegram notifications.


## License

This project is licensed under the MIT License.

#  Simple ReAct Agent

[![Open in Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/rajsiddarth/SimpleReActAgent/HEAD)
## 🔐 API Key Setup

To use this agent, you'll need an OpenAI API key..Paste your OpenAI key like this when prompted in notebook:

OPENAI_API_KEY=sk-xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx

## Overview
This project implements a basic ReAct-style agent that simulates step-by-step reasoning and action execution using OpenAI's GPT model.

The agent runs in a loop of:
**Thought → Action → PAUSE → Observation → Answer**

---

##  Features

- Maintains full conversation history
- Supports tool use through `Action:` commands
- Supports multi-step reasoning with Observations and PAUSE
- Uses OpenAI's `gpt-4.1-mini` model
- Clean agent interface with Python class

---

## How It Works

1. The user asks a question.
2. The agent thinks (`Thought`), takes an action (`Action: tool: input`), then `PAUSE`s.
3. The environment injects an `Observation`.
4. The agent resumes with final `Answer`.

Example:
Question: How much does a Bulldog weigh?
Thought: I should look up the dog's weight.
Action: average_dog_weight: Bulldog
PAUSE

PRs welcome! You can contribute by:
1. Adding new tools
2. Improving prompt design
3. Adding CLI or web UI


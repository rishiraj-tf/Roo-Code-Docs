---
description: Configure xAI's Grok models in Roo Code. Access Grok-3, Grok-2, and vision models with large context windows and reasoning capabilities.
keywords:
  - xAI
  - Grok
  - Roo Code
  - AI models
  - reasoning AI
  - vision models
  - large context
  - Grok-3
  - Grok-2
image: /img/social-share.jpg
sidebar_label: xAI (Grok)
---

# Using xAI (Grok) With Roo Code

xAI is the company behind Grok, a large language model known for its conversational abilities and large context window. Grok models are designed to provide helpful, informative, and contextually relevant responses.

**Website:** [https://x.ai/](https://x.ai/)

---

## Getting an API Key

1.  **Sign Up/Sign In:** Go to the [xAI Console](https://console.x.ai/). Create an account or sign in.
2.  **Navigate to API Keys:** Go to the API keys section in your dashboard.
3.  **Create a Key:** Click to create a new API key. Give your key a descriptive name (e.g., "Roo Code").
4.  **Copy the Key:** **Important:** Copy the API key *immediately*. You will not be able to see it again. Store it securely.

---

## Supported Models

Roo Code supports the following xAI Grok models:

### Grok-3 Models
* `grok-3-beta` (Default) - xAI's Grok-3 beta model with 131K context window
* `grok-3-fast-beta` - xAI's Grok-3 fast beta model with 131K context window
* `grok-3-mini-beta` - xAI's Grok-3 mini beta model with 131K context window
* `grok-3-mini-fast-beta` - xAI's Grok-3 mini fast beta model with 131K context window

### Grok-2 Models
* `grok-2-latest` - xAI's Grok-2 model - latest version with 131K context window
* `grok-2` - xAI's Grok-2 model with 131K context window
* `grok-2-1212` - xAI's Grok-2 model (version 1212) with 131K context window

### Grok Vision Models
* `grok-2-vision-latest` - xAI's Grok-2 Vision model - latest version with image support and 32K context window
* `grok-2-vision` - xAI's Grok-2 Vision model with image support and 32K context window
* `grok-2-vision-1212` - xAI's Grok-2 Vision model (version 1212) with image support and 32K context window
* `grok-vision-beta` - xAI's Grok Vision Beta model with image support and 8K context window

### Legacy Models
* `grok-beta` - xAI's Grok Beta model (legacy) with 131K context window

---

## Configuration in Roo Code

1.  **Open Roo Code Settings:** Click the gear icon (<Codicon name="gear" />) in the Roo Code panel.
2.  **Select Provider:** Choose "xAI" from the "API Provider" dropdown.
3.  **Enter API Key:** Paste your xAI API key into the "xAI API Key" field.
4.  **Select Model:** Choose your desired Grok model from the "Model" dropdown.

---

## Reasoning Capabilities

Grok 3 Mini models feature specialized reasoning capabilities, allowing them to "think before responding" - particularly useful for complex problem-solving tasks.

### Reasoning-Enabled Models

Reasoning is only supported by:
* `grok-3-mini-beta`
* `grok-3-mini-fast-beta`

The Grok 3 models `grok-3-beta` and `grok-3-fast-beta` do not support reasoning.

### Controlling Reasoning Effort

When using reasoning-enabled models, you can control how hard the model thinks with the `reasoning_effort` parameter:

* `low`: Minimal thinking time, using fewer tokens for quick responses
* `high`: Maximum thinking time, leveraging more tokens for complex problems

Choose `low` for simple queries that should complete quickly, and `high` for harder problems where response latency is less important.

### Key Features

* **Step-by-Step Problem Solving**: The model thinks through problems methodically before delivering an answer
* **Math & Quantitative Strength**: Excels at numerical challenges and logic puzzles
* **Reasoning Trace Access**: The model's thinking process is available via the `reasoning_content` field in the response completion object

---

## Tips and Notes

* **Context Window:** Most Grok models feature large context windows (up to 131K tokens), allowing you to include substantial amounts of code and context in your prompts.
* **Vision Capabilities:** Select vision-enabled models (`grok-2-vision-latest`, `grok-2-vision`, etc.) when you need to process or analyze images.
* **Pricing:** Pricing varies by model, with input costs ranging from $0.3 to $5.0 per million tokens and output costs from $0.5 to $25.0 per million tokens. Refer to the xAI documentation for the most current pricing information.
* **Performance Tradeoffs:** "Fast" variants typically offer quicker response times but may have higher costs, while "mini" variants are more economical but may have reduced capabilities.
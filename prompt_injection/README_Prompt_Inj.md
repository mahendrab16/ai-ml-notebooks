
# Prompt Injection Detection and Basic Defense

A beginner-friendly Python notebook demonstrating prompt injection examples against a Gemini model and simple rule-based techniques to detect or reject suspicious prompts.

## Project Overview

This notebook explores prompt injection, a technique in which a user attempts to override an AI system's instructions. It first sends example prompts to Gemini, then implements simple keyword-based detection and a basic rejection check.

## Notebook Contents

- Install and initialize the Google GenAI Python SDK.
- Create a helper function to send prompts to Gemini.
- Test sample prompt injection attempts, such as instruction override and role-play prompts.
- Define a list of suspicious keywords and detect them in input text.
- Implement a basic `secure_chat()` function that rejects a prompt containing a specific injection phrase and otherwise sends it to Gemini.

## Technologies Used

- Python
- Google GenAI SDK (`google-genai`)
- Gemini Flash model
- Basic string processing and conditional logic

## Requirements

- Python or Google Colab
- Google Gemini API key
- Internet connection

## Setup

Install the SDK:

```python
!pip install -q google-genai
```

Configure the client with your API key:

```python
from google import genai
client = genai.Client(api_key="YOUR_API_KEY")
```

**Security:** Do not hard-code a real API key in a notebook or publish it to GitHub. Use Google Colab Secrets or an environment variable instead.

## How to Run

1. Open the notebook in Google Colab.
2. Install `google-genai`.
3. Configure your Gemini API key securely.
4. Run the Gemini helper function.
5. Execute the sample prompt-injection tests.
6. Run the keyword detector and `secure_chat()` examples.

## Important Limitations

- The detector uses a small list of exact keywords/phrases, so it can miss paraphrased or indirect attacks.
- It may also flag harmless prompts that contain the listed words.
- The `secure_chat()` function checks only one phrase; it is not a complete prompt-injection defense.
- Prompt filtering alone is insufficient for securing an AI application. Use layered safeguards, clear instruction/data separation, least-privilege tools, and output validation for real deployments.

## Learning Outcome

Understand basic prompt injection examples and how simple input filtering works, including why keyword-based detection is limited.

## License

For learning and educational use. Check Google's Gemini API terms and model policies before deploying an application.

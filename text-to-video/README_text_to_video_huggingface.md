# Text-to-Video Generation using Hugging Face

Generate a video from a text prompt using the Hugging Face Inference API and the `meituan-longcat/LongCat-Video` model.

## Project Overview

This notebook demonstrates a simple text-to-video workflow. It asks the user to enter a prompt, sends that prompt to a video-generation model through Hugging Face's `InferenceClient`, and saves the generated video as an MP4 file.

## Features

- Accepts a text prompt dynamically from the user.
- Uses Hugging Face's Inference API.
- Generates a video with the `meituan-longcat/LongCat-Video` model.
- Saves the generated video as `video.mp4`.

## Technologies Used

- Python
- Hugging Face Hub (`huggingface_hub`)
- Hugging Face Inference API
- LongCat-Video model

## Requirements

- A Hugging Face account and an access token with the required permissions.
- Access to an inference provider that supports the selected model and the text-to-video task.
- Python environment or Google Colab with internet access.

## Installation

Install the required package:

```python
!pip install -q huggingface_hub
```

## Configuration

In the notebook, configure `InferenceClient` with an inference provider and your Hugging Face access token:

```python
from huggingface_hub import InferenceClient

client = InferenceClient(
    provider="YOUR_PROVIDER",
    api_key="YOUR_KEY"
)
```

Replace the placeholders with a provider that supports the model and your own token. Do not publish your token in a notebook or commit it to GitHub. In Google Colab, store it in **Secrets** and retrieve it at runtime.

## How to Run

1. Open the notebook in Google Colab or Jupyter.
2. Install `huggingface_hub`.
3. Configure the inference provider and Hugging Face token.
4. Run the video-generation cell.
5. Enter a descriptive text prompt when requested.
6. Wait for generation to finish. The notebook writes the returned video bytes to `video.mp4`.

## Output

The generated video is saved in the notebook's current working directory as:

```text
video.mp4
```

## Example Prompt

```text
A cinematic aerial view of green mountains at sunrise, soft golden light,
slow camera movement, realistic nature documentary style.
```

## Notes and Limitations

- The notebook is a minimal demonstration; it does not include a user interface, video editing, or batch generation.
- Model availability, provider support, access permissions, generation time, and usage limits may vary.
- The notebook uses placeholders for the provider and API token. Set these up before running it.
- Video generation may consume inference credits or be subject to provider pricing and rate limits.

## Security

Never upload a real API token to a public GitHub repository. If a token was previously exposed, revoke it and create a replacement. Store the replacement as a secret or environment variable.

## License

Check the license and usage terms of the selected model and Hugging Face inference provider before using generated videos commercially.

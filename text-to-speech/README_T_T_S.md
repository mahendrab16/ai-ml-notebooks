# Text-to-Speech with ElevenLabs

## About
This project converts text into spoken audio using the ElevenLabs Text-to-Speech API. It is designed to run in a Jupyter notebook or Google Colab.

## How it works
1. Installs the ElevenLabs Python library.
2. Connects to the ElevenLabs API.
3. Asks the user to enter text.
4. Converts the text into speech using the `eleven_multilingual_v2` model.
5. Saves the generated audio as `output.mp3` and plays it in the notebook.

## Requirements
- Python
- An ElevenLabs account and API key
- Internet access

Install the library:

```bash
pip install elevenlabs
```

## Run the notebook
1. Open the notebook in Google Colab or Jupyter.
2. Add your ElevenLabs API key securely (see below).
3. Run the cells.
4. Enter the text you want to convert into speech.
5. Listen to the generated audio or download `output.mp3`.

## Security note
Do not publish API keys in notebooks or GitHub repositories. The uploaded notebook contains a hard-coded API key. Revoke or rotate that key in your ElevenLabs account before sharing the notebook, then load the replacement from Colab Secrets or an environment variable.

Example using an environment variable:

```python
import os
from elevenlabs.client import ElevenLabs

client = ElevenLabs(api_key=os.environ["ELEVENLABS_API_KEY"])
```

## Output
The notebook creates an MP3 file named `output.mp3`.

## Technologies
- Python
- ElevenLabs Text-to-Speech API
- IPython Audio

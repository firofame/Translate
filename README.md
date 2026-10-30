# Malayalam translation

Use Python 3.10 or newer. The setup below uses Python 3.14 and `uv`.
Run these commands from this directory in an interactive zsh shell so your
exported `GEMINI_API_KEY` from `~/.zshrc` is available.

```sh
uv venv --python 3.14 .venv
uv pip install --python .venv/bin/python -r requirements.txt
source .venv/bin/activate
python -c 'import asyncio; from app import convert_to_malayalam; print(asyncio.run(convert_to_malayalam("Peace be upon you.")))'
```

`app.py` provides the async `convert_to_malayalam(text)` function; running it
directly only initializes the client. The translation instructions are loaded
from `prompts/translate.txt`, relative to `app.py`.

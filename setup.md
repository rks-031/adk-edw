## Set up Environment & Install ADK

Create & Activate Virtual Environment (Recommended):
```python
# Create
python -m venv .venv
# Activate (each new terminal)
# macOS/Linux: source .venv/bin/activate
# Windows CMD: .venv\Scripts\activate.bat
# Windows PowerShell: .venv\Scripts\Activate.ps1
```
Install ADK:

```bash
pip install google-adk
```

## Create Agent Project

You will need to create the following project structure:

```shell
parent_folder/
    multi_tool_agent/
        __init__.py
        agent.py
        .env
```

Create the folder `multi_tool_agent`:

```bash
mkdir multi_tool_agent/
```

Now create an __init__.py file in the folder:

```bash
echo "from . import agent" > multi_tool_agent/__init__.py
```

Your __init__.py should now look like this:

```python
from . import agent
```

Source code should be in the `agent.py` file in the `multi_tool_agent` folder:

`.env`

Create a .env file in the same folder:

```bash
touch multi_tool_agent/.env
```

## Setting up the model

1. get the API key
2. Open the .env file located inside (multi_tool_agent/) and copy-paste the following code.

```env
GOOGLE_GENAI_USE_VERTEXAI=FALSE
GOOGLE_API_KEY=PASTE_YOUR_ACTUAL_API_KEY_HERE
```

## Running the Agent using `adk-web`

Using the terminal, navigate to the parent directory of your agent project (e.g. using cd ..):

```bash
parent_folder/      <-- navigate to this directory
    multi_tool_agent/
        __init__.py
        agent.py
        .env
```

Run the following command to launch the dev UI.
```bash
adk web
```





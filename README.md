# Markdown to Google Docs Converter

This project automates the process of converting Markdown meeting notes into a styled Google Docs document using the Google Docs API. It parses Markdown content (as string), applies styles, and uploads the formatted document to Google Docs.

## Setup Instructions - Running Locally

### 1. Clone the Repository

```bash
git clone https://github.com/aaug1/markdown-to-google-docs.git
cd markdown-to-google-docs
```

### 2. Create a Virtual Environment

```bash
python3 -m venv .venv
source .venv/bin/activate  # On Windows, use `.venv\Scripts\activate`
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Authentication
- Generate a client_secret.json file in GCP
  -  click "+ Create credentials" --> OAuth client ID --> Desktop app
  -  Add yourself as a test user
- Place your `client_secret.json` file in the project directory.
- The script will automatically generate and store a token in `token.json`.

## Setup Instructions - Google Colab
**Note**: This project uses Colab's built-in authentication. No additional setup is required.

1. Open the `markdown-to-google-docs.ipynb` file in Google Colab.
2. Execute the cells step by step:
   - Install dependencies using the provided `pip install` command.
   - Authenticate using Colab's built-in authentication.
   - Parse the Markdown content and generate Google Docs API requests.
   - Create and update the Google Docs document with the generated requests.
3. View the newly created document in your Google Drive.


## Required Dependencies

The project requires the following Python libraries, which are listed in `requirements.txt`:
- `google-api-python-client`
- `google-auth-httplib2`
- `google-auth-oauthlib`
- `markdown-it-py`
- `mdit-py-plugins`

# Mental Health Support Chatbot

A compassionate AI-powered chatbot designed to provide emotional support and a listening ear. Built with Streamlit and OpenRouter API.

## Features

- 💬 Real-time chat interface
- 🎭 Mood tracking
- 🫁 Guided breathing exercises
- 🆘 Crisis resources
- 🤝 Empathetic responses
- 🎨 Modern, user-friendly UI

## Prerequisites

- Python 3.7 or higher
- pip (Python package installer)
- OpenRouter API key

## Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd <repository-directory>
```

2. Create and activate a virtual environment:
```bash
python -m venv .venv
source .venv/bin/activate  # On Windows, use: .venv\Scripts\activate
```

3. Install required packages:
```bash
pip install streamlit requests openai python-dotenv
```

## Configuration

1. Sign up for an OpenRouter account at https://openrouter.ai/

2. Create your API key:
   - Go to https://openrouter.ai/keys
   - Create a new API key
   - Copy the API key (it should start with "sk-or-v1-")

3. Set up your API key:

   Option 1: Environment Variable
   ```bash
   export OPENROUTER_API_KEY="your-api-key-here"
   ```

   Option 2: Create a .env file:
   ```
   OPENROUTER_API_KEY=your-api-key-here
   ```

## Running the Application

```bash
streamlit run mental_health_bot.py
```

The application will be available at:
- Local URL: http://localhost:8501
- Network URL: http://192.168.1.107:8501

## Troubleshooting API Authentication

If you encounter API authentication errors:

1. Verify your API key:
   - Ensure it starts with "sk-or-v1-"
   - Check that it's properly set in the code or environment variables
   - Verify the key is active in your OpenRouter dashboard

2. Check API headers:
   - Ensure both "Authorization" and "X-API-Key" headers are present
   - "Authorization" should be in format: "Bearer sk-or-v1-..."
   - "X-API-Key" should be the same as your API key

3. Common solutions:
   - Clear browser cache and cookies
   - Restart the Streamlit application
   - Check internet connection
   - Verify the API endpoint URL is correct

4. If using environment variables:
   ```python
   import os
   from dotenv import load_dotenv
   
   load_dotenv()
   OPENROUTER_API_KEY = os.getenv("OPENROUTER_API_KEY")
   ```

## Error Messages and Solutions

1. "API Error: Unauthorized"
   - Verify API key format and validity
   - Check if key has proper permissions
   - Ensure key is not expired

2. "Unable to connect to the API"
   - Check internet connection
   - Verify API endpoint URL
   - Check if OpenRouter service is operational

3. "No auth credentials found"
   - Ensure API key is properly set
   - Check header format
   - Verify environment variables are loaded

## Support

If you continue to experience issues:

1. Check the OpenRouter status page
2. Review API documentation at https://openrouter.ai/docs
3. Contact OpenRouter support
4. Check GitHub issues for similar problems

## License

This project is licensed under the MIT License - see the LICENSE file for details.

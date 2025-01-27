**[Join Idealabs Community](https://curios.pm) to connect, share, and learn with others!**


# Azure OpenAI Chat

A simple and intuitive AI-powered chatbot built with Streamlit and Azure OpenAI's GPT-4o model. It enables users to engage in real-time conversations and get intelligent responses instantly.

## What the Code Does
The app allows users to interact with an AI chatbot powered by Azure OpenAI. Users can enter queries, receive intelligent responses, and engage in a seamless chat experience with an easy-to-use interface.

### Features:
- **Real-time Chat:** Instantly interact with AI via a user-friendly interface.
- **Chat History:** Messages are stored within the session.
- **Error Handling:** Provides informative messages in case of errors.
- **Customizable AI Settings:** The app uses sensible defaults for parameters like temperature and max tokens.

---

## How to Use It (Step by Step)

### 1. Install Dependencies
Make sure Python is installed, then install the required libraries:

```bash
pip install streamlit requests openai 
```

### 2. Set Up API Credentials
Create a `.streamlit/secrets.toml` file and add your Azure OpenAI API credentials:

```toml
AZURE_OPENAI_API_ENDPOINT = "your-api-endpoint-here"
AZURE_OPENAI_API_KEY = "your-api-key-here"
```

### 3. Run the Application
Start the chatbot app with the following command:

```bash
streamlit run app.py
```

### 4. Interact with the Chatbot
1. The app starts with a title and chat input field.
2. Type your message in the chat input box.
3. When you press `Enter`, your message is added to the session history and displayed.
4. The app then sends the message to the Azure OpenAI API, retrieves a response, and displays it.
5. The assistant's response is appended to the chat history, enabling you to continue the conversation.
6. The session state stores chat messages, maintaining history during the session.

### 5. Deployment
You can deploy this app using platforms like Heroku, AWS, or Azure. Ensure the `.streamlit/secrets.toml` file is securely managed.

---
## How the App Was Built

The application uses **Streamlit** for the frontend to create an interactive chat interface. **Azure OpenAI API** is used for generating responses based on user queries. The app sends user input to the Azure OpenAI API and displays the generated response in the chat interface.## Code Structure

- **`app.py`**: This is the main Python script that contains the logic for the application. It handles:
  - User input and chat display using Streamlit components.
  - Sending requests to the Azure OpenAI API for generating responses.
  - Managing the chat history using `st.session_state`.

- **`.secrets.toml`**: This file stores sensitive credentials, such as your Azure OpenAI API endpoint and key, to keep them secure and out of the codebase.

- **`requirements.txt`**: A file that lists all the dependencies (Streamlit and Requests) required to run the app.

---

## What Happens in Each Step

1. **App Initialization:**
   - The app loads secrets from `secrets.toml`.
   - Session state initializes chat history.

2. **User Input:**
   - Users enter messages through the chat input box.
   - The app captures and stores user queries.

3. **Processing the Query:**
   - The query is sent to Azure OpenAI for processing.
   - The app receives and processes the response.

4. **Displaying the Response:**
   - The response is shown in the chat window.
   - The session state stores chat history.

5. **Error Handling:**
   - HTTP errors are caught and displayed.

---

## Folder Structure

```
project-folder/
│-- app.py                # Main chatbot application script
│-- requirements.txt      # Dependencies needed to run the app
│-- .streamlit/           
│   └── secrets.toml      # Stores API credentials
│-- README.md             # Documentation of the project
```

---

## Expected Output Example

**Input:** "Tell me about AI"

**Output:** "AI stands for Artificial Intelligence, enabling machines to mimic human intelligence."

---

## Common Issues & Troubleshooting

1. **Invalid API Key:**
   - Ensure credentials are correct in `.streamlit/secrets.toml`.

2. **Missing Dependencies:**
   - Run `pip install streamlit requests` to install missing packages.

3. **App Not Running:**
   - Check for typos and use the correct command: `streamlit run app.py`.

4. **Slow Responses:**
   - Try reducing the `max_tokens` value in the `generate_response` function.

---

## Security Considerations

- **Do not share your API keys publicly.**
- Use environment variables for production deployments.
- Regularly update your API keys for security.

---

## Troubleshooting

If you encounter issues:
- Make sure your **API credentials** are correct and that your Azure OpenAI resource is active.
- Check the terminal or Streamlit logs for any error messages.
- Ensure that all required Python packages are installed.

--- 

## Link to Hosted Version
[View Live App](https://azureaichat.streamlit.app/)

---

## Screenshots

1. **Application Interface:**  
   ![Image](https://github.com/user-attachments/assets/a80c99a7-9a1a-4d8e-a5fd-f30a2d779efe)


---

## Video Overview
*A short video walkthrough will be provided explaining the app's features and usage.*

---


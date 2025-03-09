# EmailBot - AI-Powered Email Assistant

EmailBot is an AI-powered email assistant designed to help users manage their email-related tasks efficiently. It integrates with Gmail to read, compose, and send emails, as well as handle attachments. The backend is built using Python (FastAPI, LangGraph, and PostgreSQL), and the frontend is a React-based web application. One of the standout features of EmailBot is its **voice input capability**, which allows users to interact with the assistant using speech-to-text technology.

---

## Features

1. **Read Emails**:
   - Retrieve the latest 5 emails from the user's Gmail inbox.
   - Extract and display sender, subject, body, and attachments.
   - Save attachments to a specified directory.

2. **Compose and Send Emails**:
   - Generate well-structured email bodies based on user input.
   - Send emails using Gmail's SMTP server.
   - Support attaching files to outgoing emails.

3. **AI-Powered Assistance**:
   - Use Google's Gemini model for natural language understanding and response generation.
   - Integrate with Tavily for web search capabilities.

4. **Voice Input (Speech-to-Text)**:
   - Allow users to input queries using voice commands.
   - Built using the Web Speech API for real-time speech recognition.
   - Supports continuous and interim results for a seamless experience.

5. **Edit and Resend**:
   - Edit user messages and resend them for a refined response.

6. **Persistent State**:
   - Use PostgreSQL for persistent state management and checkpointing.

---

## Tech Stack

### Backend
- **Python**: Core programming language.
- **FastAPI**: Web framework for building APIs.
- **LangGraph**: Stateful graph-based workflow management.
- **PostgreSQL**: Database for persistent state management.
- **Google Gemini**: AI model for natural language processing.
- **Tavily**: Web search tool for additional context.

### Frontend
- **React**: JavaScript library for building the user interface.
- **Tailwind CSS**: Utility-first CSS framework for styling.
- **Markdown**: Render AI responses with rich formatting.
- **Web Speech API**: For speech-to-text functionality.

---

## Setup Instructions

### Backend Setup

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-repo/emailbot.git
   cd emailbot/backend
   ```

2. **Install Dependencies**:
   Ensure you have Poetry installed, then run:
   ```bash
   poetry install
   ```

3. **Environment Variables**:
   Create a `.env` file in the backend directory with the following variables:
   ```env
   DB_URI=postgresql://user:password@host:port/database
   GOOGLE_API_KEY=your_google_api_key
   TAVILY_API_KEY=your_tavily_api_key
   EMAIL_ADDRESS=your_email@gmail.com
   APP_PASSWORD=your_gmail_app_password
   ```

4. **Run the Backend**:
   Start the FastAPI server:
   ```bash
   poetry run uvicorn main:app --port 8001 --reload
   ```

### Frontend Setup

1. **Navigate to the Frontend Directory**:
   ```bash
   cd ../frontend
   ```

2. **Install Dependencies**:
   ```bash
   npm install
   ```

3. **Run the Frontend**:
   ```bash
   npm run dev
   ```

4. **Access the Application**:
   Open your browser and navigate to `http://localhost:3000`.

---

## Voice Input (Speech-to-Text) Feature

### How It Works

1. **Activate Voice Input**:
   - Click the microphone icon in the input field.
   - Grant microphone permissions when prompted by your browser.

2. **Speak Your Query**:
   - Speak clearly into your microphone.
   - The Web Speech API will transcribe your speech into text in real-time.

3. **Submit the Query**:
   - The transcribed text will appear in the input field.
   - Press "Send" or hit Enter to submit the query.

4. **Interim Results**:
   - While speaking, interim results are displayed, allowing you to see the transcription as it happens.

5. **Stop Listening**:
   - The microphone stops listening automatically after a pause or when you click the microphone icon again.

---

## API Endpoints

### Backend API

#### `POST /generateanswer`
- **Request Body**:
  ```json
  {
    "input_text": "Your query here"
  }
  ```
- **Response**:
  ```json
  {
    "response": "AI-generated response"
  }
  ```

#### `GET /system-status`
- **Response**:
  ```json
  {
    "response": "System is online"
  }
  ```

---

## Usage

### Read Emails
- Type or say, "Read my latest emails."
- The bot will fetch and display the latest 5 emails with details.

### Send Emails
- Type or say, "Send an email to example@example.com with the subject 'Hello' and body 'This is a test email.'"
- The bot will compose and send the email.

### Search the Web
- Type or say, "Search for the latest news on AI."
- The bot will use Tavily to fetch and display relevant results.

### Edit and Resend
- Click the edit icon next to a user message, modify the text, and resend it for a refined response.

### Voice Input
- Click the microphone icon and speak your query.
- The bot will transcribe and process your voice input.

---

## Troubleshooting

### Common Issues

#### **PostgreSQL Connection Errors**:
- Ensure the `DB_URI` in `.env` is correct.
- Verify that PostgreSQL is running and accessible.

#### **Gmail Authentication Errors**:
- Ensure you are using an App Password for Gmail (not your regular password).
- Verify that IMAP is enabled in your Gmail settings.

#### **Voice Input Not Working**:
- Ensure your browser supports the Web Speech API (e.g., Chrome, Edge).
- Grant microphone permissions when prompted.
- Check if your microphone is working properly.

#### **AI Response Errors**:
- Check if the Google API key is valid and has sufficient quota.
- Verify that the Tavily API key is correct.

---

## Contributing

Contributions are welcome! Please follow these steps:
1. Fork the repository.
2. Create a new branch for your feature or bugfix.
3. Submit a pull request with a detailed description of your changes.

---

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

---

## Acknowledgments
- **Google Gemini**: For providing the AI model.
- **Tavily**: For enabling web search capabilities.
- **FastAPI**: For the robust backend framework.
- **React**: For the intuitive frontend library.
- **Web Speech API**: For enabling speech-to-text functionality.

---

## Contact
For questions or feedback, please reach out to `masfanasrullahansari123@gmail.com`.

Enjoy using EmailBot! 🚀


# 🤖 AI Study Assistant – n8n Automation Project

An AI-powered Telegram Study Assistant built using **n8n, Google Gemini, Telegram Bot API, and Google Sheets**. This project helps students manage study tasks, generate AI-powered quizzes, evaluate answers, and track learning progress through a Telegram chatbot.

## 🔗 GitHub Repository

**Repository:** https://github.com/Prasadpatil3/IAI-PEC-T3-66

## 📌 Project Overview

The AI Study Assistant is an automated chatbot designed to make student life easier and more productive.

Students can interact with the bot through Telegram to manage academic tasks, generate topic-based multiple-choice quizzes, receive instant evaluation, and store performance records.

## ✨ Features

- **Telegram Bot Integration:** Interact with the assistant through Telegram.
- **Study Task Management:** Add academic tasks with deadlines.
- **Task Tracking:** View saved tasks and mark them as completed.
- **AI Quiz Generation:** Generate topic-based MCQs using Google Gemini.
- **Automatic Quiz Evaluation:** Check answers and calculate scores.
- **Instant Feedback:** Receive correct answers and explanations.
- **Quiz Session Management:** Store quiz sessions and results in Google Sheets.

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| n8n | Workflow automation |
| Telegram Bot API | Chatbot communication |
| Google Gemini API | AI-powered quiz generation |
| Google Sheets | Data storage |
| JavaScript | Data processing and answer evaluation |

## 🏗️ System Architecture

```text
             STUDENT
                |
                ▼
          TELEGRAM BOT
                |
                ▼
         TELEGRAM TRIGGER
                |
                ▼
           SWITCH NODE
                |
       ┌────────┼───────────┐
       ▼        ▼           ▼
   TASK       AI QUIZ     HELP / START
 MANAGEMENT  GENERATION
       |        |
       ▼        ▼
 GOOGLE      GOOGLE GEMINI
 SHEETS          |
       |         ▼
       |     QUIZ QUESTIONS
       |         |
       |         ▼
       |    TELEGRAM BOT
       |         |
       |         ▼
       |    USER ANSWERS
       |         |
       |         ▼
       |    ANSWER EVALUATION
       |         |
       |         ▼
       |     QUIZ RESULTS
       |         |
       └────┬────┘
            ▼
       GOOGLE SHEETS
            |
            ▼
      TELEGRAM RESPONSE
```

## 🤖 Available Bot Commands

| Command | Description |
|---|---|
| `/start` | Start the study assistant |
| `/help` | Display available commands |
| `/task` | Add a new study task |
| `/tasks` | View saved study tasks |
| `/complete 1` | Mark task number 1 as completed |
| `/quiz Operating Systems` | Generate an Operating Systems quiz |
| `/summarize` | Summarization command, if configured |

## 📊 Google Sheets Structure

The project uses three sheets to maintain records.

### 1. Tasks

| Column | Description |
|---|---|
| chat_id | Telegram user ID |
| task | Task description |
| deadline | Task deadline |
| status | Pending or completed |
| reminder_sent | Reminder tracking field |

### 2. QuizSessions

| Column | Description |
|---|---|
| chat_id | Telegram user ID |
| topic | Quiz topic |
| questions_json | Questions and correct answers |
| score | Quiz score |
| status | Quiz session status |

### 3. QuizResults

| Column | Description |
|---|---|
| chat_id | Telegram user ID |
| topic | Quiz topic |
| score | Number of correct answers |
| total | Total questions |
| status | Quiz completion status |
| completed_at | Completion timestamp |

## 📂 Project Structure

```text
IAI-PEC-T3-66/
│
├── README.md
│
├── workflow/
│   └── AI_Study_Assistant.json
│
└── screenshots/
    ├── workflow.png
    ├── telegram_bot.png
    └── quiz_results.png
```

*Adjust the folder and filenames to match the files actually uploaded to your repository.*

## ⚙️ Setup and Installation

### Prerequisites

- n8n account or self-hosted n8n instance
- Telegram account
- Telegram bot created using BotFather
- Google account with Google Sheets access
- Google Gemini API key from Google AI Studio

### Step 1: Clone the Repository

```bash
git clone https://github.com/Prasadpatil3/IAI-PEC-T3-66.git
```

Navigate to the project directory:

```bash
cd IAI-PEC-T3-66
```

### Step 2: Import the n8n Workflow

1. Open your n8n instance.
2. Navigate to the workflow editor.
3. Open the workflow menu.
4. Select **Import from File**.
5. Choose the exported n8n JSON file.
6. Save the imported workflow.

### Step 3: Configure Telegram

1. Create a Telegram bot using BotFather.
2. Generate your bot token.
3. Configure Telegram credentials in n8n.
4. Select the credentials in the Telegram nodes.

### Step 4: Configure Google Gemini

1. Visit [Google AI Studio](https://aistudio.google.com/).
2. Generate a Gemini API key.
3. Configure the Google Gemini Chat Model credentials in n8n.

### Step 5: Configure Google Sheets

1. Create a Google Spreadsheet named `AI Study Assistant Tasks`.
2. Create three sheets: `Tasks`, `QuizSessions`, and `QuizResults`.
3. Add the required column headers.
4. Configure Google Sheets credentials in n8n.
5. Select the spreadsheet and corresponding sheets in the workflow nodes.

### Step 6: Activate and Test

1. Verify all node connections.
2. Test the Telegram commands.
3. Verify data storage in Google Sheets.
4. Activate the workflow in n8n.

## 🔐 Security

- Never upload Telegram bot tokens or Gemini API keys to GitHub.
- Store API credentials securely using n8n credentials.
- Do not commit private Google Sheets information.
- Keep sensitive configuration details private.

## 🚀 Future Enhancements

- Automated study task deadline reminders.
- Daily study schedule generation.
- Quiz performance analytics and dashboards.
- Personalized learning recommendations.
- Subject-wise progress tracking.
- AI-generated study plans.
- PDF and document summarization.

## 🎯 Project Objective

The main objective is to develop an intelligent study assistant that combines artificial intelligence and workflow automation to simplify academic task management and improve student learning.

This project demonstrates the practical application of **Artificial Intelligence, API Integration, Workflow Automation, JavaScript, and Cloud-Based Data Management**.

## 👨‍💻 Author

**Prasad Patil**

B.Tech – Computer Science and Engineering

D. Y. Patil College of Engineering and Technology, Kolhapur

## 📚 References

- [n8n Documentation](https://docs.n8n.io/)
- [Telegram Bot API](https://core.telegram.org/bots/api)
- [Google Gemini API Documentation](https://ai.google.dev/gemini-api/docs)
- [Google Sheets API Documentation](https://developers.google.com/workspace/sheets/api)

---

⭐ If you find this project useful, consider giving the repository a star!

**GitHub Repository:** https://github.com/Prasadpatil3/IAI-PEC-T3-66

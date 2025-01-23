# AI Calling Agent for Blood Test Booking

## Overview
The AI Calling Agent is an innovative solution designed to streamline blood test bookings through natural, conversational interactions. Built using the MERN stack, this project integrates advanced technologies such as:

- **Speech-to-Text**
- **Text-to-Speech**
- **Natural Language Processing (NLP)**

This application connects to Twilio's media stream for real-time voice processing, enabling users to book tests seamlessly while offering personalized responses and automated SMS confirmations.

---

## Features

- **Automated Test Booking:**
  - Captures details such as phone number, city, test name, date, time, and collection type.
- **Multilingual Support:**
  - Default language is English, switches to Hindi/Hinglish when appropriate.
- **Personalized Interactions:**
  - Custom recommendations for test preparation and optimal timings.
- **Real-Time Voice Integration:**
  - Uses Twilio Media Stream for live voice interactions.
- **SMS Confirmation:**
  - Sends confirmation details via SMS upon booking completion.

---

## Installation Guide

### Prerequisites
Ensure you have the following installed on your system:
- Node.js (v16 or higher)
- Python (for FastAPI, if needed)
- MongoDB (running locally or remotely)
- Twilio account for Media Stream setup
- Fast2SMS account for SMS notifications

### Steps

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/your-username/ai-calling-agent.git
   cd ai-calling-agent
   ```

2. **Install Dependencies:**
   - **Backend:**
     ```bash
     pip install -r requirements.txt
     ```
   - **Frontend:**
     ```bash
     npm install
     ```

3. **Set Up Environment Variables:**
   Create a `.env` file in the root directory with the following variables:
   ```env
   OPENAI_API_KEY=your_openai_api_key
   SMS_KEY=your_fast2sms_api_key
   PORT=8010
   ```

4. **Run MongoDB:**
   Ensure MongoDB is running locally or provide a connection string to your database.

5. **Start the Backend Server:**
   ```bash
   uvicorn main:app --reload
   ```

6. **Start the Frontend Server:**
   ```bash
   npm start
   ```

7. **Twilio Configuration:**
   Set up Twilio Media Stream to point to the `/incoming-call` endpoint.

8. **Test the Application:**
   Open your browser or test the application via Twilio's Voice platform.

---

## Use Cases

### 1. **Healthcare:**
   - Automates blood test bookings and provides preparation guidelines.
   - Reduces manual effort for appointment scheduling.

### 2. **Customer Support:**
   - Answers routine healthcare queries with real-time interaction.
   - Escalates complex issues to human agents if needed.

### 3. **Feedback Collection:**
   - Captures user feedback on the services provided.

### 4. **Global Communication:**
   - Handles multilingual queries for global clients.

---

## API Endpoints

### 1. **Root Endpoint:**
   ```http
   GET /
   ```
   Returns a JSON message confirming the server is running.

### 2. **Incoming Call Handler:**
   ```http
   POST /incoming-call
   ```
   Processes incoming calls via Twilio and connects to the Media Stream.

### 3. **Media Stream WebSocket:**
   ```ws
   /media-stream
   ```
   Handles real-time WebSocket communication for audio processing.

---

## Future Enhancements

1. Integration with additional diagnostic labs.
2. Enhanced analytics for call summaries and customer insights.
3. AI-powered feedback analysis for continuous improvement.
4. Advanced sentiment analysis to adapt responses based on user emotions.


## Acknowledgements
- [Twilio](https://www.twilio.com/)
- [OpenAI](https://openai.com/)
- [Fast2SMS](https://www.fast2sms.com/)

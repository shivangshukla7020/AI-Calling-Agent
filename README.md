# AI Calling Agent for Blood Test Booking

## Overview
The AI Calling Agent is an innovative solution designed to streamline blood test bookings through natural, conversational interactions. Built using FastAPI and Twilio, this project integrates advanced technologies such as:

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
- Python (for FastAPI)
- Twilio account for Media Stream setup
- Fast2SMS account for SMS notifications
- **MongoDB is not required for this project** since it uses other methods for processing and managing data.

### Steps

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/your-username/ai-calling-agent.git
   cd ai-calling-agent

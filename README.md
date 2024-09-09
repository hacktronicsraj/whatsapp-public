# AI-Powered Fitness Coach on WhatsApp 🤖💪

This project showcases the creation of an AI-powered fitness coach chatbot that you interact with directly on WhatsApp! It's designed to deliver personalized fitness plans, offering workout routines, nutritional guidance, and even mindfulness tips, all tailored through the power of OpenAI and delivered seamlessly through WhatsApp.

## ✨ Features

* **Personalized Fitness Plans:**  Receive custom-tailored workout routines, dietary suggestions, and mindfulness exercises based on your preferences and goals.
* **AI-Driven Insights:** Benefit from the intelligence of OpenAI's GPT model to get insightful recommendations and guidance on your fitness journey.
* **Seamless WhatsApp Integration:** Interact with your AI fitness coach conveniently through your WhatsApp app, making it incredibly accessible.
* **Real-time Responses:**  Experience fluid and responsive interactions thanks to the power of webhooks, ensuring you get instant feedback and support.

## 🚀 Tech Stack

* **OpenAI Assistant API:** The brain of the operation, utilizing GPT's capabilities to generate personalized fitness advice.
* **Flask Framework (Python):** Provides a lightweight and efficient framework to handle web requests, responses, and the overall chatbot logic.
* **Meta's WhatsApp Business API:**  The bridge connecting the AI to WhatsApp, allowing for direct communication between users and the bot. 
* **ngrok:** Enables secure tunneling to your locally running Flask application, making it accessible from the internet for WhatsApp webhook integration. 

## 🛠️ Getting Started

1. **Set Up Your Environment:**
   - Install Python: Ensure you have Python installed on your system ([https://www.python.org/downloads/](https://www.python.org/downloads/)).
   - Create a virtual environment (recommended) and activate it: 
     ```bash
     python -m venv .venv
     source .venv/bin/activate 
     ```
   - Install project dependencies:
     ```bash
     pip install -r requirements.txt
     ```

2. **OpenAI Integration:**
   - Create an OpenAI account and obtain an API Key: [https://platform.openai.com/account/api-keys](https://platform.openai.com/account/api-keys).
   - Create a new Assistant in the OpenAI Playground: [https://platform.openai.com/assistants](https://platform.openai.com/assistants)
   - Store your OpenAI API key and the Assistant ID in an `.env` file (refer to `example.env` for the structure).

3. **Meta WhatsApp Business API Setup:**
   - Create a Meta Developer account: [https://developers.facebook.com/](https://developers.facebook.com/).
   - Create a new WhatsApp app and follow the instructions to connect a phone number (or use a test number).
   - In your app's dashboard, set up a webhook and point it to your ngrok URL (see below). 

4. **ngrok for Local Development:**
   - Download and install ngrok: [https://ngrok.com/](https://ngrok.com/)
   - Authenticate your ngrok account and start a tunnel to your local Flask app:
     ```bash
     ngrok http 5000  # Replace 5000 if your Flask app runs on a different port
     ``` 
   - Copy the HTTPS URL provided by ngrok — you'll need this for your WhatsApp webhook.

5. **Configure the Project:**
   -  Fill in the required variables in your `.env` file, including your OpenAI credentials, WhatsApp Business API details, and the ngrok URL you obtained.

6. **Run the Application:**
   - Start your Flask application:
      ```bash
      flask run
      ```

7. **Start Chatting!** 
   -  Once your Flask app is running and connected to WhatsApp, send a message to your WhatsApp Business number to start interacting with your AI-powered fitness coach!

## 📚  Resources

- **OpenAI Assistant API Documentation:** [https://platform.openai.com/docs/assistants/overview](https://platform.openai.com/docs/assistants/overview)
- **Flask Documentation:** [https://flask.palletsprojects.com/en/latest/](https://flask.palletsprojects.com/en/latest/)
- **Meta WhatsApp Business API Documentation:** [https://developers.facebook.com/docs/whatsapp](https://developers.facebook.com/docs/whatsapp)

## 🤝 Contributing

Contributions are welcome! Please open an issue or submit a pull request if you'd like to help improve this project. 

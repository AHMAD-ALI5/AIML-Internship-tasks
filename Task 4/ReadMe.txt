📌 Title

General Health Query Chatbot using LLM (Gemini API)

📖 Description

This project implements a simple AI-powered chatbot that answers general health-related questions using a Large Language Model (LLM). The chatbot is built using the Google Gemini API and uses prompt engineering techniques to ensure responses are clear, friendly, and safe.

The chatbot is designed to provide general health information only and avoids giving harmful or misleading medical advice.

🎯 Objectives
Build a chatbot using an LLM API
Apply prompt engineering for better responses
Implement safety filtering to prevent harmful outputs
Create a simple conversational system
🛠️ Tools & Technologies
Python
Jupyter Notebook
Google Gemini API
google-generativeai
📂 Project Structure
Task4_Health_Chatbot/
│
├── chatbot.ipynb
├── README.md
⚙️ Setup Instructions
🔹 1. Install Required Library
pip install google-generativeai
🔹 2. Get API Key
Visit: https://aistudio.google.com/app/apikey
Generate and copy your API key
🔹 3. Configure API
import google.generativeai as genai

genai.configure(api_key="YOUR_API_KEY") I have removed mine for privacy.
🔹 4. Initialize Model
model = genai.GenerativeModel("gemini-1.5-flash")
🤖 Chatbot Implementation
🔹 Chatbot Function
def chatbot(query):
    prompt = f"""
    You are a helpful and friendly medical assistant.

    Rules:
    - Provide general health information only
    - Do NOT give diagnosis
    - Do NOT prescribe medication
    - Keep answers simple and clear
    - Suggest consulting a doctor when needed

    User Question: {query}
    """

    response = model.generate_content(prompt)

    if not response.text:
        return "Sorry, I couldn't understand. Please try again."

    return response.text
🛡️ Safety Filtering

To prevent harmful or inappropriate medical advice:

def safety_filter(query):
    blocked_words = ["dose", "prescribe", "treatment plan", "exact medicine"]

    for word in blocked_words:
        if word in query.lower():
            return False
    return True


def safe_chatbot(query):
    if not safety_filter(query):
        return "⚠️ Please consult a doctor for medical advice."

    return chatbot(query)
▶️ How to Run
print(safe_chatbot("What causes a sore throat?"))
💬 Example Queries
Input	Output
What causes a sore throat?	General explanation of causes
Is paracetamol safe for children?	Safe, general guidance
Give me exact dosage	⚠️ Blocked by safety filter
🧠 Prompt Engineering Strategy

The chatbot uses structured prompts to:

Maintain a friendly tone
Ensure safe and responsible responses
Avoid medical diagnosis or prescriptions

Example prompt:

Act like a helpful medical assistant.
Provide general health information only.
Do not give prescriptions or diagnosis.
⚠️ Limitations
Not a replacement for professional medical advice
Responses depend on model accuracy
Basic keyword-based safety filter
✅ Skills Demonstrated
Prompt engineering
API integration
Safety handling in AI systems
Conversational chatbot design
🎯 Conclusion

This project demonstrates how LLMs like Gemini can be used to build safe and user-friendly chatbots for general health queries while maintaining ethical boundaries.
# AI Email Chatbot – Automated Inquiry Responder (n8n Workflow)
AI-powered email chatbot built with n8n that responds to user queries through email, provides detailed information about our platform, and automatically forwards personal queries to the correct team member.
# AI Email Chatbot

This project is an **AI-powered email chatbot** built using **n8n**, **OpenAI**, and email automation tools.  
It allows users to send questions through a website form or email, and the system automatically:

- Understands the user’s message  
- Responds with relevant information about your platform  
- Handles follow-up questions  
- Forwards detailed or personal queries to the right team member in your organization  

This workflow acts like a **smart email assistant** for businesses that want fast customer support without human agents.

---

## ⚙️ Key Features

- 📩 **Receives user questions** through form submissions (Webhook) or inbound email  
- 🧠 **Uses AI (OpenAI)** to analyze the query and generate a helpful email response  
- ℹ️ **Provides information about your platform**, services, pricing, process, or FAQs  
- 🔄 **Handles deeper follow-up questions** by keeping context  
- 👤 **Sends internal email alerts** to the right person on your team for special inquiries  
- 📊 Optional: Save all conversations to Google Sheets or your CRM  

---

## 🧠 Tech Stack / Tools Used

- **n8n** – Automation platform  
- **Webhook** – To receive messages from your website form  
- **OpenAI** – For intelligent, human-like email responses  
- **Send Email node** – For sending replies to users  
- **IF / Switch nodes** – To route messages based on query type  
- **Internal Email Notification** – To forward high-priority messages to a team member  

---

## 📂 Repository Contents

- `email-chatbot-workflow.json`  
  Exported n8n workflow that contains the full logic.

- `README.md`  
  This documentation file.

- `screenshots/` *(optional)*  
  Visual images of the workflow.

---

## 🚀 How It Works (Workflow Logic)

1. **User fills a form or sends an email**  
   - The message is captured via Webhook or IMAP.

2. **n8n receives the message**  
   - Data includes: name, email, message.

3. **AI processes the query**  
   - OpenAI analyzes user’s question.  
   - Generates a friendly, accurate reply about your platform.

4. **Decision Routing**  
   - If the question is general → AI sends automatic email reply.  
   - If the question is specific (pricing, partnership, personal issue, etc.) →  
     n8n forwards the message to the relevant team member (e.g., your email).

5. **Email Response Sent Back to User**  
   - The user receives a helpful, professional, AI-generated answer.

6. **Optional:**  
   - Store conversation details into Google Sheets / Notion / database.

---

## 🛠️ Setup Instructions

### 1. Import the Workflow

1. Open n8n  
2. Go to **Workflows → Import from File**  
3. Upload: `email-chatbot-workflow.json`  
4. Click **Import**

---

### 2. Configure the Webhook

- Open the **Webhook** node  
- Copy the URL  
- Add it to your website form (WordPress, Webflow, custom HTML, etc.)  
- Ensure the form sends:
  - name  
  - email  
  - message/query  

---

### 3. Configure OpenAI

- Add your API key in n8n Credentials  
- In the OpenAI node:
  - Add system prompt explaining your platform  
  - Customize tone (Friendly, Professional, Supportive)

Example system prompt:

> “You are an AI email support assistant for [Your Platform]. Answer questions accurately and politely.”

---

### 4. Configure Email Sending

- Open **Send Email** node  
- Add your email credentials (Gmail, SMTP, Outlook, etc.)  
- Set:
  - To: user email  
  - Body: OpenAI result + your signature  

---

### 5. Configure Internal Alerts

In the “Internal Notification” email node:

- Set recipient to your team email (Example: `support@company.com`)  
- Forward user’s message + AI analysis  
- Only triggers on high-priority queries

---

## ✨ Example Use Cases

- Customer support  
- Product information bot  
- Education platform assistant  
- Booking / appointment support  
- FAQ responder  
- Lead qualification  
- Internal team notifications  

---

## 🎓 Why This Project Is Valuable

This demonstrates:

- Real automation workflow building  
- Integration of AI + email + routing  
- Smart customer communication  
- Professional n8n architecture  
- Real-world business use cases  

Perfect for:

- GitHub portfolio  
- University applications  
- Freelance clients  
- Startup MVPs  

---

## 👤 Author

- **Name:** Rai Usman  
- **GitHub:** https://github.com/Usman-rai


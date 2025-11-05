<h1 align="center">🧠 Automation Task</h1>

<p align="center">
  All automation workflows are provided here — designed for seamless <b>RSS → Google Sheets</b> news automation using <b>LLMs</b>.
</p>

---
This n8n automation workflow automatically collects new articles from RSS feeds, summarizes them using an AI model, and stores the structured results in Google Sheets.

#### ⚙️ Workflow Overview:
1. **RSS Feed Triggers:**  
   Detects new items from connected RSS feeds.

2. **Duplicate Check:**  
   Looks up each article title in Google Sheets to ensure it hasn’t been processed before.

3. **AI Summarization:**  
   Sends the article content to an AI model (Groq LLM) to generate a structured summary in JSON format.

4. **Structured Parsing:**  
   Converts the AI-generated text into a clean, machine-readable structure.

5. **Data Storage:**  
   Appends the summarized data to a Google Sheet for record-keeping and analysis.

6. **Flow Control:**  
   Uses conditional and merge nodes to manage logic between feeds, processing, and output steps.

##### 🪄 Result:
A fully automated workflow that transforms raw RSS articles into organized, AI-generated summaries and logs them into a Google Sheet without manual intervention.

---

## ⚙️ Requirements

Before running this automation, make sure you have the following:

- 🔗 **RSS Feed Link**  
- 📄 **Google Sheets Authentication Credentials**  
- 🧩 **GROQ LLM API Key** (or any compatible LLM model API key)

---

## 🚀 How It Works

1. **Provide an RSS Feed URL** — This can be from a specific website or category where news articles are published.  
   You can use any **RSS Generator** tool to convert a website link into an RSS feed.

2. **Paste the RSS Link** into the **RSS Trigger Node**.  

3. **Authenticate Google Sheets Access** —  
   Add your credentials in the **Sheet Node** so the workflow can write the fetched and summarized content to your sheet.

4. **Integrate Your LLM** —  
   Paste your **GROQ API Key** (or another LLM provider key) in the **GROQ Chat Model Node** to enable summarization and structured parsing of content.

---

## 🧩 Output Structure

Each news item follows the structure below for this workflow:

```json
{
  "Title": "",
  "Context/Problem": "",
  "The Innovation": "",
  "Key Features": [],
  "Applications": "",
  "Challenges": "",
  "Future Outlook": "",
  "Conclusion": ""
}
```
---
### 🧠 Customization Guide

You can customize this output format in the following two nodes:

- **🧠 Structured Output Parser Node** — Define the schema or structure of your output.  
- **⚡ Basic LLM Chain Node** — Modify the prompt according to your desired output fields.

---

#### 🛠️ To Add or Remove Fields:

1. Open the **LLM Basic Chain Node** and update the prompt to match your desired structure.  
2. Update the **Structured Output Parser Node** to mirror that same structure.

> 💡 *Tip:* Keep both nodes synchronized to ensure smooth and consistent parsing of your custom fields.
---

### 🧠 n8n Workflow: Automated RSS Feed Summarizer to Google Sheets





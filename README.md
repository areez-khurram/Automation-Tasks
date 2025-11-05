<h1 align="center">🧠 Automation Tasks</h1>

<p align="center">
  All automation workflows are provided here — designed for seamless <b>RSS → Google Sheets</b> news automation using <b>LLMs</b>.
</p>

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
   The automation will:
   - 📥 Fetch the latest articles automatically  
   - ✂️ Extract and summarize the content  
   - 📊 Append the summarized news directly into your **Google Sheet**

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


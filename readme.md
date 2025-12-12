# 🧩 Automated Content Generation Workflow (n8n)
# demo video : https://youtu.be/IexrkruCKoc
This workflow automates **content creation, formatting, and multi-platform publishing** using AI, Google Workspace, and social APIs — all orchestrated in **n8n**.

---

## ⚙️ Overview

The workflow streamlines:
1. Collecting data from Google Sheets  
2. Generating AI-based content with Gemini  
3. Formatting and uploading it to Google Docs & Drive  
4. Auto-sharing to Discord and LinkedIn  

Perfect for social media managers, content creators, or teams automating daily post pipelines.

---

## 🗂️ Nodes Summary

| Node Name | Type | Purpose |
|------------|------|---------|
| **Google Sheets Trigger** | Trigger | Starts the workflow when a new row or change is detected in a connected Google Sheet. |
| **Google Gemini Chat Model** | AI (Gemini) | Generates main content ideas or drafts based on the input data from Sheets. |
| **writing style linkdn** | Google Docs | Applies formatting and writing style by creating or updating a Google Doc with AI-generated text. |
| **Generate an image** | AI (Gemini Image) | Creates an AI-generated image to accompany the written post or document. |
| **Upload file** | Google Drive | Uploads the generated file (image or doc) to a specified Drive folder for storage and sharing. |
| **Share file** | Google Drive | Changes Drive file permissions to make it viewable or shareable. |
| **Download file** | Google Drive | Downloads a file from Drive for posting to social media or for use in other nodes. |
| **Create a channel** | Discord | Creates a new channel in a selected Discord server for posting updates. |
| **Discord Message** | Discord | Sends automated messages or media to the selected Discord channel. |
| **Create a post** | LinkedIn | Publishes the final AI-generated content (text + image) as a LinkedIn post. |
| **Error/No Data Handling Nodes** | IF / Merge / Set / Wait | Handle fallback conditions, merge data from multiple sources, and control execution timing. |

---

## 🧠 Workflow Logic

1. **Trigger:** Google Sheets change starts the automation.  
2. **Generate:** Gemini model produces post content based on sheet inputs.  
3. **Format:** A Google Doc is updated with polished text.  
4. **Visuals:** Gemini creates an image matching the content.  
5. **Storage:** File uploaded and shared via Google Drive.  
6. **Publish:** Automatically posted to Discord and LinkedIn.  
7. **End:** Workflow completes or loops for the next entry.

---

## 🔐 Credentials Setup

Before importing this workflow, connect your own accounts:

- **Google Sheets API**
- **Google Drive API**
- **Google Docs API**
- **Gemini API (PaLM / Vertex AI)**
- **Discord OAuth2**
- **LinkedIn OAuth2**

> ⚠️ Credentials have been removed for security. Add your own connections in n8n after importing.

---

## 🧰 Environment Variables (Optional)

| Variable | Description |
|-----------|-------------|
| `GOOGLE_SHEET_ID` | The ID of your source Google Sheet. |
| `DRIVE_FOLDER_ID` | Folder where output files will be stored. |
| `DISCORD_CHANNEL_ID` | Target channel for automated posts. |
| `LINKEDIN_PERSON_ID` | Your LinkedIn account or page URN. |

---

## 🚀 Usage

1. Open **n8n** → Import this workflow JSON.  
2. Add required credentials under each Google/Discord/LinkedIn node.  
3. Update document IDs, folder IDs, and channel references.  
4. Test the trigger by updating your Google Sheet.  
5. Watch the automation generate, upload, and publish your content.

---

## 🧾 Notes

- Designed for creators automating **AI-assisted content pipelines**.  
- Uses **Gemini** for both text and image generation.  
- Fully modular — you can remove or replace any publish node (Discord, LinkedIn, etc).  
- Add error branches for custom logging or fallback behavior if needed.

---

## 🧑‍💻 Author

**Uzumaki-ak**  
*Fullstack Developer & Automation Enthusiast*  

---

## 🪪 License

MIT License © 2025 Uzumaki-ak

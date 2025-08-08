# MindLift — by Sentinel AI Systems

**Lift your AI's memory into the cloud.**  
MindLift is a simple, browser-based tool that transforms your OpenAI ChatGPT export into a clean, deduplicated JSON file, ready for upload to either **Zep** or **Supabase**.

![MindLift Screenshot](screenshot.png) <!-- Optional: Add screenshot file in repo -->

---

## 🚀 Features
- **No Install Needed** — Runs entirely in your browser via GitHub Pages.
- **Zip Import** — Upload the `.zip` file you receive from OpenAI’s data export.
- **Auto Extraction** — Finds and parses the `conversations.json` file automatically.
- **Deduplication** — Removes duplicate messages to keep your archive clean.
- **Target Formatting** — Choose between:
  - **Zep**: Session-based format
  - **Supabase**: Conversation/message bulk insert format
- **Instant Download** — Get a single JSON file ready for your chosen platform.
- **Cyberpunk Styling** — Matches the neon, black-background style of the *Em Dash Killer* suite.

---

## 🛠 How to Use
1. **Export your data from OpenAI**  
   - Go to your ChatGPT settings → *Export data*.  
   - Wait for the email, then download the `.zip` file.

2. **Open MindLift**  
   - Visit: [https://jkh2.github.io/mindlift/](https://YOUR-GITHUB-USERNAME.github.io/mindlift/)  
   - *(Replace `YOUR-GITHUB-USERNAME` with your GitHub username)*

3. **Select your target platform**  
   - Use the dropdown to choose **Zep** or **Supabase**.

4. **Upload your `.zip` file**  
   - Click *Choose File* and select the OpenAI export zip.

5. **Download processed JSON**  
   - MindLift will unzip, deduplicate, format, and download your file — ready to upload to your chosen database.

---

## 📂 File Output

**For Zep**
```json
{
  "kind": "zep.sessions",
  "sessions": [
    {
      "id": "...",
      "title": "...",
      "messages": [
        { "role": "user", "content": "...", "metadata": { "tags": ["openai-export"] } }
      ]
    }
  ]
}

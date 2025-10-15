# 🤖 Spiffy

Spiffy is my custom AI companion project — part wit, part machine, and powered by n8n workflows, Airtable memory, and a sprinkle of sarcasm. This repo serves as the source of truth for workflows, assets, and documentation.

---

## 📂 Repo Structure

```
spiffy/
├─ workflows/      # n8n workflow exports (JSON files)
├─ assets/         # Stickers, icons, branding
├─ docs/           # Setup notes and guides
└─ README.md       # You are here
```

---

## 🚀 Workflows
All n8n workflows are stored as JSON exports in `/workflows/`.  
Examples:
- `telegram_master.json` → main Telegram interface
- `nightly_memory.json` → memory summarizer
- `random_messages.json` → occasional Spiffy one-liners

To import:  
1. Open n8n → Workflows → Import from File.  
2. Choose the JSON file from this repo.  

---

## 🎨 Assets
Spiffy’s branding lives in `/assets/`:  
- Stickers  
- Logos  
- Any other visuals  

These can be used across Telegram, GitHub, and future front-ends.

---

## 🛠 Setup
1. Clone this repo:
   ```bash
   git clone https://github.com/<your-username>/spiffy.git
   cd spiffy
   ```
2. Import workflows into n8n as needed.  
3. Reference `/docs/` for Airtable schema, environment variables, or setup guides.  

---

## 📌 Notes
- Keep secrets out of this repo. Use `.env` files locally.  
- Contributions (even from future-me) should follow clear commit messages:  
  ```
  feat: add new workflow for Telegram status
  fix: correct Airtable schema mapping
  chore: update docs
  ```

---

💡 *Spiffy may be sarcastic, but this repo should stay clean and organized.*

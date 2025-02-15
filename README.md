# 📖 GitHub Obsidian Project

## 📌 Overview
This repository is dedicated to managing and automating workflows for **Obsidian**, a powerful knowledge management and note-taking application. It helps in **version-controlling notes, automating backups, and syncing with GitHub**.

## 🚀 Features
✅ **Automatic Note Syncing** – Syncs your Obsidian vault with GitHub  
✅ **Version Control for Notes** – Track changes and restore older versions  
✅ **Automated Backup** – Schedule regular backups using GitHub Actions  
✅ **Multi-Device Access** – Keep notes updated across multiple machines  

## 🛠️ Installation & Setup

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/yourusername/obsidian-git-sync.git
cd obsidian-git-sync
```

### 2️⃣ Set Up Obsidian Vault
- Open **Obsidian** and locate your vault directory.
- Copy your vault into the cloned repository.

### 3️⃣ Configure Git
```bash
git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"
```

### 4️⃣ Automate Sync with GitHub Actions (Optional)
- Set up a **GitHub Action** to commit and push changes periodically.
- Create a `.github/workflows/sync.yml` file with:
  ```yaml
  name: Sync Obsidian Notes
  on:
    schedule:
      - cron: '0 * * * *'  # Runs every hour
  jobs:
    sync:
      runs-on: ubuntu-latest
      steps:
        - name: Checkout repository
          uses: actions/checkout@v3
        - name: Commit and Push Changes
          run: |
            git add .
            git commit -m "Auto-sync notes"
            git push
  ```

### 5️⃣ Manual Syncing Commands
```bash
git add .
git commit -m "Updated notes"
git push origin main
```

## 🤝 Contributing
Feel free to fork this repo and submit PRs for improvements!

## 📜 License
This project is open-source and available under the **MIT License**.


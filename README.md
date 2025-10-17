# Personal RAG Assistant
## Create project by using Git
#### Purpose: This project is created to build a Retrieval-Augmented Generation (RAG) assistant with version control using Git and GitHub.
1. Initialize Local Git Repository
```
# create folder & go into
mkdir personal-rag-assistant
cd personal-rag-assistant

# (optional) create vm
python -m venv venv
.\venv\Scripts\Activate.ps1

# create some default file
ni app.py -ItemType File
ni README.md -ItemType File
ni requirements.txt -ItemType File
ni .gitignore -ItemType File
```
2. Setup ```.gitignore```
Exclude sensitive or unnecessary files such as .env, cache, and virtual environments.
```
# Python
__pycache__/
*.pyc
*.pyo
*.pyd
venv/

# Env
.env
.env.*

# OS / Tooling
.DS_Store
.streamlit/

# Data
data/
```
3. Initialize Git and First Commit
```
git init
git status

# Add simple README content
echo "# Personal RAG Assistant" >> README.md

# Stage and commit files
git add .
git commit -m "chore: initialize project folder and basic files"
```
4. Create GitHub Repository and Link Remote
```
# go to GitHub → New Repository
# copy the HTTPS link and run:
git remote add origin https://github.com/katehuangishere/personal-rag-assistant.git
git branch -M main
git push -u origin main
```
```
# success message:
User-Kate@LAPTOP-TIS5R8N5 MINGW64 ~/personal-rag-assistant (main)
$ git push -u origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (5/5), 503 bytes | 167.00 KiB/s, done.
Total 5 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/katehuangishere/personal-rag-assistant.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
```
5. Daily Development Workflow
```
# Create a feature branch
git checkout -b feature/upload-and-embed

# Make changes, then commit
git add .
git commit -m "feat: add file upload and embedding pipeline"

# Merge back into main (locally or via PR)
git checkout main
git pull origin main        # Sync latest changes
git merge feature/upload-and-embed

# Push to GitHub
git push origin main
```
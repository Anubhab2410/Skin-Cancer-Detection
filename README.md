Skin Cancer Detection - README

Overview
This repository contains a Streamlit web app for skin lesion classification (Skin Cancer Detection). The Streamlit entrypoint is at: Skin_Cancer_Detection/app.py

Prerequisites
- Windows machine
- Python 3.8+
- Recommended: virtual environment
- Streamlit and other dependencies listed in requirements.txt
- Large model files (.h5) are included in model/ but it's recommended to use Git LFS for those files

Quick setup (Windows)
1. Open PowerShell or Command Prompt at repository root (f:\Skin_Cancer_Detection)
2. Create and activate venv:
   python -m venv .venv
   .\.venv\Scripts\Activate.ps1   # PowerShell
   # or
   .\.venv\Scripts\activate.bat   # Command Prompt
3. Install dependencies:
   pip install -r Skin_Cancer_Detection/requirements.txt
4. (Optional) Install Git LFS before pushing large models:
   git lfs install
   git lfs track "*.h5"
   git add .gitattributes

Run the app
From repository root:
streamlit run Skin_Cancer_Detection/app.py

Notes
- Do not commit large binary model files without Git LFS or alternative hosting (releases, cloud storage).
- Static assets are in Skin_Cancer_Detection/assets/
- Pages are implemented under Skin_Cancer_Detection/streamlit_pages/

License
Add an appropriate license file (LICENSE) if you plan to publish the repository publicly.

If you want, I can create a Markdown README.md instead or add CI/GitHub Actions, a .gitignore, or a .gitattributes file for Git LFS.

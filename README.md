Skin Cancer Detection - README

Project
A Streamlit web application for skin lesion classification using a trained deep learning model.
Entry point: Skin_Cancer_Detection/app.py

Key features
- Web UI built with Streamlit
- Image upload and prediction page
- Chat-like expert guidance page
- Team information page
- Includes model file(s) in model/ (large binaries) and example dataset

Repository structure (important files)
- Skin_Cancer_Detection/app.py            - Streamlit entrypoint and page routing
- Skin_Cancer_Detection/streamlit_pages/  - Page modules (home, predict, chat, team)
- Skin_Cancer_Detection/assets/           - CSS and static assets
- model/                                  - Trained model files (.h5) — large, consider Git LFS
- data/                                   - Example CSVs and datasets
- requirements.txt                         - Python dependencies

Prerequisites (Windows)
- Python 3.8+
- Git
- (Recommended) Git LFS for large model files
- Virtual environment tool (venv)

Quick setup (from repo root: f:\Skin_Cancer_Detection)
1. Create + activate virtual env (PowerShell)
   python -m venv .venv
   .\.venv\Scripts\Activate.ps1

2. Install dependencies
   pip install -r Skin_Cancer_Detection/requirements.txt

3. If you will push model files to GitHub, enable Git LFS:
   git lfs install
   git lfs track "*.h5"
   git add .gitattributes
   git commit -m "Track .h5 with Git LFS"

Run the app (from repo root)
streamlit run Skin_Cancer_Detection/app.py

Notes on model files
- .h5 and other large binaries should not be committed to regular Git history.
- Options:
  1) Use Git LFS (preferred for GitHub).
  2) Host model artifacts in cloud storage (S3, Google Drive) and download at runtime.
  3) Provide a small placeholder model in repo and document where to place a full model.

Recommended .gitignore entries
__pycache__/
*.pyc
.venv/
.vscode/
*.h5
.ipynb_checkpoints
.DS_Store

Testing & development tips
- Run Streamlit from the project root so relative asset paths work.
- Use smaller test images while developing to speed up inference.
- Add logging around model load/predict to help debug.

Contributing
- Create an issue for significant changes.
- Fork the repo, create a branch, and open a pull request.

License & attribution
- Add a LICENSE file appropriate for your project before publishing.
- If using public datasets (e.g., ISIC), follow their usage/license terms and cite appropriately.

Contact / Maintainer
- Anubhab Bhattacharjee(anubhabbhattacharjee07@gmail.com)


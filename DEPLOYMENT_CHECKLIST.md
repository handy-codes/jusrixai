# Streamlit Cloud Deployment Checklist

## 1. Environment Setup
- [x] Removed python-dotenv dependency
- [x] Added Streamlit secrets management
- [x] Updated PyMuPDF to stable version (1.23.8)

## 2. Required Files
- [ ] app.py
- [ ] requirements.txt
- [ ] .streamlit/secrets.toml
- [ ] modules/chat_assistant.py
- [ ] modules/document_reviewer.py
- [ ] modules/law_search.py
- [ ] modules/legal_template.py
- [ ] modules/query_builder.py

## 3. Dependencies Check
- [ ] streamlit==1.35.0
- [ ] openai==0.27.6
- [ ] langchain==0.2.0
- [ ] PyMuPDF==1.23.8
- [ ] pdfminer.six==20221105
- [ ] docx2txt==0.8
- [ ] python-docx==1.1.0
- [ ] pyttsx3==2.90
- [ ] chardet==5.2.0
- [ ] pytesseract==0.3.10
- [ ] opencv-python==4.9.0.80
- [ ] httpx==0.27.0

## 4. Deployment Steps
1. [ ] Push all changes to GitHub
2. [ ] Go to share.streamlit.io
3. [ ] Create/Update app
4. [ ] Add secrets in Streamlit Cloud dashboard:
   ```toml
   GROQ_API_KEY = "your-groq-api-key"
   OPENAI_API_KEY = "your-openai-api-key"
   ```
5. [ ] Deploy app

## 5. Common Issues to Check
- [ ] All imports use relative paths
- [ ] No hardcoded paths
- [ ] All environment variables moved to secrets
- [ ] No local file system dependencies
- [ ] All required packages in requirements.txt
- [ ] No version conflicts in requirements.txt

## 6. Testing Steps
1. [ ] Test locally with `streamlit run app.py`
2. [ ] Check all features work:
   - [ ] Chat Assistant
   - [ ] Document Review
   - [ ] Law Search
   - [ ] Legal Template
   - [ ] Query Builder
3. [ ] Verify API keys work in production
4. [ ] Check error logging

## 7. Troubleshooting
If deployment fails:
1. Check Streamlit Cloud logs
2. Verify all secrets are set
3. Check Python version compatibility
4. Verify all dependencies are installed
5. Check for any missing files 
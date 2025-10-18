# Generative AI Detection  

![Demo](https://github.com/always-nidhi/Gen-AI-Detection/raw/main/Screenshot%20(366).png)  
![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)  
![React](https://img.shields.io/badge/ReactJS-17.0-blue?logo=react)  

Detects whether a text is **human-written** or **AI-generated** using GPT-2, with a **ReactJS frontend** and **Python backend**. Developed for the **Voight-Kampff Generative AI Authorship Verification 2024** challenge.

---

## Features
- Classifies text as **human-written** or **AI-generated**  
- Calculates **Perplexity** and **Burstiness** metrics  
- **ReactJS frontend** for a user-friendly interface  
- **Python Flask backend** for model inference  

---

## Modules and Libraries
- **Flask**: Python web framework for API endpoints  
- **Flask-CORS**: Enables cross-origin requests  
- **PyTorch**: Runs GPT-2 model  
- **Transformers (Hugging Face)**: GPT-2 tokenizer and model  
- **re (Regular Expressions)**: Text processing  
- **OrderedDict (collections)**: Maintains structured results  

---

## Algorithm
- **Perplexity**: Measures text predictability; lower values suggest human text.  
- **Burstiness**: Measures variation in predictability across lines; high values indicate AI-generated content.  

**Threshold Table**:

| Perplexity | Prediction            |
|------------|---------------------|
| < 60       | Likely AI-generated |
| 60–80      | Likely AI           |
| > 80       | Likely Human        |

- API returns label along with **perplexity** and **burstiness** scores.  

---

## Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/Generative-AI-Detection.git
cd Generative-AI-Detection

# Install frontend dependencies
cd frontend
npm install

# Install backend dependencies
cd ../server
pip install -r requirements.txt

# Start backend server
python app.py

# Start frontend server
npm start

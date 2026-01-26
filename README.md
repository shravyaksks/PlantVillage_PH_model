 PlantVillage PH Model 🌱

A Flask-based web application for plant disease detection using a trained Keras model.  
This project leverages deep learning to classify plant leaf images and provide diagnostic predictions.

 🚀 Features
- Flask web server with HTML/CSS frontend
- Image upload interface for predictions
- Pre-trained Keras model (`PH_model.keras`)
- Responsive design with `style.css`
- Deployment-ready with **Procfile** for Gunicorn

 📂 Project Structure

PlantVillage_PH_model/
│
├── app_ph_model_ai.py        # Main Flask application
├── PH_model.keras            # Trained Keras model
├── requirements.txt          # Python dependencies
├── Procfile                  # Deployment configuration for Gunicorn
├── templates/
│   └── index_ph_model.html   # Frontend HTML template
├── style.css                 # Custom CSS styling
└── README.md                 # Project documentation

⚙️ Installation & Local Setup
1. Clone the repository
   git clone https://github.com/shravyaksks/PlantVillage_PH_model.git
   cd PlantVillage_PH_model

2. Create a virtual environment
   python -m venv venv
   venv\Scripts\activate   # Windows
   source venv/bin/activate # Linux/Mac

3. Install dependencies
   pip install --upgrade pip
   pip install -r requirements.txt
   
4. Run the Flask app
   python app_ph_model_ai.py
   The app will start at:
   http://127.0.0.1:5000/
   
 🌐 Deployment

 Render / PythonAnywhere
- Procfile is included for Gunicorn:
  
  web: gunicorn app_ph_model_ai:app
  
- Ensure `requirements.txt` is installed in your environment.
- Update WSGI or Start Command to point to `app_ph_model_ai:app`.

 📦 Requirements
- Python 3.10+
- Flask
- TensorFlow / Keras
- Pillow
- NumPy

 🖼️ Usage
1. Open the app in your browser.
2. Upload a plant leaf image.
3. The model predicts the disease class and displays the result.

## 📌 Notes
- Ensure `PH_model.keras` is present in the project root.
- If deploying on PythonAnywhere, update the WSGI file to import:
  python
  from app_ph_model_ai import app as application
  
 🤝 Contributing
Pull requests are welcome! For major changes, please open an issue first to discuss what you’d like to change.

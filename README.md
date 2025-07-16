
# mental-health
This is my local README.
# Mental Health Companion - Therapy Chatbot

A smart, empathetic chatbot designed to provide emotional support and detect stress levels from user messages. This web application offers a safe space for users to express their feelings and receive supportive responses along with helpful mental health resources.

## 🌟 Features

### 🤖 Intelligent Stress Detection
- **Keyword Analysis**: Detects stress indicators in user messages
- **Stress Level Tracking**: Real-time stress level visualization with color-coded progress bar
- **Contextual Responses**: Provides appropriate support based on detected stress levels

### 💬 Supportive Conversation
- **Empathetic Responses**: AI-generated supportive messages tailored to user's emotional state
- **Topic-Specific Support**: Specialized responses for anxiety, depression, work stress, and more
- **Conversation History**: Maintains chat history for continuity

### 🧘‍♀️ Mental Health Resources
- **Breathing Exercises**: Interactive 4-7-8 breathing technique with animated guidance
- **Grounding Techniques**: 5-4-3-2-1 sensory grounding exercise
- **Positive Affirmations**: Curated list of uplifting affirmations
- **Quick Actions**: Pre-defined buttons for common mental health topics

### 🎨 Beautiful, Calming UI
- **Modern Design**: Clean, soothing interface with gradient backgrounds
- **Responsive Layout**: Works perfectly on desktop and mobile devices
- **Accessibility**: Easy-to-use interface with clear visual indicators
- **Smooth Animations**: Gentle transitions and animations for a calming experience

## 🚀 How to Use

### Quick Start (Basic Mode)
1. **Open the Application**: Simply open `index.html` in your web browser
2. **Start Chatting**: Type your message in the text area and press Enter or click the send button
3. **Use Quick Actions**: Click on the quick action buttons for common topics
4. **Access Resources**: Use the sidebar resources for breathing exercises, grounding techniques, and affirmations
5. **Monitor Stress Level**: Watch the stress level indicator in the chat header

### Advanced Mode (with ML Training)

#### Basic ML Training (Emotion Dataset Only)
1. **Install Dependencies**: Run `python setup.py` to install requirements and train the model
2. **Start API Server** (Optional): Run `python api_server.py` for real-time ML predictions
3. **Use Enhanced Chatbot**: The chatbot will now use ML-trained keywords for better stress detection
4. **API Integration**: Enable ML API by setting `window.useMLAPI = true` and `window.mlAPIEndpoint = 'http://localhost:5000'` in browser console

#### Enhanced ML Training (with Local Dataset)
1. **Install Dependencies**: Run `python enhanced_setup.py --mode enhanced` to train with your local dataset
2. **Start Enhanced API Server** (Optional): Run `python enhanced_api_server.py` for enhanced ML predictions
3. **Use Enhanced Chatbot**: The chatbot will use both emotion dataset and your local dataset for better accuracy
4. **API Integration**: Enable enhanced ML API by setting `window.useMLAPI = true` and `window.mlAPIEndpoint = 'http://localhost:5001'` in browser console

#### Training Modes
- `python enhanced_setup.py --mode basic` - Train only with emotion dataset
- `python enhanced_setup.py --mode enhanced` - Train with your local dataset + emotion dataset
- `python enhanced_setup.py --mode both` - Train both models (default)
- `python enhanced_setup.py --local-dataset-path "your/path"` - Specify custom dataset path

## 📁 Project Structure

```
mental-health-chatbot/
├── index.html                           # Main HTML file with the chat interface
├── styles.css                           # Comprehensive CSS styling
├── script.js                            # JavaScript logic for chatbot functionality
├── train_model.py                       # Basic ML training script using emotion dataset
├── train_with_local_dataset.py          # Enhanced ML training with local dataset
├── api_server.py                        # Basic Flask API server for real-time predictions
├── enhanced_api_server.py               # Enhanced API server with multiple models
├── setup.py                             # Basic setup script for dependencies and training
├── enhanced_setup.py                    # Enhanced setup script with local dataset support
├── requirements.txt                     # Python dependencies
├── training_data.js                     # Generated basic ML training data for JavaScript
├── enhanced_training_data.js            # Generated enhanced ML training data for JavaScript
├── mental_health_model_*.pkl           # Basic trained ML model files
├── enhanced_mental_health_model_*.pkl  # Enhanced trained ML model files
└── README.md                           # Project documentation
```

## 🛠️ Technical Details

### Stress Detection Algorithm
The chatbot uses a sophisticated keyword-based analysis system with optional ML enhancement:

#### Basic Keyword Analysis
- **High Stress Keywords**: anxiety, panic, overwhelmed, terrified, desperate, hopeless, suicidal, etc.
- **Medium Stress Keywords**: stressed, worried, nervous, tense, frustrated, angry, sad, depressed, etc.
- **Low Stress Keywords**: concerned, uneasy, bothered, annoyed, irritated, etc.

#### ML-Enhanced Detection (Optional)
- **Trained on Emotion Dataset**: Uses the dair-ai/emotion dataset for improved accuracy
- **TF-IDF Vectorization**: Converts text to numerical features
- **Random Forest Classifier**: Predicts stress levels with confidence scores
- **Real-time API**: Optional Flask server for live ML predictions

### Response Generation
- **Contextual Responses**: Different response sets for high, medium, and low stress levels
- **Topic-Specific Responses**: Specialized responses for anxiety, depression, work stress, and breathing exercises
- **Supportive Language**: All responses use empathetic, validating language

### Interactive Features
- **Real-time Stress Tracking**: Visual stress level indicator with color-coded progress bar
- **Breathing Exercise**: Animated 4-7-8 breathing technique with visual guidance
- **Grounding Exercise**: Step-by-step 5-4-3-2-1 sensory grounding technique
- **Affirmations**: Curated list of positive affirmations for mental wellness

## 🎯 Use Cases

### For Individuals
- **Emotional Support**: Get immediate, non-judgmental support when feeling overwhelmed
- **Stress Management**: Learn and practice breathing and grounding techniques
- **Self-Care**: Access positive affirmations and mental health resources
- **Crisis Support**: Receive immediate support during difficult moments

### For Mental Health Professionals
- **Client Support**: Provide clients with a tool for between-session support
- **Stress Assessment**: Use as a preliminary stress level assessment tool
- **Resource Sharing**: Share breathing and grounding techniques with clients

## ⚠️ Important Disclaimer

This chatbot is designed to provide emotional support and is **NOT a replacement for professional mental health care**. 

**If you are experiencing:**
- Thoughts of self-harm or suicide
- Severe depression or anxiety
- Mental health crisis

**Please contact:**
- Emergency services (911 in the US)
- National Suicide Prevention Lifeline: 988
- Crisis Text Line: Text HOME to 741741
- Your mental health professional

## 🔧 Customization

### Adding New Keywords
Edit the `stressKeywords` object in `script.js`:

```javascript
this.stressKeywords = {
    high: ['your', 'new', 'keywords'],
    medium: ['your', 'new', 'keywords'],
    low: ['your', 'new', 'keywords']
};
```

### Adding New Responses
Edit the `supportiveResponses` object in `script.js`:

```javascript
this.supportiveResponses = {
    high: ['your', 'new', 'responses'],
    medium: ['your', 'new', 'responses'],
    low: ['your', 'new', 'responses']
};
```

### Styling Customization
Modify `styles.css` to change colors, fonts, and layout:

```css
:root {
    --primary-color: #667eea;
    --secondary-color: #764ba2;
    --success-color: #4CAF50;
    --warning-color: #FF9800;
    --danger-color: #F44336;
}
```

## 🌐 Browser Compatibility

- ✅ Chrome (recommended)
- ✅ Firefox
- ✅ Safari
- ✅ Edge
- ✅ Mobile browsers

## 📱 Mobile Responsive

The application is fully responsive and works great on:
- Smartphones
- Tablets
- Desktop computers

## 🤝 Contributing

Feel free to contribute to this project by:
1. Adding new stress detection keywords
2. Improving response generation
3. Adding new mental health resources
4. Enhancing the UI/UX
5. Adding new features

## 📄 License

This project is open source and available under the MIT License.

## 🙏 Acknowledgments

- Mental health professionals for guidance on supportive language
- Breathing and grounding technique resources
- Positive psychology research for affirmations
- Web development community for best practices

---

**Remember**: You are not alone, and it's okay to ask for help. This chatbot is here to support you, but professional mental health care is always the best option for ongoing support. 

---

Here’s how to deploy your project on **Render**:

---

## 1. **Push Your Code to GitHub**
You’ve already done this! ✅

---

## 2. **Create a New Web Service on Render**

1. Go to [https://dashboard.render.com/](https://dashboard.render.com/) and log in.
2. Click **New +** and select **Web Service**.
3. **Connect your GitHub account** if you haven’t already.
4. **Select your repository** (`sredhavainban/mental-health`).

---

## 3. **Configure Your Service**

- **Name:** Choose a name for your service.
- **Branch:** `main`
- **Build Command:**  
  ```
  pip install -r requirements.txt
  ```
- **Start Command:**  
  For Flask, if your main file is `app.py` and your Flask app is named `app`:
  ```
  gunicorn app:app
  ```
  (Change `app:app` if your file or app variable is named differently.)

- **Python Version:**  
  If you need a specific version, make sure you have a `runtime.txt` file in your repo (e.g., `python-3.10.13`).

- **Root Directory:**  
  Leave blank unless your code is in a subfolder.

---

## 4. **Deploy**

- Click **Create Web Service**.
- Render will clone your repo, install dependencies, and start your app.
- You’ll see build logs and a public URL when it’s live.

---

## 5. **If You See Errors**
- Copy the error message and paste it here. I’ll help you fix it!

---

### **Summary**
1. Go to Render.com → New Web Service
2. Connect your GitHub repo
3. Set build/start commands
4. Deploy!

If you need help with the **Start Command** or see any errors, let me know your backend framework (Flask, FastAPI, etc.) and your main file name, and I’ll give you the exact command to use!

---

## How to Fix
### 1. **Remove `pywin32` from `requirements.txt`**
- Open your `requirements.txt` file.
- Delete any line that says `pywin32` or `pywin32==310`.
- Save the file.

### 2. **Specify a Supported Python Version**
- In your project root, create a file called `runtime.txt` (if it doesn't exist).
- Add this line to `runtime.txt`:
  ```
  python-3.10.13
  ```
  or
  ```
  python-3.9.19
  ```
  (Choose a version supported by your dependencies.)

### 3. **Commit and Push Your Changes**
```bash
git add requirements.txt runtime.txt
git commit -m "Remove pywin32 and specify Python version"
git push origin main
```

### 4. **Redeploy on Render**

---

## **Summary**
- Remove `pywin32` from `requirements.txt`.
- Add `runtime.txt` with a supported Python version (3.10 or 3.9).
- Commit, push, and redeploy.

---

If you need help editing your files or want a sample `requirements.txt` or `runtime.txt`, let me know!

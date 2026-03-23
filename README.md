# 🏥 HEAL MATRIX - AI-Powered Multi-Agent Healthcare Platform

[![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)](https://www.python.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aliasjad6536/AliAsjad/blob/main/heal_matrix_3.ipynb)
[![Gradio](https://img.shields.io/badge/Demo-Gradio-orange.svg)](https://065ef6c540ed40fb05.gradio.live/)

> An intelligent multi-agent healthcare system integrating LangGraph, Computer Vision, Voice AI, and Location Services for comprehensive healthcare management.

---

## 🌟 Features

- **🚨 Emergency Response Agent** - Immediate first-aid guidance and nearest facility locator
- **💬 Medical Consultation Agent** - AI-powered symptom analysis and health advice
- **📅 Appointment Scheduling Agent** - Smart appointment booking and management
- **💊 Prescription Management Agent** - Medication information and pharmacy finder
- **📊 Health Monitoring Agent** - Track vitals and health metrics with trend analysis
- **🖼️ Computer Vision** - Medical image analysis using CLIP model
- **🔊 Voice Interface** - Text-to-Speech responses for accessibility
- **📍 Location Services** - Real-time facility search with Google Maps integration

---

## 🎯 Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                    Gradio Web Interface                      │
│              (Text Input + Image Upload + Voice)             │
└───────────────────────────┬─────────────────────────────────┘
                            │
                            ▼
┌─────────────────────────────────────────────────────────────┐
│                  LangGraph Orchestration                     │
│                    (State Management)                        │
└───────────────────────────┬─────────────────────────────────┘
                            │
        ┌───────────────────┼───────────────────┐
        │                   │                   │
        ▼                   ▼                   ▼
┌──────────────┐    ┌──────────────┐    ┌──────────────┐
│   Router     │    │  Emergency   │    │   Medical    │
│    Agent     │───▶│    Agent     │    │ Consultation │
└──────────────┘    └──────────────┘    └──────────────┘
        │                   │                   │
        ▼                   ▼                   ▼
┌──────────────┐    ┌──────────────┐    ┌──────────────┐
│ Appointment  │    │Prescription  │    │   Health     │
│    Agent     │    │    Agent     │    │  Monitoring  │
└──────────────┘    └──────────────┘    └──────────────┘
        │                   │                   │
        └───────────────────┴───────────────────┘
                            │
                            ▼
┌─────────────────────────────────────────────────────────────┐
│           AI Services & External APIs                        │
│  • Ollama (Gemma 2B LLM)                                    │
│  • CLIP (Computer Vision)                                   │
│  • Google TTS (Voice Synthesis)                             │
│  • Google Maps API (Geolocation)                            │
└─────────────────────────────────────────────────────────────┘
```

---

## 🚀 Quick Start

### Prerequisites

- Python 3.10 or higher
- Google Colab account (recommended)
- Google Maps API key
- GPU access (optional but recommended)

### Installation

#### Option 1: Run on Google Colab (Recommended)

1. **Open the notebook in Colab:**
   
   [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aliasjad6536/AliAsjad/blob/main/heal_matrix_3.ipynb)

2. **Run all cells sequentially**

3. **Enter your Google Maps API key** when prompted

4. **Access the Gradio interface** via the generated public link

#### Option 2: Local Installation

```bash
# Clone the repository
git clone https://github.com/aliasjad6536/AliAsjad.git
cd AliAsjad

# Install dependencies
pip install -r requirements.txt

# Install and start Ollama
curl -fsSL https://ollama.com/install.sh | sh
ollama serve &
ollama pull gemma2:2b

# Run the notebook
jupyter notebook heal_matrix_3.ipynb
```

---

## 📖 Usage

### Basic Usage

```python
# Initialize the system
from heal_matrix import process_query

# Text query
response, audio = process_query(
    user_input="I have a headache and fever",
    location="New York, NY"
)

# With image
response, audio = process_query(
    user_input="What's wrong with this rash?",
    image_path="skin_rash.jpg",
    location="Los Angeles, CA"
)
```

### Example Queries

- **Emergency:** "Help! I'm having chest pain"
- **Medical:** "What are the symptoms of diabetes?"
- **Appointment:** "Book a dentist appointment for next week"
- **Prescription:** "What are the side effects of ibuprofen?"
- **Health Tracking:** "Record my blood pressure: 120/80"

---

## 🛠️ Technology Stack

| Category | Technology |
|----------|-----------|
| **LLM** | Ollama (Gemma 2B) |
| **Agent Framework** | LangChain, LangGraph |
| **Computer Vision** | CLIP (OpenAI) |
| **Web Interface** | Gradio |
| **Voice** | Google Text-to-Speech (gTTS) |
| **Location** | Google Maps API |
| **Image Processing** | OpenCV, Pillow |
| **ML Framework** | PyTorch, Transformers |

---

## 📊 System Capabilities

### Agent Performance

| Agent | Response Time | Accuracy |
|-------|--------------|----------|
| Router | < 1s | ~90% |
| Emergency | 2-5s | High |
| Medical Consultation | 3-6s | Moderate |
| Appointment | 2-4s | High |
| Prescription | 2-5s | High |
| Health Monitor | 2-3s | High |

### Computer Vision

- **Supported Formats:** PNG, JPG, JPEG
- **Analysis Time:** 3-8 seconds
- **Categories:** Skin conditions, wounds, test results, medical documents

---

## 🔑 API Keys Setup

You'll need the following API keys:

1. **Google Maps API Key**
   - Go to [Google Cloud Console](https://console.cloud.google.com/)
   - Enable Maps JavaScript API and Places API
   - Create credentials
   - Copy the API key

2. **Set in notebook:**
   ```python
   GOOGLE_MAPS_API_KEY = "your_api_key_here"
   ```

---

## 📂 Project Structure

```
AliAsjad/
│
├── heal_matrix_3.ipynb          # Main implementation notebook
├── HEAL_MATRIX_Step_by_Step.ipynb  # Structured step-by-step version
├── README.md                     # This file
├── requirements.txt              # Python dependencies
├── LICENSE                       # MIT License
├── .gitignore                    # Git ignore rules
│
└── docs/
    ├── HEAL_MATRIX_Research_Report.docx  # Research documentation
    └── napkin_flowchart_prompts.txt      # Flowchart generation prompts
```

---

## 🎓 Research & Documentation

This project includes comprehensive research documentation:

- **Research Report:** Complete academic-style report with methodology, results, and literature review
- **Flowchart Prompts:** Ready-to-use prompts for generating system diagrams in Napkin.ai
- **Architecture Diagrams:** System architecture and data flow visualizations

Find all documentation in the `docs/` folder.

---

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## ⚠️ Disclaimer

**IMPORTANT:** This is an AI assistant for **informational and educational purposes only**. 

- ❌ NOT a replacement for professional medical advice
- ❌ NOT approved as a medical device
- ❌ NOT for emergency medical situations (call 911)
- ✅ For research and demonstration purposes
- ✅ Always consult qualified healthcare professionals

---

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- **Anthropic** - Claude AI assistance
- **Google** - Gemma model, Maps API, TTS
- **OpenAI** - CLIP model
- **Ollama** - Local LLM hosting
- **LangChain** - Agent framework
- **Gradio** - Web interface

---

## 📧 Contact

**Ali Asjad**
- GitHub: [@aliasjad6536](https://github.com/aliasjad6536)
- Repository: [AliAsjad](https://github.com/aliasjad6536/AliAsjad)

---

## 🌟 Star History

If you find this project useful, please consider giving it a star! ⭐

---

## 🔮 Future Enhancements

- [ ] Integration with wearable devices (smartwatches, fitness trackers)
- [ ] Multi-language support
- [ ] Specialized medical imaging models (X-ray, MRI analysis)
- [ ] Electronic Health Records (EHR) integration
- [ ] Telemedicine video consultation
- [ ] Blockchain for health data security
- [ ] Mobile app (iOS/Android)
- [ ] Clinical validation studies

---

## 📈 Version History

- **v1.0.0** (2026-03) - Initial release
  - Multi-agent system with 6 specialized agents
  - Computer vision integration
  - Voice interface
  - Location-based services
  - Gradio web interface

---

<div align="center">

Made with ❤️ using AI and Open Source

**[⬆ Back to Top](#-heal-matrix---ai-powered-multi-agent-healthcare-platform)**

</div>

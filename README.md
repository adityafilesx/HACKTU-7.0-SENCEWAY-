# Senseway – Web-Based Motor Accessibility System

Senseway is a web-based assistive technology platform that empowers individuals with motor disabilities to interact with computers when traditional input methods become unreliable. Using webcam-based eye-gaze tracking, intentional blink detection, and voice commands, Senseway preserves user intent even as motor control degrades due to conditions like ALS, Parkinson's disease, stroke, carpal tunnel syndrome, and repetitive strain injuries.

---

## Problem Statement

Modern digital interfaces assume precise motor control. For users with motor impairments, this assumption breaks down—even though cognitive intent remains fully intact. Senseway bridges this gap by providing an interaction model that tolerates noisy, unstable, and fatigued motor signals while preserving control, safety, and autonomy.

---

## Key Features

- **Eye-gaze cursor control** using a standard webcam
- **Intentional blink detection** with structured lock-in logic to prevent accidental clicks
- **Cursor stabilization and jitter reduction** for smoother interaction
- **On-screen gaze-friendly keyboard** for hands-free typing
- **Voice commands** to reduce physical effort
- **Emergency assistance** with confirmation-based triggering
- **Fatigue-aware interaction feedback** to adapt to changing user states
- **Consumer hardware only**—no specialized devices required

---

## Technology Stack

### Core Technologies
- **Python 3.10** (required)
- **OpenCV** – Video capture and preprocessing
- **MediaPipe Face Mesh** – Eye and facial landmark detection
- **PyAutoGUI** – Cursor, click, typing, and scroll control
- **Flask** – Web-based user interface

### AI & Voice
- **Speech-to-Text** (browser-based or API-based)
- **Gemini API** – Semantic intent classification for emergency actions

### Frontend
- **HTML/CSS/JavaScript** – Accessibility-first UI design

---

## Project Structure

```
Senseway/
├── app.py                 # Flask application entry point
├── eye_tracking/          # Eye gaze & blink detection logic
├── ui/                    # Web UI templates and static files
├── automation/            # System control & emergency logic
├── requirements.txt       # Python dependencies
└── README.md              # Project documentation
```

---

## System Requirements

Before running Senseway, ensure you have:

- **Python 3.10** installed  
  *Note: Other Python versions may cause compatibility issues*
- A working **webcam**
- A **microphone** (for voice features)
- **Stable lighting** for optimal eye-tracking performance

**Verify your Python version:**
```bash
python3 --version
```
*Must be Python 3.10.x*

---

## Installation & Setup

### Step 1: Clone the Repository
```bash
git clone https://github.com/your-username/senseway.git
cd senseway
```

### Step 2: Create a Virtual Environment (Recommended)
```bash
python3.10 -m venv venv
source venv/bin/activate      # macOS/Linux
venv\Scripts\activate         # Windows
```

### Step 3: Install Dependencies
```bash
pip install -r requirements.txt
```

### Step 4: Run the Application
```bash
python3.10 app.py
```

### Step 5: Open in Browser
Once the server starts, navigate to:
```
http://127.0.0.1:5000
```

---

## Configuration & Permissions

- **Camera and microphone access** will be requested on first use
- Ensure **adequate lighting** for accurate eye tracking
- **Emergency actions require confirmation** to prevent accidental triggers
- **Gemini API key** must be configured if emergency intent classification is enabled (see configuration documentation)

---

## Important Considerations

- This is a **research and hackathon prototype**, not a clinical product
- Eye tracking performance depends on **lighting conditions and camera quality**
- System-level controls are **intentionally guarded** to prevent accidental actions
- The web version focuses on **accessibility demonstration and research**, not production deployment
- **Security notice**: System-level automation features should be used with caution

---

## Future Development

- Android implementation using Accessibility Services
- Enhanced adaptive fatigue detection algorithms
- Long-term user ability profiling and personalization
- Expanded automation workflows and integrations
- Clinical validation and compliance pathways
- Multi-language support
- Enhanced security and privacy controls

---

## Contributing

This project was built as part of a hackathon initiative focused on inclusive and accessible technology. We welcome contributions, ideas, and improvements from the community.

### How to Contribute
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/improvement`)
3. Commit your changes (`git commit -am 'Add new feature'`)
4. Push to the branch (`git push origin feature/improvement`)
5. Submit a pull request with a clear description of your changes

---

## License

This project is intended for **educational and research purposes**. Please refer to the LICENSE file for detailed terms and conditions.

---

## Support & Contact

For questions, feedback, or collaboration inquiries, please:
- Open an issue on GitHub
- Contact the project maintainers through the repository

---

## Acknowledgments

Built with accessibility, autonomy, and dignity at its core. This project represents our commitment to creating technology that serves everyone, regardless of physical ability.

---

**Senseway — Preserving intent when motion fails.**

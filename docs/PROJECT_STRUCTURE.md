# SignBridge AI - Project Structure

## Directory Overview

```
SignBridge-AI/
├── backend/
│   ├── app.py                 # Flask application factory
│   ├── config.py              # Configuration settings
│   ├── requirements.txt        # Python dependencies
│   ├── routes/
│   │   ├── gesture_routes.py   # Gesture recognition endpoints
│   │   ├── translation_routes.py  # Translation endpoints
│   │   └── avatar_routes.py    # Avatar animation endpoints
│   ├── services/
│   │   ├── gesture_service.py     # Gesture recognition logic
│   │   ├── translation_service.py # Translation logic
│   │   └── avatar_service.py      # Avatar animation logic
│   └── tests/                 # Unit tests
├── frontend/
│   ├── package.json           # NPM dependencies
│   ├── src/
│   │   ├── App.jsx           # Main app component
│   │   ├── components/       # Reusable components
│   │   │   └── Navbar.jsx
│   │   ├── pages/            # Page components
│   │   │   ├── Home.jsx
│   │   │   ├── GestureRecognition.jsx
│   │   │   ├── Translation.jsx
│   │   │   ├── Avatar.jsx
│   │   │   └── Learning.jsx
│   │   └── services/         # API services
├── models/
│   ├── gesture_recognition.h5    # Trained gesture model
│   ├── pose_detection.h5         # Pose detection model
│   └── facial_expression.h5      # Expression recognition model
├── docs/
│   ├── PROJECT_STRUCTURE.md   # This file
│   ├── API_DOCUMENTATION.md   # API endpoints reference
│   ├── SETUP_GUIDE.md         # Installation & setup
│   └── CONTRIBUTING.md        # Contribution guidelines
└── README.md                  # Project overview
```

## Backend Structure

### Routes
- **gesture_routes.py**: Handles gesture recognition requests
- **translation_routes.py**: Handles sign-to-text, text-to-sign conversions
- **avatar_routes.py**: Handles avatar animation generation

### Services
- **gesture_service.py**: Computer vision and gesture recognition logic
- **translation_service.py**: NLP-based translation logic
- **avatar_service.py**: 3D animation generation

## Frontend Structure

### Pages
- **Home**: Landing page with feature overview
- **GestureRecognition**: Real-time camera feed and gesture recognition
- **Translation**: Text-to-sign and voice-to-sign conversion
- **Avatar**: 3D avatar animation display
- **Learning**: Interactive ISL learning module

### Components
- **Navbar**: Navigation menu with links to all pages

## Data Flow

1. **Gesture Recognition Flow**
   - User enables camera → Video frames captured → Landmarks extracted → Model prediction → Gesture output

2. **Translation Flow**
   - Input (text/speech) → NLP processing → Gesture sequence → Output (text/speech/animation)

3. **Avatar Animation Flow**
   - Gesture sequence → Animation mapping → 3D avatar rendering → Display animation

## TODO Items

- [ ] Train gesture recognition model
- [ ] Implement NLP translation models
- [ ] Set up 3D avatar system (Three.js/Babylon.js)
- [ ] Create database schema and models
- [ ] Implement authentication and user management
- [ ] Add comprehensive error handling
- [ ] Create unit and integration tests
- [ ] Deploy frontend and backend
- [ ] Optimize performance for real-time processing

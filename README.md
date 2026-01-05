# 🔭 Aladin Lite Visualizer (Web App)

[![Python](https://img.shields.io/badge/Backend-Flask-blue?logo=python)](https://flask.palletsprojects.com/)
[![Frontend](https://img.shields.io/badge/Frontend-Aladin_Lite_V3-orange)]()
[![Context](https://img.shields.io/badge/Context-CDS_Internship-red)]()

> A full-stack web application allowing researchers to upload raw astronomical data (FITS), process them, and visualize them interactively in the browser using the **Aladin Lite v3** engine.

![Project Screenshot](assets/screenshot.png)
*(Pense à mettre une capture d'écran ici !)*

## 💡 About the Project
This tool was developed during my internship at the **Centre de Données astronomiques de Strasbourg (CDS)**.
While **Aladin Lite** is the core visualization engine, this project provides the **applicative layer** needed to make it usable for custom data processing.

It bridges the gap between raw FITS files and the browser by handling:
1.  **Upload:** Secure file transfer from user to server.
2.  **Processing:** Conversion of FITS images into HiPS (Hierarchical Progressive Surveys) format on the backend.
3.  **Visualization:** Dynamic rendering using the Aladin Lite V3 API.

## ✨ Key Features
* **FITS to HiPS Conversion:** Automated backend pipeline to process astronomical images.
* **Interactive Viewer:** Zoom, pan, and change projection types (based on Aladin Lite).
* **Asynchronous Processing:** Background task management for heavy files to keep the UI responsive.
* **Sharing System:** Generation of unique URLs to share a specific view with other researchers.

## 🛠️ Technical Architecture

### Directory Structure
The project follows a standard Flask structure:
```bash
AladinLiteVisualizer/
├── app.py              # Main Flask application entry point
├── static/             # Frontend assets
│   ├── js/             # Custom JavaScript logic
│   ├── css/            # Stylesheets
│   └── aladin.js       # Aladin Lite V3 library (bundled)
├── templates/          # HTML Templates (Jinja2)
├── uploads/            # Temporary storage for uploaded FITS
└── requirements.txt    # Python dependencies
```
Tech Stack

    Backend: Python 3.10+, Flask (Web Server), Astropy (FITS handling)

    Frontend: HTML5, CSS3, JavaScript

    Core Engine: Aladin Lite v3 (WebGL2/Rust)

🚀 Installation & Setup

To run this application locally on your machine:

    Clone the repository
    Bash

git clone [https://github.com/lilou-cb/AladinLiteVisualizer.git](https://github.com/lilou-cb/AladinLiteVisualizer.git)
cd AladinLiteVisualizer

Set up the Virtual Environment
Bash

    python -m venv venv
    
    # Windows
    venv\Scripts\activate
    
    # Mac/Linux
    source venv/bin/activate

Install Python Dependencies
Bash

    pip install -r requirements.txt

Run the Application
Bash

    flask run

    Open your browser at http://127.0.0.1:5000

⚖️ License & Credits

- Project Author: Lilou Choukroun-Balzan

- Aladin Lite Engine: Developed at CDS, licensed under GPL v3.0.

- See Aladin Lite Official Repo for the core engine source code.

-------------

Developed for the Observatoire Astronomique de Strasbourg - 2025

[README.md](https://github.com/user-attachments/files/34385444/README.md)
# AI Workout Plan

An interactive workout-planning prototype for students and young adults. It creates a weekly routine based on a user's fitness goal, experience level, available time, equipment, and preferences.

## Features

- Interactive profile form
- Personalized weekly workout schedule
- Exercise library tagged by movement pattern, muscle group, equipment, level, and goal
- Beginner-friendly exercise filtering
- Basic preference and constraint handling
- Downloadable workout plan
- No API key or external account required

## How it works

The current prototype uses an explainable, rule-based recommendation engine in `workout_engine.py`. It is functional without an external AI service: user inputs are used to filter and organize exercises from the exercise knowledge base.

It is not a medical tool and does not diagnose injuries or prescribe rehabilitation. The free-text limitation field only handles a small number of explicit constraints (currently, avoiding jumping); do not rely on it for medical screening.

## Run locally

1. Install Python 3.10 or later.
2. Open a terminal in this project folder.
3. Create and activate a virtual environment (recommended):

   ```bash
   python -m venv .venv
   source .venv/bin/activate
   ```

   On Windows PowerShell:

   ```powershell
   .venv\Scripts\Activate.ps1
   ```

4. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

5. Start the app:

   ```bash
   streamlit run app.py
   ```

6. Open the local URL shown in the terminal (usually http://localhost:8501).

## Run tests

```bash
python -m unittest discover -s tests -v
```

## Project structure

```text
ai_workout_plan/
├── app.py
├── workout_engine.py
├── requirements.txt
├── README.md
├── tests/
│   └── test_workout_engine.py
└── knowledge_base/
    └── README.md
```

## Knowledge base

The `knowledge_base/` folder is intended for the five project reference documents:

1. Fitness Goals and User Profiling
2. Exercise Library and Muscle Group Classification
3. Workout Scheduling and Program Design
4. Progress Tracking and Progressive Overload
5. Workout Safety and Injury Prevention

The code currently includes a small structured exercise library in `workout_engine.py`. The PDFs are supporting references; they are not executable code.

## Future improvements

- Add a language-model API for conversational workout explanations (with safety checks).
- Save user profiles and workout history with explicit consent.
- Add a progress dashboard and exercise completion tracking.
- Expand the exercise library with reviewed instructions and video demonstrations.
- Add more robust equipment and limitation filters.

## Disclaimer

This project provides general educational fitness information, not medical advice. Users should stop if they experience pain or feel unwell. People with injuries, medical conditions, or concerns about exercise suitability should consult an appropriate qualified professional.

# MLViz

**MLViz** is an adaptive, gamified learning platform that helps users understand Machine Learning (ML) and Deep Learning (DL) through personalized, multimodal experiences. The system leverages **K2 Think**, a reasoning-first AI model, to analyze learner comprehension in real time and orchestrate creative submodels that generate tailored analogies, visuals, and coding exercises.

---

## Overview

MLViz transforms traditional ML/DL education into an intelligent, interactive learning journey. It monitors engagement signals such as reading time, chat interactions, and quiz performance to infer comprehension. Based on these insights, K2 Think dynamically adjusts the learning pathway, ensuring every user receives content suited to their understanding level.

The system uses:

* **React** for the front-end interface
* **Node.js / Express** as the backend API layer
* **PostgreSQL** for user data and module storage
* **K2 Think** as the core reasoning and adaptation engine
* **Creative Submodels** for multimodal content generation (text, visual, code)

---

## Architecture

The repository includes architecture diagrams illustrating the full system workflow:

| Diagram Type      | File                              | Description                              |
| ----------------- | --------------------------------- | ---------------------------------------- |
| Container Diagram | `diagrams/plantuml/container.png` | High-level system architecture           |
| Activity Diagram  | `diagrams/plantuml/activity.png`  | User learning and decision flow          |
| Sequence Diagram  | `diagrams/plantuml/sequence.png`  | Component-to-component interactions      |
| Data Flow Diagram | `diagrams/plantuml/dfd.png`       | Logical data movement between components |

All source files are available in both **PlantUML** (`.puml`) and **Mermaid** (`.mmd`) formats for reproducibility.

---

## Core Concept

1. **Data Capture:**
   The React interface records reading duration, quiz attempts, and chat interactions.

2. **Reasoning Layer:**
   The backend aggregates metrics and forwards them to **K2 Think**, which interprets comprehension levels using chain-of-thought reasoning.

3. **Content Orchestration:**
   Based on reasoning results, **K2 Think** instructs submodels to create new analogies, diagrams, or coding tasks that align with the learner’s understanding.

4. **Personalized Delivery:**
   The updated content is assembled and sent back to the React interface for immediate learner feedback and progression tracking.

5. **Gamification:**
   Users unlock levels, earn badges, and follow adaptive paths while maintaining consistent learning objectives.

---

## Directory Structure

```
MLViz/
 ├── diagrams/
 │    ├── plantuml/         # UML sources and PNGs
 │    └── mermaid/          # Mermaid sources
 ├── src/                   # React application (front-end)
 ├── server/                # Node.js backend (API layer)
 ├── docs/                  # Technical documentation, reports, proposal
 ├── package.json
 ├── README.md
 └── LICENSE
```

---

## Development Notes

* **Frontend:** React 18+, TypeScript recommended.
* **Backend:** Node.js (Express), integrated REST endpoints for reasoning and analytics.
* **Database:** PostgreSQL, with user progress, module metadata, and interaction logs.
* **AI Integration:** K2 Think API for reasoning; optional external creative APIs for multimodal generation.
* **Security:** Use token-based authentication (JWT) for user sessions.
* **Code Execution:** All code examples run in a sandboxed environment (e.g., Jupyter-lite or a restricted Python runner).

---

## Future Work

* Implement real-time learning analytics dashboard.
* Add multilingual content generation.
* Expand creative submodel integration for richer multimodal experiences.
* Incorporate open educational datasets for model fine-tuning.

---

## License

This project is released under the **MIT License**.
See the `LICENSE` file for details.

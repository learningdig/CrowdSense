
# CrowdSense
### AI-Powered Crowd Monitoring, Forecasting & Spatial Decision Support

CrowdSense is an AI-powered crowd monitoring and forecasting system designed to help event organizers understand crowd distribution, identify emerging congestion, and make informed decisions before overcrowding becomes critical.

The system analyzes periodic images of a venue, estimates crowd density across predefined zones, forecasts near-future crowd conditions, and generates spatially aware recommendations to support crowd management.

---

## 1. Project Overview

Managing large crowds is a complex operational challenge. Uneven crowd distribution, congested pathways, and delayed responses to overcrowding can create unsafe situations at public events and high-footfall venues.

CrowdSense aims to address this challenge by combining computer vision, machine learning, spatial analysis, and an interactive monitoring dashboard.

Rather than simply displaying the current crowd count, the system focuses on understanding **where congestion is developing, how conditions may change, and what actions could help manage the situation.**

## 2. Core Objective

The central feature of CrowdSense is:

**Zone-Level Early Warning and Spatially Aware Actionable Recommendations**

The system is designed to:

- Divide a venue into predefined zones and estimate crowd distribution within each zone.
- Monitor crowd occupancy and changes over time.
- Forecast crowd levels for individual zones.
- Identify zones that may approach or exceed configured occupancy thresholds.
- Evaluate alternative routes and possible crowd-management interventions.
- Generate explainable recommendations to assist event organizers in making operational decisions.

## 3. How It Works

The proposed system follows this workflow:

1. **Image Input:** Periodic, timestamped images of the venue are supplied to the system.
2. **Person Detection:** A computer vision model detects people in the images.
3. **Crowd Estimation:** Detected individuals are assigned to predefined venue zones to estimate zone-level crowd counts.
4. **Historical Data Storage:** Crowd observations are stored with their corresponding timestamps.
5. **Forecasting:** Machine learning models analyze historical observations to estimate future crowd levels.
6. **Spatial Risk Analysis:** Current and forecasted occupancy are evaluated against venue-specific conditions and configured thresholds.
7. **Recommendation Engine:** The system evaluates feasible routes and potential interventions to generate spatially relevant recommendations.
8. **Dashboard & Notifications:** Results are presented through a monitoring dashboard, with notifications supported through workflow automation.

## 4. Proposed Technology Stack

| Component | Proposed Technology |
|---|---|
| Frontend | React.js |
| Backend | Node.js, Express.js |
| Database | MongoDB |
| Computer Vision | YOLOv8, OpenCV |
| ML Service | Python, FastAPI |
| Forecasting | XGBoost, Random Forest, Linear Regression |
| Spatial Analysis | NetworkX, graph-based routing |
| Workflow Automation | n8n |

*The technologies listed above represent the proposed architecture. Final implementation choices may evolve during development.*

## 5. Key System Components

### Computer Vision & Crowd Estimation
- Detect individuals in venue images.
- Estimate crowd counts.
- Map detected individuals to predefined spatial zones.
- Generate zone-level crowd observations.

### Zone-Level Forecasting
- Maintain timestamped crowd observations.
- Extract relevant temporal features.
- Forecast future occupancy for individual zones.
- Evaluate forecast performance using appropriate metrics.

### Spatial Analysis & Recommendation Engine
- Represent the venue using a spatial layout and a graph of walkable pathways.
- Identify potential congestion points and alternative routes.
- Evaluate candidate crowd-management interventions.
- Generate recommendations with supporting reasoning and relevant constraints.

### Monitoring Dashboard
- Display venue layouts and zone-level crowd distribution.
- Visualize current and forecasted crowd conditions.
- Highlight zones requiring attention.
- Present recommended actions and their supporting information.

### Notification & Automation
- Integrate n8n to support automated alerts and notifications.
- Trigger notifications based on configured risk conditions.

## 6. Proposed System Architecture

```text
              PERIODIC VENUE IMAGES
                       |
                       v
              COMPUTER VISION
               YOLOv8 + OpenCV
                       |
                       v
              CROWD ESTIMATION
               Zone Assignment
                       |
                       v
               HISTORICAL DATA
                   MongoDB
                       |
                       v
              FORECASTING ENGINE
                Python + ML
                       |
                       v
              SPATIAL RISK ANALYSIS
             Grid + Venue Graph
                       |
                       v
             RECOMMENDATION ENGINE
             Route & Intervention
                   Evaluation
                       |
                       v
               MONITORING DASHBOARD
                    React
                       |
                       v
              AUTOMATED NOTIFICATIONS
                      n8n
```

## 7. Data Strategy

The project will explore publicly available crowd-analysis datasets and suitable sources of supplementary information.

Potential datasets include:

- **UCF-QNRF:** A large-scale crowd-counting dataset.
- **NWPU-Crowd:** A crowd-counting dataset containing diverse crowd scenes.
- **ShanghaiTech:** A widely used dataset for crowd counting and density estimation.
- **DroneCrowd:** A dataset for crowd analysis from aerial viewpoints.

Historical weather information may also be explored as supplementary contextual data.

An important distinction is that crowd-counting datasets do not automatically provide the timestamped sequences required for forecasting. Reliable forecasting will require suitable temporal observations, ideally captured from consistent viewpoints within the same venue.

## 8. Project Scope & Constraints

The initial system is designed around periodic image-based analysis rather than continuous live video surveillance.

Current scope:

- Periodic, timestamped image inputs.
- Predefined venue zones and spatial layouts.
- Person detection and crowd estimation.
- Historical crowd-data storage.
- Zone-level crowd forecasting.
- Spatial risk assessment.
- Explainable crowd-management recommendations.
- Interactive monitoring dashboard.

The initial implementation does not assume:

- Continuous CCTV stream processing.
- Live camera deployment.
- IoT sensors or physical crowd-counting hardware.
- Automatic knowledge of pedestrian movement from isolated images.

Forecasting and route recommendations will depend on the quality of available observations, venue geometry, and the assumptions used by the models.

## 9. Development Status

**Current stage:** Initial project setup and architecture planning.

The repository will be maintained throughout the development lifecycle. Implementation, testing, documentation, and future improvements will be tracked through GitHub.

Planned development milestones:

- [ ] Repository setup and project documentation
- [ ] Dataset exploration and data preparation
- [ ] Initial person-detection pipeline
- [ ] Venue-zone configuration and crowd estimation
- [ ] Historical crowd-data storage
- [ ] Zone-level forecasting model
- [ ] Spatial risk analysis
- [ ] Route evaluation and recommendation engine
- [ ] Backend API development
- [ ] Frontend monitoring dashboard
- [ ] n8n notification integration
- [ ] System testing and evaluation

## 10. Repository Structure

```text
CrowdSense/
│
├── frontend/              # React monitoring dashboard
│
├── backend/               # Node.js and Express API
│
├── ml-service/            # Computer vision, forecasting
│                          # and spatial recommendation logic
│
├── automation/            # n8n workflows and notifications
│
├── docs/                  # Architecture and project documentation
│
├── tests/                 # Unit and integration tests
│
├── .gitignore
└── README.md
```

The repository structure will evolve as individual components are implemented.

## 11. Team

**Project:** CrowdSense  
**Domain:** Artificial Intelligence, Machine Learning, Computer Vision and Full-Stack Development

| Team Member | Responsibility |
|---|---|
| Hardik | To be finalized |
| Vidya | To be finalized |
| Priyanshu | To be finalized |
| Anjalee | To be finalized |

---

## 12. Project Vision

CrowdSense aims to move beyond passive crowd monitoring toward predictive and spatially informed crowd management.

By combining computer vision, forecasting, and graph-based spatial analysis, the project seeks to provide event organizers with actionable information that helps them anticipate congestion and make better operational decisions.

**From observing crowds to anticipating congestion and supporting better decisions.**

# GeoSense — AI-Based Landslide Early Warning & Risk Monitoring

GeoSense (formerly **LandslideGuard**) is an AI-powered landslide risk monitoring and early-warning prototype designed to support monitoring of landslide-prone regions, with a focus on the **North Eastern Region (NER) of India**.

The project brings environmental and weather information together in a monitoring dashboard to help users understand changing conditions, assess potential risk, and support timely decision-making.

> **Live demo:** https://landslide-guard-chi.vercel.app  
> **Repository:** https://github.com/Deepak-tech06/landslide-guard

---

## Project Overview

Landslides can cause serious damage to communities, infrastructure, and the environment. GeoSense explores how software, environmental data, and risk-monitoring workflows can contribute to earlier awareness of potentially hazardous conditions.

The prototype is intended to:

- Present landslide-related monitoring information through a centralized dashboard.
- Use weather and environmental data as inputs for risk assessment.
- Help users identify areas and conditions that may require attention.
- Provide an authenticated experience with role-based access for authorized users.
- Support awareness and decision-making; it is not a substitute for official warnings or expert geological assessment.

## Key Capabilities

- **Risk monitoring dashboard** — a centralized view of available monitoring information.
- **Weather data integration** — uses weather information to support environmental monitoring.
- **Risk assessment** — presents risk-related insights based on the data and logic implemented in the application.
- **Authentication** — account registration and login through the configured authentication service.
- **Role-based access control (RBAC)** — access is managed according to configured user roles.
- **Web deployment** — frontend and backend services are deployed separately.

*The availability of individual features depends on the current deployment and configured external services.*

## Technology Stack

| Layer | Technology |
|---|---|
| Frontend | React / TypeScript |
| Backend API | Python / FastAPI |
| Authentication & database services | Supabase |
| Weather data | Open-Meteo |
| Frontend hosting | Vercel |
| Backend hosting | Render |
| Version control | Git & GitHub |

## System Architecture

At a high level, the application follows this flow:

1. A user opens the GeoSense web application.
2. The frontend communicates with the deployed backend API.
3. The application retrieves relevant weather or environmental information from its configured data source.
4. The backend and application logic process available inputs for monitoring and risk assessment.
5. The dashboard presents the resulting information to the user.
6. Authentication and role-based permissions control access to protected functionality.

## Live Deployment

- **Frontend:** https://landslide-guard-chi.vercel.app
- **Backend:** https://landslide-guard-api.onrender.com

The frontend and backend are hosted independently. The live experience may depend on the availability of these services and correctly configured environment variables.

## Getting Started

The exact commands and environment variable names depend on the current source structure. The following is a general setup outline.

### Prerequisites

- Git
- Node.js and npm
- Python 3
- Access to the configured Supabase project
- Required API credentials for any external services used by the application

### 1. Clone the repository

```bash
git clone https://github.com/Deepak-tech06/landslide-guard.git
cd landslide-guard
```

### 2. Configure environment variables

Create the environment files required by the frontend and backend. Use the variable names expected by the source code.

Typical configuration may include:

- Supabase project URL and public/anon key
- Backend API URL for the frontend
- Supabase credentials required by the backend, if applicable
- External service configuration, if required

**Do not commit secrets, private API keys, service-role keys, database passwords, or production credentials.** Keep local environment files out of version control.

### 3. Install dependencies and run

Install the frontend and backend dependencies using the package manifests and instructions in their respective project directories. Start each service using the development scripts defined by the project.

> This repository's root structure and exact run scripts should be checked before running commands; no unverified commands or environment variable names are assumed here.

## Security Notes

- Never expose Supabase service-role keys or other server-side secrets in frontend code.
- Configure authentication and row-level security policies in Supabase for the intended access model.
- Restrict protected API routes and validate user permissions on the server.
- Use HTTPS and production environment variables for deployed services.

## Limitations & Responsible Use

GeoSense is a software prototype for monitoring and decision-support exploration. Risk outputs depend on the quality, coverage, and freshness of available data and on the assumptions in the implemented assessment logic.

It should **not** be used as the sole basis for evacuation, public-safety, or other emergency decisions. Always follow official alerts and guidance from local authorities and qualified geological or disaster-management professionals.

## Project Context

This project was developed in the context of **Smart India Hackathon (SIH)** problem statement **SIH26001 — AI-Based Early Warning & Landslide Risk Monitoring System in NER**.

## Author

**Deepak B V**  
GitHub: [@Deepak-tech06](https://github.com/Deepak-tech06)

---

If you find the project useful, consider giving the repository a ⭐.

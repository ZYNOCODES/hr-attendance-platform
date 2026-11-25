# HR Attendance Platform

Attendance for field missions and travel assignments, validated by GPS and face confirmation.

Employees check in at scheduled points during missions and multi-day assignments. The server validates distance to the expected zone, managers follow attendance as heatmaps, and notifications remind people of pending check-ins.

> **Structure only.** The source code is private. Source files here are intentionally empty so you can see how the project is organized. Commands describe the private codebase.
>
> Company names, logos and data were removed. All data in the screenshots is fictional.

![Overview](docs/screenshots/overview.png)

## Features

- Missions with scheduled check-in points
- Multi-day travel assignments by region
- GPS radius validation and face confirmation
- Manual validation by an administrator
- Attendance rates by employee and day
- Notifications

## Applications

| Application | Role |
| --- | --- |
| [API server](server/README.md) | REST API for the dashboard and mobile clients |
| [Dashboard](dashboard/README.md) | React administration interface |

## Architecture

```mermaid
flowchart LR
  M[Mobile client] -- check-in --> S[API server]
  D[Dashboard] --> S
  S --> DB[(MySQL)]
  S --> N[Push notifications]
```

## Engineering highlights

- Layered modules: validator, service, controller, routes
- Unified response format and central error handling
- Environment validated at startup
- Soft deletion and structured logs

## Screenshots

| Overview | Missions |
| --- | --- |
| ![Overview](docs/screenshots/overview.png) | ![Missions](docs/screenshots/missions.png) |
| **Mission attendance** | **Travel assignments** |
| ![Mission attendance](docs/screenshots/mission-presence.png) | ![Travel assignments](docs/screenshots/deplacements.png) |
| **Travel attendance** | **GPS regions** |
| ![Travel attendance](docs/screenshots/deplacement-presence.png) | ![GPS regions](docs/screenshots/regions.png) |
| **Departments** | **Employees** |
| ![Departments](docs/screenshots/departments.png) | ![Employees](docs/screenshots/users.png) |
| **Sign in** |
| ![Sign in](docs/screenshots/login.png) |

Screenshots show the real dashboard connected to a mock API with fictional data, because the server needs MySQL.

## Repository layout

```text
server/                                 REST API for the dashboard and mobile clients
dashboard/                              React administration interface
docs/screenshots/
```

Each application has its own README with responsibilities, dependencies, structure and commands.

## Usage

Published for portfolio and presentation purposes. No license is granted for reuse.

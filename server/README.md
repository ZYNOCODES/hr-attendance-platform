# API server

REST API for the dashboard and mobile clients. Part of [HR Attendance Platform](../README.md).

> **Structure only.** The source code is private. Source files here are intentionally empty so you can see how the project is organized. Commands describe the private codebase.

## Responsibilities

- Separate mobile and dashboard route groups
- JWT, roles, Joi validation and rate limits
- Haversine distance checks for every check-in
- Scheduled reminders and push notifications
- Photo management
- Interactive API documentation outside production

## Main dependencies

`bcrypt`, `cors`, `dotenv`, `express`, `express-rate-limit`, `firebase-admin`, `helmet`, `joi`, `jsonwebtoken`, `morgan`, `multer`, `mysql2`, `node-cron`, `sequelize`, `swagger-jsdoc`, `swagger-ui-express`, `winston`

## Structure

```text
config/                           4 files
middlewares/                      5 files
models/                           16 files
modules/                          33 files
utils/                            7 files
```

## Commands

```bash
npm install
npm run dev
npm start
npm run lint
```

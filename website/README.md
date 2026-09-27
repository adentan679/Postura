# Postura Website

Main FastAPI application with user accounts, a posture dashboard,
work-session tracking, and CSV logging. Uses MySQL and Docker.

This application runs independently from `python/server.py`.

## Run Locally

Start Docker Desktop. From the repository root using Git Bash:

```bash
cd website
cp env.example .env
```

On first setup, edit `.env` with your database password and set
`MQTT_TOPIC` to match the firmware (`chuach1234` by default).

```bash
touch posture_data.csv
docker compose up --build
```

Open http://localhost:8000 and register an account. If MySQL is
still starting, wait briefly and refresh.

Press Ctrl+C to stop. For later runs, use `docker compose up`.

## Notes

- Live readings require a connected ESP32 with matching MQTT settings.
- Stop the standalone dashboard before using port 8000.
- Keep `.env` and private session data out of Git.
- The current Docker setup does not preserve MySQL account data
  reliably across container removal or recreation.
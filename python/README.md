# Sensor Dashboard

Standalone FastAPI dashboard for live sensor readings, calibration,
and CSV data collection. Runs independently from `website/`.

## Run Locally

Requires Python 3.10+ and internet access. From the repository root
using Windows Git Bash:

```bash
cd python
py -m venv .venv
source .venv/Scripts/activate
python -m pip install fastapi "uvicorn[standard]" jinja2 paho-mqtt python-dotenv numpy matplotlib requests
python server.py
```

Open http://localhost:8000. Press Ctrl+C to stop.

Live readings require the ESP32 to use the same MQTT broker and
topic prefix. The default prefix is `chuach1234`.

Run this dashboard or the main website one at a time because both
use port 8000. Keep `.env`, `.venv/`, and private data out of Git.
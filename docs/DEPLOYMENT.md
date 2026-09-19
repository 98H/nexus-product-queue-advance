# Deployment & Operations Guide: Product Queue Advance

## 🚀 Live Access & URLs
- **Live Public Access URL:** [/preview/prod-product-queue-advance-a1ffa4/](/preview/prod-product-queue-advance-a1ffa4/)
- **Internal Port:** `0`
- **Runtime Engine:** `python_preview`
- **Deployment Status:** `DEPLOYED / ACTIVE`
- **Timestamp:** `2026-09-19T16:47:19.202616+00:00`

## 🛠️ Management & Service Control
### Launch Command
```bash
python3 app.py --port 0
```

### Health Check Probe
```bash
curl -I http://127.0.0.1:0/
```

### Systemd Service Template
```ini
[Unit]
Description=Product Queue Advance Service
After=network.target

[Service]
Type=simple
WorkingDirectory=/tmp/pytest-of-root/pytest-3/test_backlog_engine_advances_o0/workspaces/prod-product-queue-advance-a1ffa4
ExecStart=/usr/bin/python3 /tmp/pytest-of-root/pytest-3/test_backlog_engine_advances_o0/workspaces/prod-product-queue-advance-a1ffa4/app.py
Restart=always
RestartSec=3

[Install]
WantedBy=multi-user.target
```

## 🔒 Production Security Protocols
- HTTP-only reverse proxy via Nexus Gateway.
- Dedicated port allocation with zero port conflict.

# CV-Mindcare - Privacy-First Wellness Monitor 🌱

> ## ⚠️ Superseded — this repository is archived
>
> CV-Mindcare (v1) was a final-year student prototype built by two students with no prior
> experience. It was rebuilt from the ground up as
> **[WorkWell](https://github.com/XGradien/WorkWell)** — a single data pipeline, five channels,
> a demo mode that actually demonstrates the system, 56 passing tests, and CI on GitHub Actions.
>
> This repository is kept for historical reference of the original work.

**Local wellness monitoring using camera, microphone, and air quality sensors with AI-powered recommendations.**

[![Tests](https://img.shields.io/badge/tests-302%2F302-brightgreen)](https://github.com/Salman-A-Alsahli/CV-Mindcare/actions)
[![Python](https://img.shields.io/badge/python-3.9%2B-blue)](https://www.python.org/downloads/)
[![License](https://img.shields.io/badge/license-MIT-green)](LICENSE)
[![Version](https://img.shields.io/badge/version-1.0.0-brightgreen)](https://github.com/Salman-A-Alsahli/CV-Mindcare/releases)
[![Docker](https://img.shields.io/badge/docker-ready-blue)](Dockerfile)

---

## ⚡ Quick Start

```bash
git clone https://github.com/Salman-A-Alsahli/CV-Mindcare.git
cd CV-Mindcare

# Install (fast ~2 minutes)
pip install -e .

# Start web dashboard
./setup-frontend.sh && ./start-dashboard.sh

# Open http://localhost:5173
```

**🍓 Raspberry Pi / ARM64 Users:** The setup script automatically detects ARM64 architecture and applies necessary workarounds for Rollup/Vite. See [ARM64_SETUP.md](ARM64_SETUP.md) for details.

Alternative methods:
```bash
# API only
uvicorn backend.app:app --reload
# Visit http://localhost:8000/docs

# With optional ML features (emotion detection - slower install ~40 min)
pip install -e .[ml]
```

---

## ✨ Features

- 🎥 **Greenery Detection** - Camera-based nature presence monitoring
  - 📷 **Picamera2 Support** - Native Raspberry Pi camera (10x faster than OpenCV)
  - 🔄 **Auto-detection** - Tries Picamera2 first, falls back to OpenCV
  - 🎨 **OpenCV Processing** - HSV color analysis for greenery detection
- 🎤 **Noise Analysis** - Ambient sound level tracking (dB)
- 🌬️ **Air Quality** - MQ-135 sensor for CO₂, NH₃, benzene, smoke
  - 📊 **Comprehensive Statistics** - Historical data aggregation and analysis
  - 📈 **Trend Detection** - Identify air quality patterns over time
  - 🔍 **Anomaly Detection** - Detect unusual air quality readings
  - 📉 **Level Distribution** - Track air quality level percentages
- 🧠 **AI Recommendations** - Personalized wellness suggestions
- 📊 **Real-Time Dashboard** - Beautiful React interface
- 🔒 **Privacy-First** - All processing stays local, zero cloud
- 🔌 **WebSocket Streaming** - Live sensor data updates
- 📈 **Advanced Analytics** - Trends, anomalies, correlations for all sensors
- ⚡ **Simulation Engine** - Realistic scenario-based testing without hardware
- 🚀 **Performance Optimized** - WAL mode, optimized caching, efficient queries

---

## 📚 Documentation

### Getting Started
- 📖 [Quick Start Guide](docs/getting-started/quick-start.md) - 5-minute setup
- 🔧 [Installation Guide](docs/getting-started/installation.md) - Detailed instructions
- 🛠️ [Hardware Setup](docs/getting-started/hardware-setup.md) - Sensor configuration

### User Guide
- 📊 [Web Dashboard](docs/user-guide/web-dashboard.md) - Using the interface
- ⚡ [Features](docs/user-guide/features.md) - Complete feature list

### Development
- 🏗️ [Architecture](docs/development/architecture.md) - System design
- 🤝 [Contributing](docs/development/contributing.md) - How to contribute
- 🧪 [Testing](docs/development/testing.md) - Test guidelines
- 📡 [API Reference](docs/development/api-reference.md) - Complete API docs

### Deployment
- 🍓 [Raspberry Pi](docs/deployment/raspberry-pi.md) - Deploy on RPi 5
- 🐳 [Docker](docs/deployment/docker.md) - Containerized deployment
- 🚀 [Production](docs/deployment/production.md) - Production checklist

### Project
- 🎯 [Milestones](docs/project-management/milestones.md) - Roadmap
- �� [Changelog](docs/project-management/changelog.md) - Version history
- 📋 [Backlog](docs/project-management/backlog.md) - Future features

### Resources
- 🔧 [Troubleshooting](docs/TROUBLESHOOTING.md) - Common issues & solutions
- 🍓 [ARM64 Setup Guide](ARM64_SETUP.md) - Raspberry Pi / ARM64 specific instructions
- 📷 [Picamera2 Integration](docs/PICAMERA2_INTEGRATION.md) - Raspberry Pi camera + OpenCV guide
- ⚡ [Performance](docs/PERFORMANCE.md) - Optimization guide
- 🔌 [Integrations](docs/integrations/README.md) - Home Assistant & more
- 📚 [API Examples](docs/examples/) - Python, JS, cURL samples
- 🎯 [Examples](examples/) - Demo scripts and code samples

---

## 🎯 Current Status

**Version**: v1.0.0 (Production Release) 🎉  
**Tests**: 302/302 passing (100%) ✅  
**Features**: Camera ✅ | Microphone ✅ | Air Quality ✅ | Docker ✅  
**Status**: Production Ready - Stable Release

---

## 🛠️ Tech Stack

- **Backend**: Python 3.9+, FastAPI, WebSockets, SQLite
- **Frontend**: React 18, Vite, Recharts, TailwindCSS
- **Sensors**: OpenCV, SoundDevice, MQ-135 (Serial/GPIO)
- **AI/ML**: DeepFace, Transformers (optional)
- **Testing**: Pytest, 302 tests, 100% passing ✅

---

## 📦 Installation Options

```bash
# Base installation (fast ~2 min, recommended)
pip install -e .

# With ML features (emotion detection - slower ~40 min)
pip install -e .[ml]

# With development tools
pip install -e .[dev]

# Raspberry Pi optimized
pip install -e .[rpi]

# Everything
pip install -e .[all]
```

---

## 🤝 Contributing

We welcome contributions! See our [Contributing Guide](docs/development/contributing.md).

1. Fork the repository
2. Create feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open Pull Request

---

## 📄 License

MIT License - see [LICENSE](LICENSE) for details.

---

## 🙏 Acknowledgments

- Built with ❤️ for privacy-conscious wellness monitoring
- Optimized for Raspberry Pi 5
- Community-driven development

---

## 🔗 Links

- [Documentation](docs/README.md)
- [GitHub Issues](https://github.com/Salman-A-Alsahli/CV-Mindcare/issues)
- [GitHub Discussions](https://github.com/Salman-A-Alsahli/CV-Mindcare/discussions)
- [Project Board](https://github.com/Salman-A-Alsahli/CV-Mindcare/projects)

---

**Made with ❤️ for your wellbeing | 100% Local | 0% Cloud**

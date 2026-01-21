# WhatsSecure – AI-Powered WhatsApp Security Assistant

WhatsSecure is an intelligent security system designed to detect phishing, scams, and malicious links shared via WhatsApp messages. It automatically analyzes user-submitted links, generates security intelligence using multiple threat analysis platforms, and returns human-readable safety guidance in real time.

The project focuses on **cybersecurity awareness**, **threat detection**, and **digital forensics**, with emphasis on protecting users in high-risk environments where WhatsApp-based scams are prevalent.

## Core Functionality

- ✅ Receives WhatsApp messages via WhatsApp Cloud API
- ✅ Automatically extracts URLs, emails, and domains from messages
- ✅ Scans links using multiple threat intelligence services
- ✅ Uses AI to interpret technical scan results into clear explanations
- ✅ Sends actionable security advice back to users on WhatsApp
- ✅ Generates forensic-style summaries for analysis and reporting

## System Architecture

```
WhatsApp User
    ↓
WhatsApp Cloud API
    ↓
n8n (Workflow Orchestration)
    ↓
Threat Intelligence Layer
├─ VirusTotal (malware analysis)
├─ urlscan.io (website behavior)
├─ Hybrid Analysis (sandbox detection)
└─ Have I Been Pwned (breach checks)
    ↓
AI Engine (OpenAI / DeepSeek)
    ↓
Response & Logging
```

## Key Features

- 🔒 Phishing and scam link detection
- 🎯 QR-code phishing (Quishing) awareness
- 📊 Metadata extraction from URLs and scan reports
- 🤖 AI-generated security explanations (non-technical)
- ⚡ Real-time WhatsApp responses
- 🔧 Modular and extensible workflow design
- 💰 Built entirely using free or freemium tools

## Technologies Used

| Component | Technology |
|-----------|-----------|
| **Messaging** | WhatsApp Cloud API |
| **Orchestration** | n8n |
| **AI/NLP** | OpenAI / DeepSeek |
| **Threat Intel** | VirusTotal, urlscan.io, Hybrid Analysis, HaveIBeenPwned |
| **Language** | JavaScript / JSON |
| **Logging** | JSON-based forensic logs |

## Setup & Installation

### Prerequisites

- WhatsApp Business Account
- n8n instance (cloud or self-hosted)
- API credentials for threat intelligence services

### Environment Configuration

1. Clone the repository:
```bash
git clone <repository-url>
cd whatsecure
```

2. Create `.env` file from `.env.example`:
```bash
cp .env.example .env
```

3. Add your API credentials to `.env` file

4. Import n8n workflow from `workflows/` directory

5. Configure webhooks in WhatsApp Business Manager

## Usage

### For End Users

1. Send a suspicious link to WhatsSecure WhatsApp bot
2. The system analyzes the link within seconds
3. Receive a clear security report on WhatsApp
4. Follow recommendations (safe/suspicious/malicious)

### For Developers

```json
{
  "message": "Check this link",
  "extracted_urls": ["https://example.com"],
  "scan_results": {
    "virustotal": {...},
    "urlscan": {...}
  },
  "ai_summary": "Security assessment provided",
  "risk_level": "LOW"
}
```

## Use Cases

- 👤 Individuals checking suspicious WhatsApp links
- 🎓 Students learning cybersecurity and digital forensics
- 📢 Awareness campaigns against online scams
- 🔬 Academic cybersecurity projects
- 🏢 Organizations training staff on phishing

## Threat Detection Sources

### VirusTotal
- Malware reputation analysis
- File hash verification
- URL/domain risk scoring

### urlscan.io
- Website behavior analysis
- Screenshot and DOM extraction
- SSL/TLS certificate verification

### Hybrid Analysis
- Sandbox-based threat detection
- Behavioral analysis
- File detonation reports

### Have I Been Pwned
- Email/domain breach history
- Data leak verification
- Compromise timeline

## AI-Powered Analysis

The system uses OpenAI/DeepSeek to:
- Convert technical threat data into user-friendly language
- Provide actionable recommendations
- Explain risks without requiring security expertise
- Generate incident summaries for forensic review

## Security & Privacy

- ⚠️ **No data retention**: URLs are analyzed on-demand
- 🔐 **Encrypted API communication**: All API calls use HTTPS
- 📝 **Optional logging**: Forensic logs stored locally
- 🛡️ **API keys**: Never logged or exposed
- 🔒 **User privacy**: No personal data collection

## Forensic Capabilities

Generate lightweight incident reports for analysis:
```json
{
  "timestamp": "2025-01-21T10:30:00Z",
  "analyzed_content": "hashed_for_privacy",
  "threat_verdict": "PHISHING",
  "confidence": 0.95,
  "indicators": ["suspicious_behavior"],
  "action_taken": "user_warned"
}
```

## Project Structure

```
whatsecure/
├── workflows/           # n8n workflow exports
├── logs/               # Forensic logs (gitignored)
├── .env.example        # Environment variables template
├── .gitignore          # Git ignore rules
├── README.md           # This file
├── LICENSE             # MIT License
└── SECURITY.md         # Security guidelines
```

## Roadmap

- [ ] Mobile app with offline analysis
- [ ] Telegram bot integration
- [ ] Advanced machine learning threat scoring
- [ ] Community threat intelligence database
- [ ] Multi-language support
- [ ] Browser extension

## Contributing

Contributions are welcome! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

### Development

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## License

This project is licensed under the MIT License - see [LICENSE](LICENSE) file for details.

## Support & Feedback

- 🐛 Report issues via GitHub Issues
- 💬 Discuss ideas in GitHub Discussions

## Disclaimer

WhatsSecure is a security awareness tool. While it uses reputable threat intelligence sources, no system is 100% accurate. Always exercise caution with suspicious links and don't rely solely on automated detection for critical decisions.

---

**Stay Secure. Stay Aware. Stay Protected.** 🛡️

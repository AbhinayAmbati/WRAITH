# WRAITH

> **AI-Native Backend Generator for Natural Language Developers**

WRAITH empowers developers to build scalable backend APIs using natural language. No more repetitive boilerplate, just simple `.wi` files to define intents and generate REST APIs instantly.

---

## Why WRAITH?
- **Intuitive**: Write backend logic in plain English-like syntax
- **Fast**: Instantly deploy endpoints with no setup
- **Extendable**: Supports models, services, and future integrations
- **CLI-powered**: Rapid project creation and local development

---

## Features
- [x] Define backend routes using `.wi` intent files
- [x] Auto-generate RESTful endpoints from intent scripts
- [x] Simple expression parsing for inputs like `input.username`
- [x] Integrated dev server with live intent loading
- [x] Command-line interface (`wraith`) for all project operations

---

## Installation
```bash
npm install -g wraith-cli
```

---

## Getting Started
```bash
wraith init myApp
cd myApp
wraith dev
```

This creates a new project with sample intent structure and launches the dev server.

---

## Example Intent File (`hello.wi`)
```wi
@Intent("GreetUser")
respond with "Hello, " + input.name
```

### Test the Endpoint
```bash
curl -X POST http://localhost:8080/intent/greetuser \
  -H "Content-Type: application/json" \
  -d '{ "name": "John" }'
```
**Response:**
```json
{
  "intent": "GreetUser",
  "message": "Hello, John"
}
```

---

## Project Structure
```
/intents/           → .wi intent files
/models/            → .wm model declarations (coming soon)
/services/          → .ws backend logic services (coming soon)
/config/            → app configs
wraith.config.json  → project metadata
```

---

## CLI Commands
```bash
wraith init <projectName>   # Scaffold new WRAITH project
wraith dev                  # Run local development server
```

---

## Future Roadmap
- [ ] Input schema validation
- [ ] `.wm` model-to-DB auto mapping
- [ ] Auth & session management
- [ ] Service-layer logic handling (`.ws` files)
- [ ] Frontend SDK generation
- [ ] GPT-native intent expansion

---

## License
MIT

---

## Connect with Us
For collaboration, feedback, or demo requests:
**Email:** wraith.dev@protonmail.com  
**Twitter:** [@WraithStack](https://twitter.com/WraithStack)

---

**Made with fire and ambition by the WRAITH team — backend will never be the same.**

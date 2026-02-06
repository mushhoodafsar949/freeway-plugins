# DevOps & CI/CD Generator Plugin

Generate complete DevOps infrastructure files from a simple voice description of your tech stack.

## 🎯 What It Does

This plugin generates production-ready DevOps configuration files based on your tech stack description. Just say "I have [your tech stack]" and get:

- **Dockerfile** - Optimized, multi-stage container builds
- **docker-compose.yml** - Complete service orchestration
- **GitHub Actions** - CI/CD workflow
- **Azure DevOps** - Alternative CI/CD pipeline
- **Nginx config** - Reverse proxy configuration
- **Deploy script** - Production deployment automation
- **Logging config** - Centralized logging setup

## 🚀 Usage

1. **Configure the plugin:**
   - Get your OpenAI API key from https://platform.openai.com/api-keys
   - Enter it in the plugin settings
   - Optionally customize the model (default: `gpt-4o-mini`)

2. **Use voice input:**
   - Activate Freeway voice input
   - Say: **"I have Node.js and PostgreSQL"**
   - Or: **"I have .NET Core + Angular + Redis"**
   - Or: **"I have Python Flask, MySQL, and Nginx"**

3. **Get your files:**
   - The plugin generates all DevOps files
   - Copy and paste into your project
   - Files are ready to use!

## 📋 Example Inputs

- "I have React frontend, Node.js backend, MongoDB"
- "I have .NET Core API, Angular SPA, PostgreSQL database"
- "I have Python FastAPI, Redis cache, PostgreSQL"
- "I have three microservices: Go service, Python service, Node.js service"

## ⚙️ Configuration

### Required Settings
- **OpenAI API key** - Your OpenAI API key (required)

### Optional Settings
- **Model** - OpenAI model to use (default: `gpt-4o-mini`)
  - `gpt-4o-mini` - Cost-effective, good quality
  - `gpt-4o` - Higher quality, more expensive
  - `gpt-4-turbo` - Best quality, most expensive

- **Prompt Template** - Customize the AI prompt (advanced)

## 🧪 Testing

### Automated Testing (Optional)
A test script is included to verify plugin functionality:

```bash
# Set your OpenAI API key
export OPENAI_API_KEY="sk-..."

# Run tests
python plugins/devops-cicd-generator/test_plugin.py
```

The test script will:
- Test tech stack extraction logic
- Test trigger prefix stripping
- Test full plugin integration (if API key is provided)

### Manual Testing in Freeway
1. Install Freeway app on macOS
2. Add this plugin folder to Freeway
3. Configure your OpenAI API key in plugin settings
4. Test with voice input:
   - Say: "I have Node.js and MongoDB"
   - Verify generated output contains all expected files

### Expected Output Format
```
=== Dockerfile ===
FROM node:18-alpine AS builder
...

=== docker-compose.yml ===
version: '3.8'
services:
...

=== .github/workflows/ci.yml ===
name: CI/CD Pipeline
...
```

## 🔧 Troubleshooting

### "OpenAI API key is missing"
- Make sure you've entered your API key in plugin settings
- Verify the key is valid and has credits

### "No tech stack description found"
- Make sure you include the trigger phrase "I have"
- Example: "I have Node.js and PostgreSQL" ✓
- Example: "Node.js and PostgreSQL" ✗

### Generated files are incomplete
- Try using a more powerful model (gpt-4o instead of gpt-4o-mini)
- Be more specific about your tech stack
- Check OpenAI API status

## 💡 Tips

1. **Be specific:** Include versions if important (e.g., "Node.js 18", "PostgreSQL 14")
2. **Mention databases:** Always include your database (PostgreSQL, MySQL, MongoDB, etc.)
3. **Include frontend:** If you have a frontend framework, mention it
4. **Multiple services:** Describe all services (e.g., "API service, worker service, frontend")
5. **Review output:** Always review generated files before using in production

## 📚 Supported Tech Stacks

The plugin works with any tech stack, including:

- **Backend:** Node.js, Python (Flask/Django/FastAPI), .NET Core, Go, Java, Ruby, PHP
- **Frontend:** React, Angular, Vue.js, Next.js, Svelte
- **Databases:** PostgreSQL, MySQL, MongoDB, Redis, SQLite
- **Message Queues:** RabbitMQ, Kafka, Redis
- **Web Servers:** Nginx, Apache
- **Cloud:** AWS, Azure, GCP (mentioned in stack)

## 🎓 Best Practices

1. **Review generated files** - Always review and test before production use
2. **Customize as needed** - Generated files are templates, customize for your needs
3. **Security** - Review security settings, especially for production
4. **Environment variables** - Use environment variables for secrets
5. **Testing** - Add tests to CI/CD pipelines

## 📝 License

MIT License - See LICENSE file in repository root.

## 🤝 Contributing

Contributions welcome! Please:
1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## 📞 Support

- **Issues:** https://github.com/tryfreeway/freeway-plugins/issues
- **Documentation:** https://docs.tryfreeway.com
- **Freeway App:** https://tryfreeway.com


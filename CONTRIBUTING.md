# Contributing to WhatsSecure

First, thank you for your interest in contributing to WhatsSecure! We welcome contributions from the community to help improve our security tool.

## Code of Conduct

- Be respectful and inclusive
- Focus on constructive feedback
- Report security issues privately
- Follow ethical security practices

## How to Contribute

### Reporting Issues

1. Check if the issue already exists
2. Provide clear description and steps to reproduce
3. Include environment details (OS, n8n version, Python version, etc.)
4. Security vulnerabilities: See [SECURITY.md](SECURITY.md)

### Submitting Changes

1. **Fork** the repository
2. **Create** a feature branch: `git checkout -b feature/your-feature`
3. **Make** your changes
4. **Test** thoroughly
5. **Commit** with clear messages: `git commit -m "Add: description of changes"`
6. **Push** to your fork: `git push origin feature/your-feature`
7. **Create** a Pull Request with detailed description

### Pull Request Guidelines

- Reference any related issues
- Describe what your changes do
- Include test results (if applicable)
- Keep PRs focused on single features
- Update documentation if needed

## Development Setup

### Prerequisites

- n8n (cloud or self-hosted)
- Node.js 14+ (for local testing)
- Git

### Local Setup

```bash
git clone https://github.com/yourusername/whatsecure.git
cd whatsecure
cp .env.example .env
# Add your API keys to .env
```

### Workflow Testing

1. Export your n8n workflow
2. Test with mock WhatsApp messages
3. Verify threat analysis outputs
4. Check error handling

## Contribution Areas

We welcome contributions in:

- ✅ Threat detection improvements
- ✅ New threat intelligence integrations
- ✅ AI response quality enhancement
- ✅ Error handling and edge cases
- ✅ Documentation improvements
- ✅ Testing and QA
- ✅ UI/UX feedback
- ✅ Translation and localization
- ✅ Security hardening
- ✅ Performance optimization

## Documentation

- Update [README.md](README.md) for feature changes
- Add comments for complex logic
- Document new APIs or integrations
- Keep examples current

## Testing

- Test with various link types
- Verify threat intelligence responses
- Check WhatsApp message handling
- Test error scenarios

## Style Guidelines

- Use clear, descriptive variable names
- Keep n8n workflows modular
- Comment complex logic
- Follow existing code patterns
- Keep JSON workflows properly formatted

## Commit Messages

Use clear, descriptive commit messages:

```
Add: Brief description of addition
Fix: Brief description of bug fix
Improve: Brief description of improvement
Docs: Documentation updates
Refactor: Code restructuring
Test: Test additions
```

## Release Process

Maintainers handle releases, but we follow:

- Semantic versioning (MAJOR.MINOR.PATCH)
- Changelog updates
- Version tag creation
- Release notes documentation

## Questions?

- Open a discussion in GitHub Discussions
- Check existing issues and PRs
- Review documentation

## Legal

By contributing, you agree that your contributions will be licensed under the MIT License.

---

Thank you for making WhatsSecure better! 🙏

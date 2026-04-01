# Security Policy

## Reporting a Vulnerability

The GitPOAP team takes security bugs seriously. We appreciate your efforts to responsibly disclose your findings and will make every effort to acknowledge your contributions.

### How to Report a Security Vulnerability

**Please do not report security vulnerabilities through public GitHub issues.**

Instead, please report them via one of the following methods:

1. **Email**: Send an email to [team@gitpoap.io](mailto:team@gitpoap.io) with the subject line "Security Vulnerability Report"
2. **GitHub Security Advisory**: Use GitHub's [private vulnerability reporting](https://github.com/Kushmanmb/gitpoap-fe/security/advisories/new) feature

Please include the following information in your report:

- Type of vulnerability (e.g., XSS, SQL injection, authentication bypass, etc.)
- Full paths of source file(s) related to the vulnerability
- The location of the affected source code (tag/branch/commit or direct URL)
- Step-by-step instructions to reproduce the issue
- Proof-of-concept or exploit code (if possible)
- Impact of the vulnerability, including how an attacker might exploit it

### What to Expect

- **Acknowledgment**: We will acknowledge receipt of your vulnerability report within 3 business days
- **Communication**: We will keep you informed about our progress throughout the investigation
- **Resolution**: We aim to resolve critical vulnerabilities within 30 days
- **Credit**: We will credit you for your discovery in our security advisory (unless you prefer to remain anonymous)

## Supported Versions

We release patches for security vulnerabilities in the following versions:

| Version | Supported          |
| ------- | ------------------ |
| main    | :white_check_mark: |
| < main  | :x:                |

## Security Best Practices

When contributing to this project, please follow these security best practices:

### Code Security

- Never commit secrets, API keys, or credentials to the repository
- Always use environment variables for sensitive configuration
- Validate and sanitize all user inputs
- Use parameterized queries to prevent injection attacks
- Keep dependencies up to date

### Dependencies

- Regularly update dependencies to patch known vulnerabilities
- Review dependency changes before merging Dependabot PRs
- Use `yarn audit` to check for known vulnerabilities
- Only add dependencies from trusted sources

### Authentication & Authorization

- Never store passwords in plain text
- Use secure, httpOnly cookies for session management
- Implement proper access controls
- Use HTTPS for all production traffic

### Data Protection

- Minimize collection of personal data
- Encrypt sensitive data at rest and in transit
- Follow GDPR and privacy best practices
- Implement proper data retention policies

## Automated Security Measures

This repository implements several automated security measures:

### GitHub Actions Workflows

- **CodeQL Analysis**: Automated code scanning for security vulnerabilities
- **Dependency Review**: Checks for vulnerable dependencies in pull requests
- **Security Audit**: Daily vulnerability scanning of dependencies
- **Dependabot**: Automated dependency updates with security patches

### Branch Protection

We recommend the following branch protection rules for the `main` branch:

- Require pull request reviews before merging
- Require status checks to pass before merging
- Require branches to be up to date before merging
- Include administrators in restrictions
- Restrict who can push to matching branches

### Code Review Requirements

- All code changes must be reviewed by at least one maintainer
- Security-sensitive changes require review from multiple maintainers
- All CI/CD checks must pass before merging

## Security Contact

For any security-related questions or concerns, please contact:

- Email: [team@gitpoap.io](mailto:team@gitpoap.io)
- Discord: [GitPOAP Community](https://discord.gg/qa3mfPvjWm)

## Disclosure Policy

- We will investigate all legitimate reports and do our best to quickly fix the problem
- We will acknowledge security researchers who responsibly report vulnerabilities
- We will publicly disclose vulnerabilities once a fix is available

## Additional Resources

- [GitHub Security Best Practices](https://docs.github.com/en/code-security)
- [OWASP Top Ten](https://owasp.org/www-project-top-ten/)
- [npm Security Best Practices](https://docs.npmjs.com/packages-and-modules/securing-your-code)

Thank you for helping keep GitPOAP and our users safe!

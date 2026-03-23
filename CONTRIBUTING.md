# Contributing to HEAL MATRIX

Thank you for your interest in contributing to HEAL MATRIX! This document provides guidelines and instructions for contributing.

## 🤝 Code of Conduct

- Be respectful and inclusive
- Provide constructive feedback
- Focus on what is best for the community
- Show empathy towards other community members

## 🚀 How to Contribute

### Reporting Bugs

1. **Check existing issues** to avoid duplicates
2. **Use the bug report template**
3. **Include:**
   - Clear description of the bug
   - Steps to reproduce
   - Expected vs actual behavior
   - System information (OS, Python version, etc.)
   - Screenshots if applicable

### Suggesting Enhancements

1. **Check existing feature requests**
2. **Describe the feature clearly**
3. **Explain why it would be useful**
4. **Provide examples if possible**

### Pull Requests

1. **Fork the repository**
2. **Create a feature branch:**
   ```bash
   git checkout -b feature/YourFeatureName
   ```
3. **Make your changes**
4. **Test thoroughly**
5. **Commit with clear messages:**
   ```bash
   git commit -m "Add feature: description of feature"
   ```
6. **Push to your fork:**
   ```bash
   git push origin feature/YourFeatureName
   ```
7. **Open a Pull Request**

## 📝 Code Standards

### Python Style Guide

- Follow [PEP 8](https://pep8.org/)
- Use meaningful variable names
- Add docstrings to functions and classes
- Keep functions focused and small
- Add type hints where appropriate

### Example:

```python
def analyze_symptom(symptom: str, severity: int) -> Dict[str, Any]:
    """
    Analyze a medical symptom and provide recommendations.
    
    Args:
        symptom: Description of the symptom
        severity: Severity level (1-10)
    
    Returns:
        Dictionary with analysis results and recommendations
    """
    # Implementation here
    pass
```

### Commit Messages

- Use present tense ("Add feature" not "Added feature")
- Use imperative mood ("Move cursor to..." not "Moves cursor to...")
- Limit first line to 72 characters
- Reference issues and PRs when applicable

**Good examples:**
```
Add emergency contact feature
Fix appointment scheduling bug #123
Update medical consultation prompt
```

## 🧪 Testing

- Add tests for new features
- Ensure existing tests pass
- Test on multiple environments if possible
- Include edge cases

## 📚 Documentation

- Update README.md if needed
- Add docstrings to new functions
- Update API documentation
- Include code examples

## 🎯 Priority Areas

We're especially interested in contributions for:

1. **Medical Knowledge Base** - Expanding medical information
2. **Multi-language Support** - Translations and localization
3. **Computer Vision** - Improved medical image analysis
4. **Security** - Enhanced data privacy and security
5. **Testing** - Unit tests and integration tests
6. **Documentation** - Tutorials and guides

## ❓ Questions?

- Open an issue with the "question" label
- Contact the maintainers
- Check existing documentation

## 🙏 Recognition

Contributors will be:
- Listed in the README
- Mentioned in release notes
- Given credit in documentation

Thank you for contributing to making healthcare AI more accessible! 🏥✨

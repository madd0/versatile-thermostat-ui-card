# Contributing to Versatile Thermostat UI Card

Thank you for your interest in contributing! 🎉

## Getting Started

### Using GitHub Codespaces (Easiest)

1. Click the **Code** button on the repository
2. Select **Codespaces** → **Create codespace**
3. Wait for the environment to set up (installs dependencies automatically)
4. Run `npm start` to begin development

### Local Setup

See [DEVELOPMENT.md](DEVELOPMENT.md) for detailed local setup instructions.

## How to Contribute

### Reporting Bugs

- Check if the issue already exists
- Provide detailed steps to reproduce
- Include Home Assistant and card versions
- Add screenshots if applicable

### Suggesting Features

- Describe the feature and its use case
- Explain why it would be useful
- Consider if it fits the scope of the project

### Code Contributions

1. **Fork the repository** and create a new branch:
   ```bash
   git checkout -b feature/my-new-feature
   ```

2. **Make your changes**:
   - Follow the existing code style
   - Keep changes focused and atomic
   - Add comments for complex logic

3. **Test your changes**:
   ```bash
   npm run build
   ```

4. **Format your code**:
   ```bash
   npm run format
   ```

5. **Commit with clear messages**:
   ```bash
   git commit -m "feat: add new feature description"
   ```

6. **Push and create a Pull Request**:
   ```bash
   git push origin feature/my-new-feature
   ```

### Translation Contributions

We welcome translations in all languages!

**Using Sherlock VS Code Extension:**
1. Install the inlang Sherlock extension (auto-installed in Codespaces)
2. Edit JSON files in `src/localize/languages/`
3. The extension highlights missing translations

**Using Fink Web Editor:**
```bash
npx @inlang/cli open editor
```

**Manual Translation:**
1. Copy `src/localize/languages/en.json` as a template
2. Create or edit your language file (e.g., `de.json`, `fr.json`)
3. Translate all strings while keeping the keys unchanged
4. Update `src/localize/localize.ts` to import your language
5. Add your language to `project.inlang.json` `languageTags` array

### Commit Message Convention

We follow conventional commits:

- `feat:` - New feature
- `fix:` - Bug fix
- `docs:` - Documentation changes
- `style:` - Code style changes (formatting, etc.)
- `refactor:` - Code refactoring
- `test:` - Adding tests
- `chore:` - Maintenance tasks

Example: `feat: add support for custom icons`

## Code Style

- **Format**: Use Prettier (runs on save in VS Code)
- **TypeScript**: Follow existing patterns
- **Comments**: Add JSDoc for public APIs
- **Naming**: Use descriptive variable names

## Pull Request Process

1. Update documentation if needed
2. Ensure builds succeed (`npm run build`)
3. Format code (`npm run format`)
4. Provide a clear PR description
5. Link related issues
6. Be responsive to review feedback

## Development Tips

- Use `npm start` for hot reload during development
- Test in a real Home Assistant instance when possible
- Check the browser console for errors
- Reference the [Lit documentation](https://lit.dev/) for web components

## Questions?

- Check [DEVELOPMENT.md](DEVELOPMENT.md) for technical details
- Review existing issues and PRs
- Open a discussion for general questions

## Code of Conduct

- Be respectful and constructive
- Welcome newcomers
- Focus on what's best for the project
- Accept feedback gracefully

Thank you for contributing! 🚀

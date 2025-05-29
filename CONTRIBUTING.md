# Contributing to AKIKUBA 🤝

Thank you for your interest in contributing to **AKIKUBA**! We're excited to work with developers, designers, translators, and community members from around the world to build the most complete digital ecosystem for Cuba's cosplay community.

## 📖 Table of Contents

- [🌟 Ways to Contribute](#-ways-to-contribute)
- [🚀 Getting Started](#-getting-started)
- [💻 Development Setup](#-development-setup)
- [🔄 Development Workflow](#-development-workflow)
- [📝 Coding Standards](#-coding-standards)
- [✅ Testing Guidelines](#-testing-guidelines)
- [📚 Documentation](#-documentation)
- [🤝 Community Guidelines](#-community-guidelines)
- [🎯 Issue Guidelines](#-issue-guidelines)
- [🔀 Pull Request Process](#-pull-request-process)
- [📋 Commit Convention](#-commit-convention)
- [🎨 Design Contributions](#-design-contributions)
- [🌍 Translation & Localization](#-translation--localization)
- [❓ Questions & Support](#-questions--support)

## 🌟 Ways to Contribute

### 💻 Code Contributions

- **Frontend Development**: React, Vue, Angular, or framework TBD
- **Backend Development**: Node.js, Python, or stack TBD
- **Mobile Development**: React Native, Flutter, or native apps
- **DevOps & Infrastructure**: CI/CD, deployment, monitoring
- **Security**: Security audits, vulnerability testing
- **Performance**: Optimization, caching, scaling solutions

### 🎨 Design Contributions

- **UI/UX Design**: User interface and experience design
- **Visual Design**: Icons, illustrations, branding
- **Prototyping**: Interactive prototypes and mockups
- **Accessibility**: A11y improvements and testing
- **User Research**: Surveys, interviews, usability testing

### 📝 Content & Documentation

- **Technical Documentation**: API docs, guides, tutorials
- **User Documentation**: Help articles, FAQs, onboarding
- **Translation**: Localization to different languages
- **Content Creation**: Blog posts, case studies, examples
- **Video Content**: Tutorials, demos, walkthroughs

### 🐛 Quality Assurance

- **Bug Reports**: Detailed issue reporting
- **Testing**: Manual and automated testing
- **Code Review**: Reviewing pull requests
- **Performance Testing**: Load testing, benchmarking
- **Security Testing**: Vulnerability assessments

### 🌍 Community Contributions

- **Community Management**: Discord, forums, social media
- **Event Organization**: Meetups, conferences, workshops
- **Mentoring**: Helping new contributors
- **Feedback**: User experience insights
- **Beta Testing**: Early feature testing

## 🚀 Getting Started

### 📋 Prerequisites

Before you start contributing, please:

1. **📖 Read our documentation**:
   - [README.md](README.md) - Project overview
   - [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) - Community standards
   - [SECURITY.md](SECURITY.md) - Security policy
   - [docs/README.md](docs/README.md) - Complete documentation

2. **🔍 Explore the project**:
   - Browse the codebase
   - Check existing issues and discussions
   - Review recent pull requests
   - Understand the project structure

3. **💬 Join the community**:
   - Follow the project on GitHub
   - Join our Discord/Slack (links TBD)
   - Introduce yourself in discussions

### 🔰 First-Time Contributors

New to open source? Welcome! Here's how to get started:

1. **🍴 Fork the repository**
2. **⭐ Star the project** to show your support
3. **🐛 Look for "good first issue" labels**
4. **💬 Ask questions** - we're here to help!
5. **📖 Read our [beginner's guide](docs/12-resources/beginner-guide.md)** (coming soon)

## 💻 Development Setup

### 🛠️ Local Environment

**Note**: Detailed setup instructions will be added as the tech stack is finalized.

#### General Requirements

- **Git**: Version control
- **Node.js**: Latest LTS version (when applicable)
- **Package Manager**: PNPM preferred over npm/yarn
- **IDE**: VS Code recommended with extensions
- **Browser**: Chrome/Firefox with dev tools

#### Development Tools

- **Linting**: ESLint, Prettier
- **Testing**: Jest, Cypress (or framework-specific)
- **Build Tools**: Vite, Webpack (or modern alternatives)
- **Database**: PostgreSQL, MongoDB (TBD)

### 📦 Installation Steps

```bash
# 1. Fork and clone the repository
git clone https://github.com/YOUR_USERNAME/AkiKuba.git
cd AkiKuba

# 2. Install dependencies (when available)
pnpm install

# 3. Set up environment variables
cp .env.example .env.local
# Edit .env.local with your settings

# 4. Start development server
pnpm dev

# 5. Run tests
pnpm test
```

### 🔧 IDE Configuration

#### VS Code Extensions (Recommended)

- **ESLint**: Code linting
- **Prettier**: Code formatting
- **GitLens**: Git supercharged
- **Auto Rename Tag**: HTML/JSX tag renaming
- **Bracket Pair Colorizer**: Better bracket visualization
- **Path Intellisense**: Autocomplete file paths

#### Settings

Use the workspace settings in `.vscode/settings.json` (will be provided).

## 🔄 Development Workflow

### 🌿 Branching Strategy

We use **Git Flow** with the following branches:

- **`main`**: Production-ready code
- **`develop`**: Integration branch for features
- **`feature/*`**: New features
- **`hotfix/*`**: Critical bug fixes
- **`release/*`**: Release preparation

### 📋 Workflow Steps

1. **🔄 Sync your fork** with upstream
2. **🌿 Create a feature branch** from `develop`
3. **💻 Make your changes** following our standards
4. **✅ Test your changes** thoroughly
5. **📝 Write/update documentation** if needed
6. **🔀 Submit a pull request** to `develop`
7. **📊 Address review feedback** promptly
8. **🎉 Celebrate** when merged!

## 📝 Coding Standards

### 🎯 General Principles

- **📖 Readability**: Write code that tells a story
- **🔧 Simplicity**: Prefer simple solutions over complex ones
- **♻️ Reusability**: Write modular, reusable components
- **🛡️ Security**: Always consider security implications
- **⚡ Performance**: Optimize for user experience
- **♿ Accessibility**: Make it accessible to everyone

### 🌐 Frontend Standards

#### JavaScript/TypeScript

```javascript
// ✅ Good: Descriptive function names
function calculateCosplayBudget(materials, labor) {
  return materials.reduce((total, item) => total + item.cost, 0) + labor;
}

// ❌ Bad: Unclear naming
function calc(m, l) {
  return m.reduce((t, i) => t + i.c, 0) + l;
}
```

#### Component Structure

```jsx
// ✅ Good: Clear component structure
interface CosplayCardProps {
  cosplay: Cosplay;
  onLike: (id: string) => void;
  className?: string;
}

export function CosplayCard({ cosplay, onLike, className }: CosplayCardProps) {
  // Component logic here
  return (
    <div className={`cosplay-card ${className}`}>
      {/* JSX here */}
    </div>
  );
}
```

#### CSS/Styling

- **🎨 Use CSS modules** or styled-components
- **📱 Mobile-first** responsive design
- **🎨 Follow design system** colors and spacing
- **♿ Include focus states** for accessibility

### 🔧 Backend Standards

#### API Design

- **🌐 RESTful** endpoints when possible
- **🔀 GraphQL** for complex data fetching
- **📝 Clear documentation** with examples
- **🔒 Security-first** approach
- **⚡ Performance optimization**

#### Code Structure

```javascript
// ✅ Good: Clear error handling
async function getCosplayById(id) {
  try {
    const cosplay = await CosplayModel.findById(id);
    if (!cosplay) {
      throw new NotFoundError('Cosplay not found');
    }
    return cosplay;
  } catch (error) {
    logger.error('Error fetching cosplay:', error);
    throw error;
  }
}
```

### 📁 File Naming Conventions

- **📄 Components**: `PascalCase` (e.g., `CosplayCard.tsx`)
- **📄 Utilities**: `camelCase` (e.g., `formatPrice.ts`)
- **📄 Constants**: `UPPER_SNAKE_CASE` (e.g., `API_ENDPOINTS.ts`)
- **📁 Directories**: `kebab-case` (e.g., `user-profile/`)

## ✅ Testing Guidelines

### 🧪 Testing Strategy

- **🔬 Unit Tests**: Test individual functions/components
- **🔗 Integration Tests**: Test component interactions
- **🌐 E2E Tests**: Test complete user workflows
- **📱 Visual Tests**: Screenshot testing for UI
- **♿ Accessibility Tests**: A11y compliance testing

### 📝 Writing Tests

```javascript
// ✅ Good: Descriptive test names
describe('CosplayCard', () => {
  it('should display cosplay title and creator name', () => {
    // Test implementation
  });

  it('should call onLike when like button is clicked', () => {
    // Test implementation
  });

  it('should be accessible via keyboard navigation', () => {
    // Accessibility test
  });
});
```

### 🎯 Testing Requirements

- **📊 Coverage**: Aim for 80%+ code coverage
- **🔄 CI/CD**: All tests must pass before merge
- **📝 Documentation**: Document complex test scenarios
- **⚡ Performance**: Keep tests fast and reliable

## 📚 Documentation

### 📝 Documentation Types

- **🔧 API Documentation**: Auto-generated from code
- **📖 User Guides**: Step-by-step instructions
- **💻 Developer Docs**: Technical implementation details
- **🎨 Design Docs**: UI/UX specifications
- **📋 Process Docs**: Workflows and procedures

### ✍️ Writing Guidelines

- **🎯 Clear and concise**: Get to the point quickly
- **📝 Use examples**: Show, don't just tell
- **🔄 Keep updated**: Update docs with code changes
- **🌍 Consider audience**: Write for your target readers
- **📸 Include visuals**: Screenshots, diagrams, videos

## 🤝 Community Guidelines

### 🌟 Our Values

- **🤗 Inclusivity**: Everyone is welcome
- **🎓 Learning**: We learn together
- **🤝 Collaboration**: Better together than alone
- **🔍 Transparency**: Open communication always
- **🎉 Fun**: Enjoy the journey!

### 💬 Communication Guidelines

- **🗣️ Be respectful**: Treat everyone with kindness
- **🤔 Be patient**: Everyone is learning
- **💡 Be constructive**: Focus on solutions
- **📝 Be clear**: Communicate your ideas clearly
- **🎯 Stay on topic**: Keep discussions relevant

### 🚫 Unacceptable Behavior

Please review our [Code of Conduct](CODE_OF_CONDUCT.md) for detailed guidelines on unacceptable behavior.

## 🎯 Issue Guidelines

### 🐛 Bug Reports

Use the bug report template and include:

- **📝 Clear description** of the issue
- **🔄 Steps to reproduce** the problem
- **🎯 Expected behavior** vs actual behavior
- **🖥️ Environment details** (OS, browser, version)
- **📸 Screenshots/videos** if applicable
- **🔗 Minimal reproduction** example if possible

### ✨ Feature Requests

Use the feature request template and include:

- **🎯 Problem statement**: What problem does this solve?
- **💡 Proposed solution**: How should it work?
- **🔄 Alternatives considered**: Other approaches you thought of
- **📊 User impact**: Who benefits and how?
- **🖼️ Mockups/examples**: Visual representation if applicable

### 📋 Issue Labels

- **🏷️ Priority**: `high`, `medium`, `low`
- **🏷️ Type**: `bug`, `feature`, `documentation`, `question`
- **🏷️ Difficulty**: `beginner`, `intermediate`, `advanced`
- **🏷️ Status**: `needs-review`, `in-progress`, `blocked`

## 🔀 Pull Request Process

### 📋 PR Checklist

Before submitting your PR, ensure:

- [ ] **🌿 Branch**: Created from `develop` branch
- [ ] **📝 Description**: Clear description of changes
- [ ] **✅ Tests**: All tests pass
- [ ] **📚 Documentation**: Updated if needed
- [ ] **🔍 Self-review**: Reviewed your own code
- [ ] **📊 No conflicts**: Resolved merge conflicts
- [ ] **🏷️ Labels**: Added appropriate labels

### 📝 PR Description Template

```markdown
## 📋 Description
Brief description of what this PR does.

## 🔗 Related Issues
Fixes #123
Related to #456

## 🔄 Type of Change
- [ ] 🐛 Bug fix
- [ ] ✨ New feature
- [ ] 💥 Breaking change
- [ ] 📚 Documentation update

## ✅ Testing
- [ ] Unit tests pass
- [ ] Integration tests pass
- [ ] Manual testing completed

## 📸 Screenshots
If applicable, add screenshots here.

## 📝 Notes
Any additional notes for reviewers.
```

### 🔍 Review Process

1. **🤖 Automated checks** run first
2. **👥 Code review** by maintainers
3. **💬 Feedback** and discussion
4. **🔄 Updates** based on feedback
5. **✅ Approval** and merge

## 📋 Commit Convention

We use [Conventional Commits](https://www.conventionalcommits.org/) format:

### 📝 Format

```
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```

### 🏷️ Types

- **✨ feat**: New feature
- **🐛 fix**: Bug fix
- **📚 docs**: Documentation changes
- **💅 style**: Code style changes (formatting, etc.)
- **♻️ refactor**: Code refactoring
- **⚡ perf**: Performance improvements
- **✅ test**: Adding or updating tests
- **🔧 chore**: Maintenance tasks
- **🎉 init**: Initial commit
- **🚀 deploy**: Deployment-related changes

### 📝 Examples

```bash
git commit -m "feat(auth): add OAuth login with Google"
git commit -m "fix(api): resolve CORS issue in user endpoint"
git commit -m "docs(readme): update installation instructions"
git commit -m "style(components): format CosplayCard component"
```

### 📋 Best Practices

- **🎯 One logical change** per commit
- **📝 Present tense**: "add feature" not "added feature"
- **📏 Keep it short**: Under 72 characters for the subject
- **💡 Explain why**: Use body for context when needed

## 🎨 Design Contributions

### 🎭 Design System

- **🎨 Colors**: Follow AKIKUBA brand guidelines
- **📏 Typography**: Consistent font usage
- **📐 Spacing**: 8px grid system
- **🔘 Components**: Reusable UI components
- **📱 Responsive**: Mobile-first approach

### 🛠️ Design Tools

- **🎨 Figma**: Primary design tool
- **📐 Adobe XD**: Alternative design tool
- **🖼️ Sketch**: For macOS users
- **📊 Miro**: For user journey mapping
- **🎭 Principle**: For prototyping

### 📋 Design Process

1. **🔍 Research**: Understand user needs
2. **💡 Ideation**: Brainstorm solutions
3. **📝 Wireframes**: Create low-fidelity mockups
4. **🎨 Design**: Create high-fidelity designs
5. **🧪 Test**: User testing and feedback
6. **🔄 Iterate**: Refine based on feedback

## 🌍 Translation & Localization

### 🗣️ Supported Languages

- **🇺🇸 English**: Primary language
- **🇪🇸 Spanish**: Primary target (Cuba)
- **🇫🇷 French**: Future consideration
- **🇵🇹 Portuguese**: Future consideration

### 📝 Translation Guidelines

- **🎯 Context**: Understand the context of text
- **🌍 Culture**: Consider cultural differences
- **📏 Length**: Consider text expansion/contraction
- **🔧 Technical**: Maintain technical accuracy
- **✅ Review**: Native speaker review preferred

### 🛠️ Translation Tools

- **🌐 i18next**: Translation framework
- **📋 Crowdin**: Translation management
- **🔧 GitHub**: Direct PR contributions
- **📝 Google Sheets**: Collaborative translation

## ❓ Questions & Support

### 🆘 Getting Help

- **📚 Documentation**: Check our [docs](docs/README.md) first
- **❓ Discussions**: GitHub Discussions for questions
- **🐛 Issues**: GitHub Issues for bugs/features
- **💬 Discord**: Real-time community chat (link TBD)
- **📧 Email**: Contact maintainers directly

### 📞 Contact Information

**Primary Maintainer**: Jonathan Alejandro Rodriguez Lopes

- 🌐 GitHub: [@ItsJhonAlex](https://github.com/ItsJhonAlex)
- 📧 Email: `itsjhonalex@gmail.com`

**Co-Maintainer**: Amanda Beatriz Perez Rodriguez

- 🌐 GitHub: [@Rav3n-Dev](https://github.com/Rav3n-Dev)
- 📧 Email: `coderavenscript@gmail.com`

### 🔄 Response Times

- **🐛 Critical bugs**: Within 24 hours
- **❓ Questions**: Within 2-3 days
- **🔀 PR reviews**: Within 1 week
- **✨ Feature requests**: Within 2 weeks

---

## 🙏 Recognition

We believe in recognizing our contributors! Contributors will be:

- **📝 Listed** in our [Contributors file](CONTRIBUTORS.md)
- **🎉 Mentioned** in release notes for significant contributions
- **🏆 Featured** on our website (when available)
- **🎁 Rewarded** with AKIKUBA swag for major contributions
- **📢 Highlighted** in community showcases

---

## 📄 Legal

By contributing to AKIKUBA, you agree that your contributions will be licensed under the [MIT License](LICENCE). See our [Copyright Policy](docs/09-legal/copyright.md) for more details.

---

*Thank you for making AKIKUBA better! Every contribution, no matter how small, makes a difference in building the best platform for Cuba's cosplay community.* 🇨🇺✨

*"Together, we create something amazing!"* 🤝🚀

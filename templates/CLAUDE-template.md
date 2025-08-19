# ({project-name}) Regenerable Technical Specification & AI Instructions

## Overview

[Brief description of what this project does and why it exists]

## Core Requirements

### [Requirement Category 1]
- [Specific requirement]
- [Another requirement]
- [Detailed technical requirement]

### [Requirement Category 2]
- [Performance requirements]
- [Scalability requirements]
- [Integration requirements]

## Architecture

### [Component 1]
- **Purpose**: [What this component does]
- **Responsibilities**: [Key responsibilities]
- **Dependencies**: [What it depends on]
- **Interfaces**: [How it connects to other components]

### [Component 2]
- **Purpose**: [What this component does]
- **Responsibilities**: [Key responsibilities]
- **Dependencies**: [What it depends on]
- **Interfaces**: [How it connects to other components]

## API Design

### [API Category/Interface]
- `function_name(params)` - [Description of what it does]
- `another_function(params)` - [Description and parameters]

### Error Handling
- [Error types and when they occur]
- [Error message formats]
- [Recovery strategies]

## Implementation Details

### Technology Stack
- **Language**: [Primary language and version]
- **Framework**: [Framework choice and rationale]
- **Database**: [If applicable]
- **Key Dependencies**: [Important libraries with justification]

### File Structure
```
{project-name}/
├── CLAUDE.md                    # This specification
├── README.md                    # End-user documentation
├── DECISIONS.md                 # Architectural decisions
├── src/
│   ├── [component1]/
│   ├── [component2]/
│   └── utils/
├── tests/
│   ├── unit/
│   ├── integration/
│   └── e2e/
├── config/
└── package.json
```

### Data Models
```typescript
interface [ModelName] {
  [property]: [type];  // [description]
  [property]: [type];  // [description]
}
```

### Configuration
- [Configuration file structure]
- [Environment variables]
- [Default values and validation]

## Testing Strategy

### Test Organization
```
tests/
├── unit/           # [What gets unit tested]
├── integration/    # [What gets integration tested]
├── e2e/           # [End-to-end scenarios]
└── helpers/       # [Test utilities and fixtures]
```

### Test Requirements
- **Coverage**: Maintain 90%+ test coverage
- **Performance**: [Performance benchmarks and requirements]
- **Integration**: [External service testing strategy]
- **Regression**: [Bug fix test requirements]

## Quality Standards

### Code Quality
- **TypeScript**: Strict mode enabled
- **Linting**: [Linting rules and configuration]
- **Formatting**: [Code formatting standards]
- **Documentation**: JSDoc for all public APIs

### Performance Requirements
- [Response time requirements]
- [Memory usage constraints]
- [Scalability targets]
- [Benchmark establishment]

## Decision Log Management

### When to Log Decisions
Document any decision that:
- Changes the public API or tool interfaces
- Affects architecture or major code organization
- Chooses between significant alternatives (libraries, patterns, approaches)
- Impacts testing strategy or deployment process
- Resolves a design problem or technical constraint

### Decision Format
```markdown
## Decision #{number} - {YYYY-MM-DD} - {Title}

**Context**: Brief description of the situation requiring a decision

**Decision**: What was decided

**Rationale**: Why this decision was made

**Alternatives**: Other options considered

**Impact**: Expected consequences of this decision

---
```

### Decision Log Archiving
When `DECISIONS.md` reaches 250 entries:
1. Archive entries 1-200 to `DECISIONS-archive-{timestamp}.md`
2. Keep entries 201-250 in active log, renumber as 1-50
3. Add reference to archived file at top of active log

## Important Additional Instructions

### Critical Maintenance Requirements

**CLAUDE.md File Maintenance**:
- This specification MUST be updated whenever any architectural decision is made
- All new features, APIs, or significant changes MUST be documented here
- The specification must remain complete enough to regenerate the entire project
- Version the specification alongside code changes

**README.md File Maintenance**:
- Must be maintained as the primary end-user documentation
- Focus on software description, installation, and usage instructions
- Avoid architectural details or implementation specifics
- Include practical examples and common use cases
- Keep separate from CLAUDE.md with minimal cross-over
- Update whenever user-facing features or installation process changes

**DECISIONS.md File Maintenance**:
- EVERY architectural decision must be logged immediately when made
- Use the specified format consistently
- Reference decision numbers in commit messages and code comments
- Review and update impact assessments as implementations progress

### Code Quality Standards
- **TypeScript Strict Mode**: All code must pass strict type checking
- **Error Handling**: Every operation must have appropriate error handling with AI-friendly messages
- **Logging**: Structured logging at appropriate levels throughout
- **Documentation**: JSDoc comments for all public APIs
- **Performance**: Profile critical paths and optimize for expected load

### AI Development Guidelines
When working with Claude Code or other AI assistance:
- Always reference current CLAUDE.md for project context
- Require decision logging for any architectural changes
- Insist on test coverage for new functionality
- Validate that changes maintain specification compliance
- Update documentation before considering features complete

### Project Regeneration Verification
Periodically verify regeneration capability by:
1. Creating new project from CLAUDE.md specification alone
2. Comparing against existing implementation
3. Identifying and fixing specification gaps
4. Updating specification with missing details

## Installation & Usage

### Development Setup
```bash
# [Installation steps]
npm install
npm run build
npm test
```

### Configuration
```json
{
  // [Configuration example]
}
```

### Usage Examples
```typescript
// [Code examples showing how to use the project]
```

## Deployment

### [Deployment Method]
- [Deployment steps]
- [Environment requirements]
- [Configuration for production]

### Monitoring
- [Logging setup]
- [Metrics collection]
- [Health checks]

## Success Criteria

### Functional Requirements
- ✅ [Specific functional requirement]
- ✅ [Another functional requirement]
- ✅ [Performance requirement]

### Quality Requirements
- ✅ [Test coverage requirement]
- ✅ [Performance benchmark]
- ✅ [Maintainability requirement]

## Regeneration Requirements
This specification contains all information needed to recreate the project:
- Complete architecture and file structure
- Implementation details for all APIs and components
- Testing strategy and organization
- Error handling patterns
- Data validation and transformation logic
- Distribution and deployment setup
- Decision log management process
- Quality standards and maintenance procedures
- README.md maintenance requirements for end-user documentation

This specification provides a comprehensive foundation for building [project description] while maintaining complete regenerability, architectural decision transparency, and clear end-user documentation.
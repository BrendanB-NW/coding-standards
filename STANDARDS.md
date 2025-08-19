# Luke's Coding Standards

## Core Principles

### Regenerable Specifications
Every project must be completely regenerable from its specification:
- **CLAUDE.md** contains complete technical specification and AI instructions
- All architectural decisions, APIs, and implementation details documented
- Specification updated immediately when changes are made
- AI should be able to recreate the entire project from CLAUDE.md alone

### Architectural Decision Logging
All significant decisions must be documented:
- **DECISIONS.md** maintained with standardized format
- Every architectural choice logged immediately when made
- Rationale, alternatives, and impact documented
- Decision numbers referenced in code and commits

### Test-Driven Development
Tests are not optional:
- Write tests before implementing features
- Maintain 90%+ test coverage
- Update tests immediately when changing functionality
- Include negative test cases and edge conditions
- Performance benchmarks for critical paths

### Documentation Separation
Three distinct documentation files with clear purposes:
- **CLAUDE.md**: Technical specification for regeneration
- **README.md**: End-user focused documentation
- **DECISIONS.md**: Architectural decision history

## Project Structure Standards

### Standard File Organization
```
project-name/
├── CLAUDE.md                    # Regenerable technical specification
├── README.md                    # End-user documentation
├── DECISIONS.md                 # Architectural decision log
├── src/                         # Source code
├── tests/                       # Test suites
│   ├── unit/
│   ├── integration/
│   ├── e2e/
│   └── helpers/
├── docs/                        # Additional documentation
├── config/                      # Configuration files
├── scripts/                     # Build/deployment scripts
└── package.json                 # Dependencies and scripts
```

### Naming Conventions
- **Projects**: `kebab-case` with meaningful prefixes (`mcp-mycelium`, `api-gateway`)
- **Files**: `kebab-case.extension` for consistency
- **Functions**: `camelCase` for JavaScript/TypeScript
- **Constants**: `SCREAMING_SNAKE_CASE`
- **Types/Interfaces**: `PascalCase`

## Code Quality Standards

### TypeScript Requirements
- Strict mode enabled always
- No `any` types without explicit justification
- Complete type definitions for all public APIs
- JSDoc comments for all exported functions

### Error Handling
- Every operation must have appropriate error handling
- Error messages should be AI-friendly and descriptive
- Use structured error types with context
- Log errors with sufficient debugging information

### Testing Strategy
- **Unit Tests**: All core modules and utilities
- **Integration Tests**: API interactions and data flows
- **End-to-End Tests**: Complete user workflows
- **Performance Tests**: Critical paths and scalability
- **Regression Tests**: All bug fixes must include tests

### Performance Standards
- Profile critical paths and optimize for expected load
- Establish performance benchmarks and monitor
- Memory usage should scale predictably
- Response times documented and monitored

## AI Development Guidelines

### Working with AI Assistants
- Always reference current CLAUDE.md for project context
- Require decision logging for any architectural changes
- Insist on test coverage for new functionality
- Validate that changes maintain specification compliance
- Update documentation before considering features complete

### Prompt Patterns
- Start with project context: "I'm working on [project] which [brief description]"
- Reference standards: "Following my coding standards from [repo]"
- Be explicit about requirements: "This must include tests and decision logging"
- Request documentation updates: "Update CLAUDE.md to reflect these changes"

## Maintenance Requirements

### Continuous Documentation
- CLAUDE.md updated with every architectural change
- README.md updated when user-facing features change
- DECISIONS.md updated immediately when decisions are made
- All three files version-controlled alongside code

### Quality Gates
Before merging any feature:
- [ ] Tests pass and coverage maintained
- [ ] Documentation updated appropriately
- [ ] Architectural decisions logged if applicable
- [ ] Code follows established patterns
- [ ] Performance impact assessed

### Regeneration Verification
Periodically verify regeneration capability:
1. Create new project from CLAUDE.md specification alone
2. Compare against existing implementation
3. Identify and fix specification gaps
4. Update specification with missing details

## Technology Preferences

### Languages & Frameworks
- **TypeScript** for type safety and tooling
- **Node.js** for server-side applications
- **Modern frameworks** with active communities
- **Established libraries** over bleeding-edge options

### Infrastructure
- **Docker** for containerization and deployment
- **Configuration-driven** setup over hardcoded values
- **Environment-based** configuration management
- **Structured logging** with appropriate levels

### Monitoring & Observability
- Structured logs in JSON format
- Performance metrics for critical operations
- Error tracking with context and stack traces
- Health checks for all services

## Decision Making Framework

### When to Log Decisions
Document any decision that:
- Changes public APIs or interfaces
- Affects architecture or major code organization
- Chooses between significant alternatives
- Impacts testing strategy or deployment
- Resolves design problems or technical constraints

### Decision Criteria
Evaluate options based on:
- **Maintainability**: Can future developers understand and modify?
- **Testability**: Can we write comprehensive tests?
- **Performance**: Does it meet expected load requirements?
- **Documentation**: Can we document it clearly?
- **Regenerability**: Does it support complete project recreation?

## Anti-Patterns to Avoid

### Code Smells
- Functions longer than 50 lines without clear justification
- Classes with more than 10 public methods
- Nested conditionals deeper than 3 levels
- Magic numbers or strings without named constants
- Copy-paste code without refactoring

### Documentation Issues
- Out-of-date specifications that don't match implementation
- Missing decision rationale for architectural choices
- User documentation that assumes technical knowledge
- API documentation without examples

### Testing Problems
- Tests that depend on external services
- Flaky tests that pass/fail randomly
- Tests that test implementation details instead of behavior
- Missing edge case coverage

## Evolution of Standards

These standards should evolve based on project experience:
- Add new patterns that prove successful
- Remove or modify patterns that cause problems
- Update based on new technology capabilities
- Incorporate lessons learned from project retrospectives

Document changes to standards in this repo's own DECISIONS.md file.
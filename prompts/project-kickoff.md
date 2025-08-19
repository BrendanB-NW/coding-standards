# Project Kickoff Prompt Template

Use this template when starting new projects with AI assistance.

## Base Prompt

```
I'm starting a new [type] project called "{project-name}" that [brief description of what it does].

Please follow my coding standards from github.com/lukeh/coding-standards, specifically:

1. **Regenerable Specification**: Create a complete CLAUDE.md file using templates/CLAUDE-template.md that contains everything needed to regenerate this project

2. **Architectural Decision Logging**: Set up DECISIONS.md using templates/DECISIONS-template.md and log all significant architectural decisions immediately

3. **Test-Driven Development**: Implement comprehensive testing with 90%+ coverage including unit, integration, and e2e tests

4. **Documentation Separation**: 
   - CLAUDE.md for technical specification and AI instructions
   - README.md for end-user documentation using templates/README-template.md
   - DECISIONS.md for architectural decisions

5. **Quality Standards**: TypeScript strict mode, structured error handling, JSDoc for public APIs, and performance benchmarking

Key requirements for this project:
- [Specific requirement 1]
- [Specific requirement 2]
- [Performance/scalability requirements]

Technology preferences:
- [Language/framework preferences]
- [Any specific libraries or tools]

Please start by:
1. Creating the project structure following my standards
2. Writing the CLAUDE.md specification
3. Logging the initial technology decisions in DECISIONS.md
4. Setting up the test framework
5. Creating a basic README.md for end users

Ask clarifying questions about requirements before beginning implementation.
```

## Specific Project Type Variants

### MCP Server Project

```
I'm creating a new Model Context Protocol (MCP) server called "{project-name}" that [description].

Follow my coding standards from github.com/lukeh/coding-standards and create:

1. A regenerable CLAUDE.md specification covering:
   - Complete MCP tool definitions and implementations
   - Error handling patterns for AI-friendly responses
   - Performance requirements and optimization strategies
   - Testing approach for MCP protocol compliance

2. MCP-specific requirements:
   - TypeScript with strict typing for all MCP interfaces
   - Comprehensive error handling with descriptive messages
   - Tool validation and input sanitization
   - Performance benchmarks for tool response times

3. Testing strategy including:
   - Unit tests for all tool implementations
   - Integration tests with MCP protocol
   - Performance tests for concurrent requests
   - Mock data for realistic testing scenarios

The MCP tools should provide:
- [List specific tools and their purposes]

Target performance: [response time requirements]
```

### API/Service Project

```
I'm building a [REST API/GraphQL API/microservice] called "{project-name}" that [description].

Follow my coding standards from github.com/lukeh/coding-standards with focus on:

1. API design following REST/GraphQL best practices
2. Comprehensive error handling with structured error responses
3. Input validation and sanitization
4. Performance monitoring and optimization
5. Security considerations and implementation

Key endpoints/operations:
- [List main API endpoints or operations]

Performance requirements:
- [Response time targets]
- [Throughput requirements]
- [Scalability expectations]

Integration requirements:
- [External services or APIs]
- [Database requirements]
- [Authentication/authorization needs]
```

### Library/Package Project

```
I'm creating a [JavaScript/TypeScript] library called "{project-name}" that [description].

Follow my coding standards from github.com/lukeh/coding-standards with emphasis on:

1. Clean, well-documented public API
2. Comprehensive examples and usage documentation
3. Browser and Node.js compatibility (if applicable)
4. Performance benchmarks and optimization
5. Semantic versioning and changelog management

Library should provide:
- [Main functions or classes]
- [Key features and capabilities]

Target users: [describe intended users and use cases]
Distribution: [npm, CDN, etc.]
```

## Customization Guidelines

### Project-Specific Additions

Add these sections as needed:

**For data-heavy projects:**
```
Data requirements:
- [Data sources and formats]
- [Processing requirements]
- [Storage and retrieval patterns]
```

**For UI projects:**
```
UI/UX requirements:
- [Framework preferences]
- [Design system or styling approach]
- [Accessibility requirements]
- [Browser support targets]
```

**For CLI tools:**
```
CLI requirements:
- [Command structure and arguments]
- [Configuration file formats]
- [Output formats and verbosity levels]
- [Shell integration features]
```

### Quality Gate Reminders

Always include:
```
Before considering any feature complete:
- [ ] Tests written and passing
- [ ] Documentation updated (CLAUDE.md, README.md)
- [ ] Architectural decisions logged in DECISIONS.md
- [ ] Error handling implemented with AI-friendly messages
- [ ] Performance benchmarked if applicable
```

### Follow-up Prompts

Use these for ongoing development:

**For feature additions:**
```
I want to add [feature description] to {project-name}.

Reference the current CLAUDE.md for project context and ensure:
1. Update CLAUDE.md with the new feature specification
2. Log any architectural decisions in DECISIONS.md
3. Write tests before implementing
4. Update README.md if user-facing changes
5. Consider performance impact and add benchmarks if needed
```

**For refactoring:**
```
I want to refactor [component/module] in {project-name} to [goal].

Following my coding standards:
1. Log the refactoring decision and rationale in DECISIONS.md
2. Ensure tests cover both old and new behavior during transition
3. Update CLAUDE.md if architecture changes
4. Maintain backward compatibility or document breaking changes
```

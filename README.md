# claude-code
# Feature Documentation Generator

Generate complete documentation for the feature: $ARGUMENTS

## Objective
Produce two documentation artifacts:
1. Developer documentation (technical implementation details)
2. User documentation (end-user guide)

Documentation must follow existing project documentation patterns and naming conventions.

## Arguments
$ARGUMENTS = feature name, feature branch, or related files.

If a feature name is provided:
- Search codebase for related files
- Identify relevant modules, components, APIs, and tests

If files are provided:
- Use those as the primary documentation sources.

## Process

### Step 1 — Discover Context
Identify:
- Related frontend components
- Backend services or APIs
- Database changes
- Config changes
- Tests referencing this feature
- Existing documentation references

Determine feature classification:
- Frontend (UI components, screens)
- Backend (APIs, services, data logic)
- Full-stack (both)

### Step 2 — Analyze Implementation
Extract:
- Purpose of feature
- Architecture decisions
- Dependencies used
- API contracts
- Data flow
- Error handling behavior
- Security considerations
- Performance considerations

### Step 3 — Detect Documentation Patterns
Review existing docs in:
- docs/dev/
- docs/user/

Match:
- Formatting style
- Heading hierarchy
- Naming conventions
- Tone (technical vs user friendly)

### Step 4 — Generate Developer Documentation

Create:

docs/dev/{feature-name}-implementation.md

Must include:

## Overview
Technical description of feature purpose.

## Architecture
Components involved and interactions.

## Implementation Details
Key files and responsibilities.

## API Changes (if applicable)
Endpoints
Request/response formats
Auth requirements

## Data Model Changes
Schema updates
Migrations

## Dependencies
Libraries or services used.

## Testing Strategy
Unit tests
Integration tests
E2E coverage

## Deployment Notes
Configuration requirements
Feature flags
Environment dependencies

## Known Limitations
Edge cases or constraints.

## Related Documentation
Links to:
- Related features
- API docs
- Architecture docs

### Step 5 — Generate User Documentation

Create:

docs/user/how-to-{feature-name}.md

Must include:

## Overview
Simple explanation of feature value.

## When to Use This Feature
Practical scenarios.

## Step-by-Step Instructions

### Step 1
Instruction

[SCREENSHOT: step-1-placeholder]

### Step 2
Instruction

[SCREENSHOT: step-2-placeholder]

### Step 3
Instruction

[SCREENSHOT: result-placeholder]

## Tips
Best practices for usage.

## Troubleshooting
Common problems and solutions.

## FAQ
Common user questions.

## Related Features
Cross-links to other guides.

### Step 6 — Screenshot Handling

If UI exists:
Insert screenshot placeholders:

[SCREENSHOT: feature-overview]
[SCREENSHOT: interaction-flow]
[SCREENSHOT: success-state]

If screenshot tooling exists:
Document capture steps:

Screenshot command:
npm run screenshots {feature}

Otherwise:
Insert TODO markers.

### Step 7 — Cross-Reference Documents

Developer doc must link to:
docs/user/how-to-{feature}.md

User doc must link to:
docs/dev/{feature}-implementation.md (if appropriate)

Link related:
- API documentation
- Related features
- Configuration docs

## Output Requirements

Generate exactly two files:

docs/dev/{feature-name}-implementation.md

docs/user/how-to-{feature-name}.md

Naming rules:
- lowercase
- kebab-case
- descriptive

Example:
password-reset
user-notifications
invoice-export

## Documentation Standards

Developer docs:
- Technical tone
- Precise terminology
- Architecture focus

User docs:
- Simple language
- Action-oriented instructions
- No internal jargon

## Boundaries

Do not:
- Invent functionality not in code
- Document unrelated features
- Assume UI flows without evidence
- Duplicate existing docs unnecessarily

Prefer:
- Existing terminology
- Existing documentation structure
- Existing naming patterns

## Error Handling

If feature cannot be clearly identified:
List possible matches.

If documentation exists:
Update instead of duplicating.

If incomplete implementation:
Document known gaps.

## Completion Checklist

Verify:
✓ Two documentation files created
✓ Naming conventions followed
✓ Cross references included
✓ Screenshot placeholders added
✓ Related docs linked
✓ Feature classification correct

## Success Criteria

Command is complete when:
- Both documents exist
- Documentation matches project patterns
- Cross-references work
- Content reflects actual implementation

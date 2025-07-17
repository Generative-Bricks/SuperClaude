---
allowed-tools: [Read, Write, TodoWrite, Grep, Glob]
description: "Challenge-focused innovation with constraint-based creativity"
---
wave-enabled: false
complexity-threshold: 0.5
performance-profile: standard

# /sc:ideate - Challenge-Focused Innovation

## Purpose
Generate breakthrough solutions for specific challenges using constraint-based creativity and cross-domain thinking.

## Usage
```
/ideate [challenge] [--constraint-creativity budget|time|technology|resources] [--perspective-shift user|competitor|expert|beginner] [--memory-context remember|fresh|selective]
```

## Arguments
- `challenge` - Specific problem, constraint, or opportunity to address
- `--constraint-creativity` - Use limitations as innovation catalysts
- `--perspective-shift` - Force alternative viewpoints for fresh insights
- `--memory-context` - How to leverage previous creative sessions
- `--creativity-level` - Constraint level for solution generation

## Innovation Approaches

### Constraint-Based Creativity
Transform limitations into innovation opportunities:

**Budget Constraints (`--constraint-creativity budget`)**
- Focus on cost-effective, resourceful solutions
- Leverage existing assets and capabilities
- Prioritize high-impact, low-cost innovations
- Auto-activates: brainstormer + constraint-based thinking

**Time Constraints (`--constraint-creativity time`)**
- Rapid iteration and quick wins focus
- Minimal viable solutions with fast deployment
- Leverage existing patterns and proven approaches
- Auto-activates: performance persona for speed optimization

**Technology Constraints (`--constraint-creativity technology`)**
- Work within current tech stack limitations
- Creative use of existing tools and platforms
- Focus on configuration over custom development
- Auto-activates: architect persona for system integration

**Resource Constraints (`--constraint-creativity resources`)**
- Optimize for available team and tool capabilities
- Leverage automation and efficiency multipliers
- Focus on solutions that scale with current resources
- Auto-activates: devops persona for automation opportunities

### Perspective Shifting
Force alternative viewpoints for breakthrough insights:

**User Perspective (`--perspective-shift user`)**
- Customer/end-user needs and pain points focus
- User experience and accessibility priorities
- Real-world usage scenarios and edge cases
- Auto-activates: frontend persona + user-centered design

**Competitor Perspective (`--perspective-shift competitor`)**
- Competitive analysis and differentiation focus
- Market positioning and unique value propositions
- Disruption opportunities and market gaps
- Auto-activates: analyzer persona for competitive intelligence

**Expert Perspective (`--perspective-shift expert`)**
- Domain specialist deep knowledge application
- Advanced techniques and cutting-edge approaches
- Industry best practices and proven methodologies
- Auto-activates: relevant technical persona (security, performance, etc.)

**Beginner Perspective (`--perspective-shift beginner`)**
- Fresh eyes and naive questions approach
- Challenge assumptions and conventional wisdom
- Simple, elegant solutions over complex ones
- Auto-activates: mentor persona for clarity and simplification

**Opposite Perspective (`--perspective-shift opposite`)**
- Contrarian thinking and assumption challenging
- Invert the problem or approach completely
- Question fundamental premises and constraints
- Auto-activates: synthesizer persona for alternative connections

## Memory Integration
- **Challenge Patterns**: Recognizes similar problems and successful solutions
- **Constraint Solutions**: Builds library of creative constraint workarounds
- **Perspective Insights**: Tracks which viewpoints generate breakthrough ideas
- **Cross-Domain Applications**: Connects solutions from different domains

## Innovation Techniques

### Problem Inversion
- Instead of "How to increase user engagement?"
- Ask "How to completely disengage users?" then invert solutions

### Analogical Reasoning
- How do other industries solve similar challenges?
- What biological/natural systems address comparable problems?
- How would different cultures or time periods approach this?

### Assumption Challenging
- List all assumptions about the challenge
- Systematically question each assumption
- Generate solutions that violate key assumptions

### Resource Reframing
- What if you had unlimited resources?
- What if you had zero resources?
- What if you could only use what's already available?

## Execution
1. Analyze challenge and identify core constraints
2. Apply perspective shifting for fresh viewpoints
3. Use constraints as creative catalysts rather than limitations
4. Generate solutions that embrace or creatively work around constraints
5. Leverage memory for similar challenge patterns and successful solutions
6. Synthesize breakthrough approaches that combine insights

## Claude Code Integration
- Uses Memory MCP for challenge pattern recognition
- Leverages Sequential for systematic constraint analysis
- Applies Context7 for cross-domain solution examples
- Auto-activates appropriate personas based on perspective and constraints

## Example Sessions
```
/ideate "improve app performance on low-end devices" --constraint-creativity technology --perspective-shift user

/ideate "increase team productivity with limited budget" --constraint-creativity budget --perspective-shift expert --memory-context remember

/ideate "reduce customer support load" --perspective-shift opposite --creativity-level wild --memory-context fresh
```
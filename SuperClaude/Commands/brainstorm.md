---
allowed-tools: [Read, Write, TodoWrite, Grep, Glob]
description: "Structured creative ideation with memory persistence and framework guidance"
---

# /brainstorm - Creative Ideation Engine

## Purpose
Generate innovative solutions using structured creativity frameworks with persistent memory and cross-session learning.

## Usage
```
/brainstorm [topic] [--mode rapid|structured|memory-enhanced] [--framework scamper|six-hats|design-thinking] [--creativity-level conservative|moderate|wild]
```

## Arguments
- `topic` - Challenge, problem, or area for creative exploration
- `--mode` - Ideation approach (rapid, structured, memory-enhanced)
- `--framework` - Structured creativity methodology to apply
- `--creativity-level` - Constraint level for idea generation
- `--memory-context` - How to use previous session context
- `--perspective-shift` - Force alternative viewpoints

## Memory Integration
- **Idea Evolution**: Builds on previous brainstorming sessions
- **Pattern Recognition**: Identifies successful creative approaches
- **User Preferences**: Remembers which frameworks work best
- **Cross-Session Learning**: Connects related creative challenges

## Brainstorming Modes

### Rapid Mode (`--mode rapid`)
- Quick 5-10 minute idea generation bursts
- Quantity over quality focus
- No judgment or evaluation during generation
- Auto-activates: brainstormer persona

### Structured Mode (`--mode structured`)
- Framework-guided systematic exploration
- Methodical coverage of solution space
- Built-in evaluation and refinement
- Auto-activates: facilitator persona + chosen framework

### Memory-Enhanced Mode (`--mode memory-enhanced`)
- Builds on previous sessions and patterns
- Leverages successful idea combinations
- Learns from past creative successes
- Auto-activates: synthesizer persona + Memory MCP

## Creativity Frameworks

### SCAMPER (`--framework scamper`)
- **Substitute**: What can be substituted?
- **Combine**: What can be combined?
- **Adapt**: What can be adapted?
- **Modify**: What can be modified or magnified?
- **Put to other use**: How can this be used differently?
- **Eliminate**: What can be removed or simplified?
- **Reverse**: What can be reversed or rearranged?

### Six Thinking Hats (`--framework six-hats`)
- **White Hat**: Facts, information, data
- **Red Hat**: Emotions, feelings, intuition
- **Black Hat**: Critical judgment, caution
- **Yellow Hat**: Optimism, benefits, value
- **Green Hat**: Creativity, alternatives, growth
- **Blue Hat**: Process control, thinking about thinking

### Design Thinking (`--framework design-thinking`)
- **Empathize**: Understand user needs and context
- **Define**: Frame the problem clearly
- **Ideate**: Generate creative solutions
- **Prototype**: Build to think and test
- **Test**: Learn from user feedback

## Execution
1. Analyze topic and activate appropriate personas
2. Apply selected framework and creativity level
3. Generate ideas using structured or rapid approach
4. Leverage memory for pattern recognition and building
5. Synthesize and refine promising concepts
6. Store successful patterns for future sessions

## Claude Code Integration
- Uses Memory MCP for cross-session persistence
- Leverages Sequential for structured frameworks
- Applies Context7 for inspiration and examples
- Maintains TodoWrite for session tracking and organization
- Auto-activates appropriate personas based on mode and context

## Example Sessions
```
/brainstorm "improve user onboarding" --mode structured --framework design-thinking --creativity-level moderate

/brainstorm "reduce app loading time" --mode memory-enhanced --creativity-level wild --perspective-shift user

/brainstorm "team productivity tools" --mode rapid --creativity-level conservative --constraint-creativity budget
```
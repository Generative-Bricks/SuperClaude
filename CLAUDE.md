# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

SuperClaude is a framework that extends Claude Code with specialized commands, personas, and MCP server integration. It provides 19 specialized commands, smart personas that adapt behavior for different domains, and MCP server integration for enhanced capabilities.

**Architecture**: Python-based framework with modular installation system, comprehensive documentation, and integrated MCP server orchestration.

## Development Commands

### Installation & Setup
```bash
# Install SuperClaude framework
python3 SuperClaude.py install --quick

# Development installation with all components
python3 SuperClaude.py install --profile developer

# Check what components are available
python3 SuperClaude.py install --list-components

# Interactive installation
python3 SuperClaude.py install
```

### Core Operations
```bash
# Update existing installation
python3 SuperClaude.py update

# Remove installation
python3 SuperClaude.py uninstall

# Create backup
python3 SuperClaude.py backup --create

# Dry run any operation
python3 SuperClaude.py install --dry-run
```

### Validation & Testing
```bash
# Run system validation
python3 -c "from setup.core.validator import Validator; v = Validator(); print(v.validate_system())"

# Check installation requirements
python3 -c "from setup.core.config_manager import ConfigManager; cm = ConfigManager(); print(cm.validate_requirements())"
```

## High-Level Architecture

### Core Components

**SuperClaude.py**: Main entry point and unified CLI hub for all operations (install, update, uninstall, backup)

**SuperClaude/Core/**: Framework behavior documentation that guides Claude Code:
- `CLAUDE.md`: Entry point referencing all other core files
- `COMMANDS.md`: 19 specialized command definitions and execution framework
- `PERSONAS.md`: 14 domain-specific AI personalities with auto-activation
- `MCP.md`: Integration with Context7, Sequential, Magic, and Playwright servers
- `FLAGS.md`: Command flags and auto-activation patterns
- `ORCHESTRATOR.md`: Intelligent routing and decision-making system
- `PRINCIPLES.md`: Development principles and quality standards
- `RULES.md`: Actionable operational rules
- `MODES.md`: Task management, introspection, and token efficiency modes

**SuperClaude/Commands/**: Slash command definitions (analyze, build, improve, etc.)

**setup/**: Modular installation system with components, operations, and utilities

### Installation System Architecture

**setup/operations/**: Core operations (install, update, uninstall, backup)
**setup/components/**: Installable components (core, commands, mcp, hooks)
**setup/core/**: Configuration management, validation, and registry systems
**setup/utils/**: UI components, logging, and security utilities

### Component Registry
Components are registered and managed through:
- **config/**: Feature definitions and system requirements
- **profiles/**: Installation profiles (quick, minimal, developer)
- Component dependencies and validation rules

### Framework Integration
The framework integrates with Claude Code through:
1. **Documentation Files**: Installed to `~/.claude/` to guide behavior
2. **Slash Commands**: 15 specialized commands for development tasks
3. **MCP Servers**: External services for documentation, UI generation, testing
4. **Smart Routing**: Automatic tool and persona selection

## Key Development Patterns

### Configuration Management
- JSON-based configuration in `config/` directory
- Profile-based installation with component selection
- Requirement validation for Python, Node.js, Claude CLI
- Modular component architecture with dependency tracking

### Installation Architecture
- **Base Classes**: `Installer`, `Component` for extensible architecture
- **Registry System**: `ComponentRegistry` for tracking installed components
- **Validation Layer**: `Validator` for system requirements and compatibility
- **Operation Pattern**: Separate modules for install/update/uninstall operations

### Error Handling & Logging
- Comprehensive logging system with file and console output
- Graceful fallback mechanisms for missing dependencies
- Dry-run support for all operations
- Progress tracking and user feedback

### File Organization
- **Absolute paths** for all file operations
- **Security validation** to prevent path traversal
- **Backup systems** before making changes
- **Transaction-like behavior** for installation operations

## Common Development Tasks

### Adding New Commands
1. Create command definition in `SuperClaude/Commands/[command].md`
2. Add command to `COMMANDS.md` with proper YAML metadata
3. Include allowed tools, persona mappings, and MCP integrations

### Adding New Components
1. Create component class inheriting from `setup.base.component.Component`
2. Register in `setup/components/__init__.py`
3. Add to appropriate installation profiles
4. Update requirements in `config/requirements.json`

### Modifying Installation Behavior
1. Update operation modules in `setup/operations/`
2. Modify base installer logic in `setup/base/installer.py`
3. Update CLI argument parsing in respective operation modules
4. Test with `--dry-run` flag

### Framework Development
- Core behavior changes go in `SuperClaude/Core/`
- Command definitions in `SuperClaude/Commands/`
- Installation components in `setup/components/`
- Configuration changes in `config/` and `profiles/`

## Important Notes

### Security Considerations
- All file operations use absolute paths to prevent path traversal
- System validation before installation
- User confirmation for destructive operations
- Backup creation before major changes

### Version Compatibility
- Python 3.8+ required for framework
- Node.js 16+ required for MCP servers
- Claude CLI required for MCP integration
- Git recommended for development workflows

### Framework Behavior
The installed framework modifies Claude Code behavior through documentation files that provide:
- Automatic persona activation based on task context
- MCP server orchestration for enhanced capabilities
- Intelligent routing and tool selection
- Token optimization and efficiency modes

### Installation Process
1. System validation (Python, Node.js, disk space)
2. Component selection (via profiles or interactive)
3. File installation to `~/.claude/` directory
4. MCP server setup (if selected)
5. Configuration validation and testing
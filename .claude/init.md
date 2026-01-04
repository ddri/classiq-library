# Classiq Library - Quantum Computing Repository

This repository contains quantum algorithms, applications, and tutorials built with the Classiq platform.

## Repository Structure

- **algorithms/** - Quantum algorithms (Grover, Shor, QAOA, VQE, QPE, etc.)
- **applications/** - Real-world applications (chemistry, finance, optimization, CFD)
- **tutorials/** - Learning materials and educational notebooks
- **functions/** - Reusable quantum functions
- **research/** - Research implementations
- **built_in_apps/** - Built-in Classiq applications

## File Types

### QMOD Files (`.qmod`)
- Quantum Model Definition files
- Define quantum programs in Classiq's quantum language
- Upload to https://platform.classiq.io/synthesis for GUI synthesis

### Jupyter Notebooks (`.ipynb`)
- Interactive tutorials and examples
- Combine quantum code with explanations
- Use Classiq Python SDK

### Synthesis Options (`.synthesis_options.json`)
- Configuration for quantum program synthesis
- Optimization parameters (circuit depth, qubit count, etc.)

### Metadata Files (`.metadata.json`)
- Notebook/QMOD metadata for documentation system
- Required fields: title, description, tags, etc.

## Common Patterns

### Classiq SDK Workflow
1. Define quantum logic with `@qfunc` decorators
2. Create model: `create_model(main)`
3. Synthesize: `synthesize(model)`
4. Execute: `execute(quantum_program)`

### Quantum Types
- `QBit` - Single qubit
- `QNum` - Quantum number (register)
- `QArray` - Array of qubits
- `Output[T]` - Output quantum variable

## Important Commands

### Testing
```bash
pytest tests/                    # Run all tests
pytest -k "test_name"           # Run specific test
```

### Pre-commit Hooks
- Validates notebook metadata
- Strips notebook outputs
- Checks QMOD syntax
- Auto-formats code

## Git Workflow

### Upstream Repository
- **Upstream**: https://github.com/Classiq/classiq-library.git (parent)
- **Origin**: https://github.com/ddri/classiq-library.git (your fork)

### Staying in Sync
Use `/sync-upstream` command to pull latest changes from parent repo.

## Documentation Links

- [Classiq Platform](https://platform.classiq.io/)
- [Classiq Documentation](https://docs.classiq.io/latest/)
- [Python SDK Reference](https://docs.classiq.io/latest/reference-manual/python-sdk/)
- [QMOD Language Reference](https://docs.classiq.io/latest/reference-manual/platform/qmod/)

## Development Tips

1. **Always check metadata** - Notebooks need proper metadata.json files
2. **Test before committing** - Pre-commit hooks will validate your changes
3. **Follow naming conventions** - Use descriptive names for algorithms/examples
4. **Add synthesis options** - Each QMOD should have synthesis options
5. **Update outputs carefully** - Use internal tools for updating notebook outputs

## Python Environment

- **SDK**: `pip install classiq`
- **Python Version**: 3.8-3.11 (3.12 not yet supported - see Issue #17)
- **Testing**: Uses pytest framework

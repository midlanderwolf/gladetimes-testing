# Agent Instructions for bustimes.org

## Commands

### Frontend (TypeScript/React)
- **Build**: `npm run build`
- **Lint**: `npm run lint`
- **Test**: `npm run test`
- **Single test**: `npm test -- <test_file>`
- **Watch**: `npm run watch`

### Backend (Django/Python)
- **Test**: `uv run ./manage.py test`
- **Single test**: `uv run ./manage.py test <app>.<TestClass>.<test_method>`
- **Coverage**: `uv run coverage run ./manage.py test` then `uv run coverage html`
- **Lint**: `ruff check --fix` and `ruff format`

### Pre-commit Hooks (auto-run)
- ruff-check --fix, ruff-format, biome-check --unsafe, djade

## Code Style

### Python
- **Imports**: stdlib → third-party → local (one per line)
- **Formatting**: Ruff (Black-compatible)
- **Naming**: snake_case functions/variables, PascalCase classes
- **Tests**: `test_` prefix, Django TestCase, descriptive docstrings
- **Error handling**: Standard try/except, log appropriately

### TypeScript/React
- **Imports**: React → third-party → local components
- **Formatting**: Biome (spaces, recommended rules)
- **Naming**: PascalCase components, camelCase functions/variables
- **Types**: Explicit annotations, `type` for interfaces
- **Tests**: @testing-library/react, jsdom environment

### General
- **Templates**: djade formatting for Django templates
- **CSS**: Standard SCSS via Parcel
- **Comments**: Only for complex logic
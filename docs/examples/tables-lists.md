# Tables and Lists Examples

Comprehensive examples of tables and lists in MkDocs.

## Simple Tables

### Basic Table

| Name | Age | City |
|------|-----|------|
| Alice | 28 | New York |
| Bob | 35 | Los Angeles |
| Carol | 42 | Chicago |

### Aligned Columns

| Left Aligned | Center Aligned | Right Aligned |
|:-------------|:--------------:|--------------:|
| Left | Center | Right |
| Text | Text | Text |
| 123 | 456 | 789 |

## Complex Tables

### Feature Comparison

| Feature | Basic | Pro | Enterprise |
|:--------|:-----:|:---:|:----------:|
| Users | 5 | 25 | Unlimited |
| Storage | 1 GB | 10 GB | 100 GB |
| Support | Email | Priority | 24/7 Phone |
| API Access | No | Yes | Yes |
| Custom Domain | No | Yes | Yes |
| SSO | No | No | Yes |
| Price | Free | $19/mo | $99/mo |

### Status Table

| Service | Status | Uptime | Last Incident |
|---------|--------|--------|---------------|
| API | **Operational** | 99.99% | 30 days ago |
| Website | **Operational** | 99.95% | 15 days ago |
| Database | **Degraded** | 99.50% | Today |
| CDN | **Operational** | 100% | Never |

### Technical Specifications

| Component | Specification | Notes |
|-----------|---------------|-------|
| CPU | Intel i7-12700K | 12 cores, 20 threads |
| RAM | 32 GB DDR5 | 4800 MHz |
| Storage | 1 TB NVMe SSD | PCIe 4.0 |
| GPU | NVIDIA RTX 4080 | 16 GB VRAM |
| PSU | 850W 80+ Gold | Fully modular |

## Lists

### Unordered Lists

Basic list:

- Item one
- Item two
- Item three

Nested list:

- Frontend
  - HTML
  - CSS
  - JavaScript
    - React
    - Vue
    - Angular
- Backend
  - Python
  - Node.js
  - Go
- Database
  - PostgreSQL
  - MongoDB

### Ordered Lists

Steps to deploy:

1. Clone the repository
2. Install dependencies
3. Configure environment variables
4. Build the application
5. Deploy to server

Nested ordered list:

1. Planning Phase
   1. Gather requirements
   2. Create specifications
   3. Design architecture
2. Development Phase
   1. Set up environment
   2. Implement features
   3. Write tests
3. Deployment Phase
   1. Stage for testing
   2. Get approval
   3. Deploy to production

### Mixed Lists

Project structure:

1. **Source Code**
   - `src/` - Main source files
   - `lib/` - Library code
   - `tests/` - Test files

2. **Configuration**
   - `config.yaml` - Main config
   - `.env` - Environment variables

3. **Documentation**
   - `README.md`
   - `docs/` folder

### Task Lists

Project progress:

- [x] Create project structure
- [x] Set up development environment
- [x] Implement core features
- [ ] Write documentation
- [ ] Add unit tests
- [ ] Deploy to production

### Definition Lists

HTTP Methods
:   The standard methods used in RESTful APIs

GET
:   Retrieve a resource

POST
:   Create a new resource

PUT
:   Update an existing resource

DELETE
:   Remove a resource

## Combined Tables and Lists

### Requirements Matrix

| Requirement | Priority | Status | Notes |
|-------------|----------|--------|-------|
| User authentication | High | Done | Uses JWT |
| Data export | Medium | In Progress | - CSV format<br>- JSON format |
| Email notifications | Low | Planned | Features:<br>- Welcome email<br>- Password reset |

## Practical Examples

### Keyboard Shortcuts

| Action | Windows/Linux | macOS |
|--------|---------------|-------|
| Save | <kbd>Ctrl</kbd>+<kbd>S</kbd> | <kbd>Cmd</kbd>+<kbd>S</kbd> |
| Copy | <kbd>Ctrl</kbd>+<kbd>C</kbd> | <kbd>Cmd</kbd>+<kbd>C</kbd> |
| Paste | <kbd>Ctrl</kbd>+<kbd>V</kbd> | <kbd>Cmd</kbd>+<kbd>V</kbd> |
| Undo | <kbd>Ctrl</kbd>+<kbd>Z</kbd> | <kbd>Cmd</kbd>+<kbd>Z</kbd> |
| Find | <kbd>Ctrl</kbd>+<kbd>F</kbd> | <kbd>Cmd</kbd>+<kbd>F</kbd> |

### Command Reference

| Command | Description | Example |
|---------|-------------|---------|
| `mkdocs serve` | Start dev server | `mkdocs serve -a localhost:8080` |
| `mkdocs build` | Build static site | `mkdocs build --clean` |
| `mkdocs gh-deploy` | Deploy to GitHub | `mkdocs gh-deploy --force` |
| `mkdocs new` | Create new project | `mkdocs new my-docs` |

### Version History

| Version | Date | Changes |
|---------|------|---------|
| 2.0.0 | 2024-01-15 | - Major redesign<br>- New API<br>- Breaking changes |
| 1.5.0 | 2023-11-01 | - Added dark mode<br>- Performance improvements |
| 1.4.0 | 2023-08-15 | - New export feature<br>- Bug fixes |
| 1.3.0 | 2023-05-01 | - Added search<br>- UI updates |

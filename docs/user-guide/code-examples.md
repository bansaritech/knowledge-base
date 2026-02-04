# Code Examples

MkDocs provides excellent support for displaying code with syntax highlighting.

## Inline Code

Use backticks for inline code:

```markdown
Use the `print()` function to output text.
The `config.yml` file contains settings.
```

Use the `print()` function to output text.
The `config.yml` file contains settings.

## Code Blocks

### Basic Code Block

Use triple backticks:

    ```
    This is a code block
    No syntax highlighting
    ```

### Syntax Highlighting

Specify the language after the opening backticks:

    ```python
    def hello_world():
        print("Hello, World!")
    ```

```python
def hello_world():
    print("Hello, World!")
```

## Language Examples

### Python

```python
class Calculator:
    """A simple calculator class."""

    def add(self, a: int, b: int) -> int:
        """Add two numbers."""
        return a + b

    def subtract(self, a: int, b: int) -> int:
        """Subtract b from a."""
        return a - b

# Usage
calc = Calculator()
result = calc.add(5, 3)
print(f"Result: {result}")
```

### JavaScript

```javascript
// ES6 Class Example
class UserService {
  constructor(apiUrl) {
    this.apiUrl = apiUrl;
  }

  async getUser(id) {
    const response = await fetch(`${this.apiUrl}/users/${id}`);
    return response.json();
  }

  async createUser(userData) {
    const response = await fetch(`${this.apiUrl}/users`, {
      method: 'POST',
      headers: { 'Content-Type': 'application/json' },
      body: JSON.stringify(userData)
    });
    return response.json();
  }
}

// Usage
const service = new UserService('https://api.example.com');
const user = await service.getUser(123);
```

### TypeScript

```typescript
interface User {
  id: number;
  name: string;
  email: string;
  role: 'admin' | 'user' | 'guest';
}

function greetUser(user: User): string {
  return `Hello, ${user.name}!`;
}

const user: User = {
  id: 1,
  name: 'John Doe',
  email: 'john@example.com',
  role: 'admin'
};

console.log(greetUser(user));
```

### Bash / Shell

```bash
#!/bin/bash

# Variables
PROJECT_NAME="my-project"
BUILD_DIR="./dist"

# Function to build project
build_project() {
    echo "Building $PROJECT_NAME..."
    mkdir -p $BUILD_DIR
    npm run build
    echo "Build complete!"
}

# Main execution
if [ -d "$BUILD_DIR" ]; then
    rm -rf $BUILD_DIR
fi

build_project
```

### SQL

```sql
-- Create users table
CREATE TABLE users (
    id SERIAL PRIMARY KEY,
    username VARCHAR(50) UNIQUE NOT NULL,
    email VARCHAR(100) UNIQUE NOT NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

-- Insert sample data
INSERT INTO users (username, email) VALUES
    ('john_doe', 'john@example.com'),
    ('jane_smith', 'jane@example.com');

-- Query with JOIN
SELECT
    u.username,
    COUNT(o.id) as order_count
FROM users u
LEFT JOIN orders o ON u.id = o.user_id
GROUP BY u.username
ORDER BY order_count DESC;
```

### YAML

```yaml
# Docker Compose configuration
version: '3.8'

services:
  web:
    build: .
    ports:
      - "8000:8000"
    environment:
      - DEBUG=true
      - DATABASE_URL=postgres://db:5432/mydb
    depends_on:
      - db
    volumes:
      - .:/app

  db:
    image: postgres:13
    environment:
      POSTGRES_DB: mydb
      POSTGRES_PASSWORD: secret
    volumes:
      - postgres_data:/var/lib/postgresql/data

volumes:
  postgres_data:
```

### JSON

```json
{
  "name": "my-project",
  "version": "1.0.0",
  "description": "A sample project",
  "main": "index.js",
  "scripts": {
    "start": "node index.js",
    "test": "jest",
    "build": "webpack --mode production"
  },
  "dependencies": {
    "express": "^4.18.0",
    "lodash": "^4.17.21"
  },
  "devDependencies": {
    "jest": "^29.0.0"
  }
}
```

### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Page</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <nav>
            <a href="/">Home</a>
            <a href="/about">About</a>
        </nav>
    </header>
    <main>
        <h1>Welcome</h1>
        <p>This is a sample page.</p>
    </main>
    <script src="app.js"></script>
</body>
</html>
```

### CSS

```css
/* Modern CSS with variables */
:root {
  --primary-color: #007bff;
  --secondary-color: #6c757d;
  --font-family: 'Segoe UI', sans-serif;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 1rem;
}

.button {
  background-color: var(--primary-color);
  color: white;
  padding: 0.75rem 1.5rem;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.button:hover {
  background-color: darken(var(--primary-color), 10%);
}
```

## Code with Line Numbers

Some themes support line numbers:

    ```python linenums="1"
    def fibonacci(n):
        if n <= 1:
            return n
        return fibonacci(n-1) + fibonacci(n-2)
    ```

## Highlighting Specific Lines

With some extensions, highlight specific lines:

    ```python hl_lines="2 3"
    def example():
        # This line is highlighted
        # This one too
        return True
    ```

## Supported Languages

MkDocs supports many languages including:

| Category | Languages |
|----------|-----------|
| Web | HTML, CSS, JavaScript, TypeScript |
| Backend | Python, Java, C#, Go, Rust, PHP |
| Data | SQL, JSON, YAML, XML |
| Shell | Bash, PowerShell, Zsh |
| Config | TOML, INI, Dockerfile |
| Other | Markdown, LaTeX, Diff |

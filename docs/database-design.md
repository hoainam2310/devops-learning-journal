# Database Design

## Entity: Note

A Note represents a DevOps learning note.

## Attributes

| Attribute | Description |
|------------|------------|
| id | Unique identifier |
| title | Note title |
| category | Note category |
| content | Note content |
| created_at | Creation timestamp |
| updated_at | Last update timestamp |

## Design Decisions

### Categories

For MVP, a note belongs to one category only.

Examples:
- Docker
- Git
- Linux
- CI/CD
- Jira

### Users

For MVP, notes are owned by a single user only.

Multi-user support will be considered in future versions.
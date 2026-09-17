# Database Design

## Entity: Note

A Note represents a DevOps learning note.

## Attributes

| Attribute | Description |
|------------|------------|
| id | Unique identifier |
| title | Note title |
| category | Note category |
| tags | Note tags |
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

### Tags

A note can contain zero or more tags.

Examples:
- networking
- volume
- git
- github-actions
- spring-boot

Tags are used to improve search and organization.

### Content Format

Notes are stored in Markdown format.

Examples:

# Docker Networking

## Bridge Network

docker network ls

Benefits:
- Better readability
- Supports code blocks
- Supports headings
- Supports lists
- Useful for DevOps commands, YAML, JSON and documentation

### Delete Strategy

MVP:
- Hard delete only (Delete note -> Gone forever)

Future:
- Soft delete support (Can restore later)
- Restore deleted notes
- Permanent delete option

### Attachments

MVP:
- No attachment support

Future:
- Upload images
- Upload log files
- Upload architecture diagrams
- Upload documents

Reason:
- Keep MVP simple
- Avoid file storage complexity
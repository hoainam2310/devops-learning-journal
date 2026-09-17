# API Design

## Design Principles

The application follows REST principles.

Each API maps directly to an MVP feature.

## HTTP Methods

| Method | Purpose | CRUD Operation |
|----------|----------|----------|
| GET | Retrieve data | Read |
| POST | Create data | Create |
| PUT | Update existing data | Update |
| DELETE | Delete data | Delete |

Examples:

GET /notes
- Retrieve all notes

POST /notes
- Create a new note

PUT /notes/{id}
- Update an existing note

DELETE /notes/{id}
- Delete a note

---

## Base URL

/api

Examples:

GET /api/notes

POST /api/notes

PUT /api/notes/{id}

DELETE /api/notes/{id}

---

## Notes API

### Create Note

POST /api/notes

Purpose:
Create a new note.

Related MVP Feature:
- Create Note

### Get All Notes

GET /api/notes

Purpose:
Retrieve all notes.

Related MVP Feature:
- View Notes

### Get Note By ID

GET /api/notes/{id}

Purpose:
Retrieve a specific note.

Related MVP Feature:
- View Note Details

### Update Note

PUT /api/notes/{id}

Purpose:
Update an existing note.

Related MVP Feature:
- Edit Note

### Delete Note

DELETE /api/notes/{id}

Purpose:
Delete a note.

Related MVP Feature:
- Delete Note

---

## Search API

### Search Notes

GET /api/notes/search

Purpose:
Search notes by title, category, tags, or content.

Related MVP Feature:
- Search Notes

Example:

GET /api/notes/search?q=docker

---

## Response Format

Example Note:

{
  "id": 1,
  "title": "Docker Networking",
  "category": "Docker",
  "tags": ["networking", "bridge"],
  "content": "# Docker Networking",
  "createdAt": "2026-09-17T10:00:00Z",
  "updatedAt": "2026-09-17T10:00:00Z"
}

---

## Error Handling

404 Not Found
- Note does not exist

400 Bad Request
- Invalid request data

500 Internal Server Error
- Unexpected server error

Example:

{
  "message": "Note not found"
}
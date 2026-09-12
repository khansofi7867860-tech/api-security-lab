# BOLA — Broken Object Level Authorization

## Scenario

The API contains projects belonging to different organizations.

- Sofia belongs to Organization 1.
- Project 101 belongs to Organization 1.
- Project 202 belongs to Organization 2.

## Test

Authenticated as Sofia:

```http
X-User-ID: 1
GET /projects/202


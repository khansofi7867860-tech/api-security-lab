BOLA — Broken Object Level Authorization
Scenario

The API contains projects belonging to different organizations.

Sofia belongs to Organization 1.
Project 101 belongs to Organization 1.
Project 202 belongs to Organization 2.
Test

Authenticated as Sofia:

X-User-ID: 1
GET /projects/202
Expected behavior

The API should deny access because Project 202 belongs to another organization.

Actual behavior

The API returns Project 202.

Root cause

The endpoint verifies the user's identity but does not verify whether the authenticated user is authorized to access the requested project.

Security concept

Authentication establishes the identity of the requester.

Authorization determines whether that requester can access the requested object.

Status

Vulnerable — remediation not yet implemented.

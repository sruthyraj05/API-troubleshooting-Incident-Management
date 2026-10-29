# Workflow — API Troubleshooting & Incident Management System

1. Receive incident details from a client or developer.
2. Validate the request with FastAPI.
3. Normalize error code/message for consistent rule matching.
4. Run the rule-based diagnostic engine.
5. Classify the incident and generate a suggested action when a rule matches.
6. Save incident details, diagnosis, and status in SQLite.
7. Emit application logs; route them to AWS CloudWatch only when configured.
8. Return a JSON response containing incident details and the incident ID.
9. Retrieve incidents and update their status during investigation.
10. Run Pytest for API validation, diagnostic rules, persistence, and error paths.

Suggested status flow: `open → investigating → resolved`. Use only statuses supported by the actual implementation.

---
hide:
- navigation
- toc
---

# MangaDB - Authentication Endpoints <img src="https://img.shields.io/badge/Version-1.0.0-blue">

To access the other endpoints in the MangaDB API, you'll need to obtain an authentication token. There are different methods for obtaining a token depending on the context:

- For production use, API tokens are issued with a 24-hour expiration period.
- Sandbox tokens are available for testing purposes and do not expire.
- If you're using the API locally, the token is set to never expire by default, although this may not be advisable for security reasons.

The sandbox API provides two default user accounts, and while you can register your own account,
it will not have elevated privileges. The available default accounts are:

- User: **user@test.com** | **password**
- Editor: **editor@test.com** | **password**

<swagger-ui src="/Authentication/openapi.yml"/>
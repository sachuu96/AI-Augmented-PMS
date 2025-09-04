# Prompt (2025-09-05 11:00)
You are a senior API reviewer with expertise in REST, OpenAPI 3.0, and event-driven architectures.  
I am designing a scalable, event-driven product management system for an e-commerce platform.  
I already drafted the OpenAPI spec (v3.0.3) with these features:
- Products: CRUD (id, name, description, price, quantity, category).
- Auth approach: documented only, via X-Seller-Id header.
- Events: ProductCreated, ProductUpdated, ProductDeleted, LowStockWarning.
- Notifications: Server-Sent Events (SSE) endpoint.
- Optional: NDJSON import/export via Node.js streams.

Please perform a structured review of my draft `openapi.yaml` with focus on:
1. Resource design: Are the paths, naming, and request/response semantics consistent with REST best practices?
2. Error model: Is the `Problem+JSON` schema adequate and consistently applied?
3. Pagination: Is the cursor-based pagination approach correct and clear?
4. Event schemas: Are the event contracts sufficiently explicit for downstream consumers?
5. Security documentation: Is the X-Seller-Id header approach clear and properly described?
6. SSE endpoint: Is the format and use of `Last-Event-ID` clear and standards-compliant?
7. Testability & tool support: Will this spec generate usable client/server stubs with openapi-generator or Swagger Codegen?

Please suggest concrete, actionable improvements without overcomplicating the design. 
Keep scope aligned with a senior-level coding assessment (clarity, correctness, demo-ready).

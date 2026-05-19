# NestJS Request/Response Life Cycle

![[nestjs-life-cycle.png]]

**Inbound (request side):**

- **Middleware** runs first, before routing even happens — great for things like `helmet`, `cors`, request logging, or coarse-grained auth.
- **Guards** decide _authorization_ — they run after routing resolves the handler but before anything touches the data. `canActivate()` returns a boolean or throws.
- **Interceptors** wrap the entire execution — the "before" half runs here, useful for caching checks, request timing, or attaching context.
- **Pipes** validate and transform `@Body()`, `@Param()`, `@Query()` — `ValidationPipe` + class-validator DTOs live here. Bad data throws a `400` before the handler ever sees it.

**Handler:** The controller method runs, typically delegating to a service layer → repository → database.

**Outbound (response side):**

- **Interceptors (after)** can map or enrich the response — e.g. wrapping everything in `{ data: ... }`.
- **Exception filters** catch anything thrown during the whole pipeline and shape it into a proper HTTP error response.
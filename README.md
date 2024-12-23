
# Codegen_backend

API_FIRST :- 

https://www.linkedin.com/pulse/unveiling-api-first-approach-andreas-staufer-wewpf/?trackingId=B6DrDw2nRR2PQQYdHl6J%2FQ%3D%3D

https://www.linkedin.com/posts/postman-platform_api-first-the-future-of-development-is-activity-7261436455179202561-ACG0?utm_source=share&utm_medium=member_desktop

How is it done ? :-

1. Define OpenAPI Spec in SwaggerHub
2. Integrate with Github API. Once the spec is ready, click save -> new repo created in Github with the spec
3. Trigger github workflow to generate spring boot code using swagger codegen
4. swagger codegen uses moustache template which can be customised

Additional :-

1. OpenApi spec allows custom fields - we can use this to define hibernate entities and relations
2. Smartbear ( the company that owns swagger ) has taken over Stoplight ( company that owns spectral - library for linting the OpenAPI spec )
3. Linting rules can be written in github workflows - response can be given back to swaggerhub via SwaggeHub API.

Key elements:
1. GitHub API, SwaggerHub API, Spectral Library, Swagger codegen, Moustache Template

Dev Effort required in foll areas: 
1. Architect , product owner, dev leads, techno-functional spocs - Discuss and finalize standards - exception model, http status codes, number of microservices, OpenApi spec structure, Backend Tech stack, **WRITING THE OPENAPI SPEC**.
2. Developers - Moustache template customization, Spectral linting rules ( if required - for standard naming convention for schema fields , type checking )
3. Developers/Dev Lead/ Architect - SwaggerHub - GitHub integration , github workflow design + setup for automated code generation, security
4. Dev effort - Writing the service layer logic - transformations, utilities, constants

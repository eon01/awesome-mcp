# Awesome MCP

> **Practical MCP with FastMCP & LangChain: Engineering the Agentic Experience**
>
> To support this work, get your copy of my course [Practical MCP with FastMCP & LangChain](https://faun.dev/sensei/academy/practical-mcp-with-fastmcp-langchain-2ce0af-02ad51/).

This appendix is a curated, opinionated map of the MCP ecosystem: the projects, tools, and resources worth knowing after you have built and shipped your first servers.

**Note**: This is not a list of servers. It's a list of tools and resources for developers and engineers building MCP systems.

## Specification and official resources

- [Model Context Protocol specification](https://modelcontextprotocol.io) - the canonical spec, concepts, and transport definitions. Read this before trusting any third-party explainer.
- [MCP GitHub organization](https://github.com/modelcontextprotocol) - SDKs, reference servers, the inspector, the registry, and the docs, all in one place.
- [MCP blog](https://blog.modelcontextprotocol.io) - protocol release candidates, registry announcements, and governance updates. The fastest way to learn what changed.
- [MCP Inspector](https://github.com/modelcontextprotocol/inspector) - the official GUI for connecting to a server and exercising its tools, resources, and prompts by hand. Your first debugging stop.

## Learning resources

- [Official MCP documentation](https://modelcontextprotocol.io) - tutorials, concept guides, and the client and server build walkthroughs, kept current with the spec.
- [FastMCP documentation](https://gofastmcp.com) - deep, example-driven docs for the framework used throughout this book.
- [DeepWiki](https://deepwiki.com) - AI-generated, browsable documentation for MCP repositories, handy for orienting yourself in an unfamiliar codebase fast.
- [Reference servers](https://github.com/modelcontextprotocol/servers) - the official educational implementations (filesystem, fetch, memory, and more), maintained to demonstrate SDK usage and protocol features cleanly.
- [Practical MCP with FastMCP & LangChain](https://faun.dev/sensei/academy/practical-mcp-with-fastmcp-langchain-2ce0af-02ad51/) - A hands-on course for engineers done with demos: build production-grade MCP servers, clients, and middleware with FastMCP and LangChain, from first principles through human-in-the-loop flows, progress and sampling, RAG, and stateful deployment, capped by a full PostgreSQL and Redis analytics system.

## Newsletters and communities

- [AILinks](https://faun.dev/topics/ailinks): Generative AI is changing everything, and most of the coverage is noise. We cut through it - one weekly issue packed with the most relevant tools, research, and news in AI and machine learning, with a take you won't find anywhere else.

## Server frameworks and SDKs

- [FastMCP](https://github.com/jlowin/fastmcp) - the Pythonic, high-level way to build servers and clients, and the framework this book is built around. Docs at [gofastmcp.com](https://gofastmcp.com).
- [Python SDK](https://github.com/modelcontextprotocol/python-sdk) - the official low-level Python implementation. FastMCP's foundations were upstreamed here.
- [TypeScript SDK](https://github.com/modelcontextprotocol/typescript-sdk) - official, runs on Node.js, Bun, and Deno. The reference implementation for the JavaScript world.
- [Go SDK](https://github.com/modelcontextprotocol/go-sdk) - official, maintained in collaboration with Google.
- [C# SDK](https://github.com/modelcontextprotocol/csharp-sdk) - official .NET SDK, maintained with Microsoft.
- [Java SDK](https://github.com/modelcontextprotocol/java-sdk) and [Spring AI MCP](https://docs.spring.io/spring-ai/reference/api/mcp/mcp-overview.html) - official Java support, with Spring AI providing the higher-level integration.
- [mcp-framework](https://github.com/QuantGeekDev/mcp-framework) - a TypeScript framework with automatic tool discovery and multi-transport support, aiming to fill the ergonomic gap that FastMCP fills in Python.

## Gateways and proxies

- [agentgateway](https://agentgateway.dev) - a Rust data-plane gateway with native MCP and A2A support, JWT and OAuth, tool-level RBAC, and OpenTelemetry tracing. A Linux Foundation project contributed by Solo.io, with Envoy and Istio roots.
- [Microsoft MCP Gateway](https://github.com/microsoft/mcp-gateway) - a reverse proxy and control plane for session-aware routing and lifecycle management of MCP servers on Kubernetes, with Entra ID auth. Enterprise-oriented.
- [IBM ContextForge](https://github.com/IBM/mcp-context-forge) - a gateway, registry, and proxy that federates MCP, A2A, and REST or gRPC behind one endpoint, with a plugin system, virtual servers, and OpenTelemetry. Strong community traction.
- [Docker MCP Gateway](https://github.com/docker/mcp-gateway) - runs MCP servers as isolated containers with credential injection and restricted privileges by default. Ships with Docker Desktop's MCP Toolkit.
- [MCPJungle](https://github.com/mcpjungle/MCPJungle) - a self-hostable gateway and registry that centralizes many servers behind one endpoint, with tool groups, access control, and audit trails. A sensible default for small to medium teams.
- [Bifrost](https://github.com/maximhq/bifrost) - a high-performance Go AI gateway from Maxim AI that doubles as an MCP gateway, centralizing tool connections, governance, and auth. Apache 2.0.
- [Obot](https://github.com/obot-platform/obot) - an open-source MCP platform (gateway, registry, hosting, and chat client) that enforces OAuth, applies access policies, and audits every call.
- [Plano](https://github.com/katanemo/plano) - an Envoy-based, AI-native proxy and data plane for agentic apps, with orchestration, guardrails, and smart LLM routing, now fronting MCP servers too. Built by core Envoy contributors.
- [DeployStack](https://github.com/deploystackio/deploystack) - a team layer over MCP with an encrypted credential vault, RBAC, and one shared endpoint for a whole team. AGPL-3.0.
- [MCPO](https://github.com/open-webui/mcpo) - not a router but an MCP-to-OpenAPI proxy that exposes any MCP server as a REST endpoint, so non-MCP clients (Open WebUI and others) can use it. The most popular option for personal setups.
- [Lasso MCP Gateway](https://github.com/lasso-security/mcp-gateway) - a security-first, plugin-based gateway focused on tool authorization, network filtering, and content inspection against MCP-specific attack vectors.
- [awesome-mcp-gateways](https://github.com/e2b-dev/awesome-mcp-gateways) - a maintained comparison list. Start here to evaluate the full field, including commercial AI gateways such as LiteLLM, Portkey, TrueFoundry, and Composio that have added MCP support.

## Registries and discovery

- [Official MCP Registry](https://registry.modelcontextprotocol.io) - the community-driven, canonical metadata repository, backed by Anthropic, GitHub, Microsoft, and PulseMCP. In preview with an API freeze at v0.1 as of mid-2026, so expect breaking changes before general availability.
- [mcp.so](https://mcp.so) - one of the largest hosted directories, indexing tens of thousands of servers.
- [Smithery](https://smithery.ai) - a registry plus one-click hosted deployment for many servers.
- [Glama](https://glama.ai/mcp) - a directory covering both servers and clients, with quality signals.
- [awesome-mcp-servers](https://github.com/punkpeye/awesome-mcp-servers) - An awesome list of MCP servers.

## Clients and host applications

- [Claude Desktop](https://claude.ai/download) - the original reference host, and one of the few with full support for the MCP Apps interactive UI spec.
- [Cursor](https://cursor.com) - the default recommendation for professional developers, with polished visual server setup and multi-agent support.
- [Cline](https://github.com/cline/cline) - the leading open-source coding agent inside VS Code, with full model and cost control.
- [VS Code with GitHub Copilot](https://code.visualstudio.com/docs/copilot/copilot-mcp) - native MCP support in the editor most developers already use.
- [Goose](https://github.com/block/goose) - Block's open-source agent, another full MCP Apps implementer.
- [LibreChat](https://github.com/danny-avila/LibreChat) - a self-hosted, multi-user chat platform for teams that need data sovereignty and MCP at scale.

## Security and auth

- [MCP-Scan](https://github.com/invariantlabs-ai/mcp-scan) - a static scanner from Invariant Labs that inspects server configs and tool metadata for prompt injection, tool poisoning, rug-pulls, and unsafe cross-origin settings. Run it before installing anything.
- [OWASP guidance on MCP and LLM risks](https://genai.owasp.org) - the OWASP GenAI project's evolving guidance, including the tool-poisoning and agentic-attack patterns MCP inherits.
- [Agentgateway](https://github.com/agentgateway/agentgateway) - an open source proxy built on AI-native protocols (MCP & A2A) that provides drop-in security, observability, and governance for agent-to-LLM, agent-to-tool, and agent-to-agent communication across any framework and environment.

## Observability and debugging

- [MCP Inspector](https://github.com/modelcontextprotocol/inspector) - listed again because it is your first-line interactive debugger for any server.
- [Langfuse](https://langfuse.com) - open-source LLM and MCP observability. Its Python v3 and JS v4 SDKs are built on OpenTelemetry, so tool-call traces slot into existing pipelines.
- [OpenTelemetry](https://opentelemetry.io) - the vendor-neutral tracing standard. MCP propagates context through its `_meta` convention, letting you link client and server spans across the wire.

## Deployment and hosting

- [FastMCP Cloud](https://fastmcp.cloud) - the fastest path to a live URL for a Python FastMCP server, with a free personal tier. Now branded Prefect Horizon.
- [Cloudflare Workers](https://developers.cloudflare.com/agents/guides/remote-mcp-server/) - near-zero cold starts for remote TypeScript servers over Streamable HTTP, with a generous free tier.
- [Smithery](https://smithery.ai) - hosted deployment tied to its registry, useful when you want discovery and hosting in one step.

---

Help keep this list alive. If you are building a gateway, framework, or tool that belongs here, or you know one that has outgrown a project already listed, open a pull request!

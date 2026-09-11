# ZAMBO

    ### The cross-AI execution and verification layer.

    **Give the AI you already use tools, memory, and proof.**

    Zambo sits between an AI client and the work it needs to complete. It gives supported MCP clients one shared execution layer for live tools, durable continuity, explicit approvals, artifacts, and execution receipts—without replacing the model or forcing users into another chatbot.

    [Connect Zambo](https://zambo.dev/mcp) · [Explore workflows](https://zambo.dev/workflows) · [View reliability](https://zambo.dev/reliability) · [Open zambo.dev](https://zambo.dev)

    ---

    ## How it fits

    ```text
    Claude · ChatGPT · Grok · Cursor · other Streamable HTTP MCP clients
                                  │
                                  ▼
                               ZAMBO
                                  │
            tools · execution · continuity · approvals · artifacts · receipts
    ```

    Zambo is not a model provider or an AI replacement. Keep the assistant you prefer. Zambo provides the operational layer beside it, so work can continue across calls and clients with clearer state and evidence.

    ## Connect in under a minute

    **Remote MCP endpoint**

    ```text
    https://zambo.dev/api/mcp
    ```

    Minimal configuration for clients that accept remote Streamable HTTP MCP servers:

    ```json
    {
      "mcpServers": {
        "zambo": {
          "url": "https://zambo.dev/api/mcp"
        }
      }
    }
    ```

    After connecting, ask your AI to discover a capability or execute a safe task. Consequential actions may require explicit confirmation. Gateway, product, and upstream-provider limits can apply.

    ## What Zambo provides

    - **Execution:** route requests to real tools and return observed results rather than invented completion claims.
    - **Continuity:** preserve job and session context so interrupted work can be resumed deliberately.
    - **Control:** distinguish plans, previews, approval requests, executions, failures, and unavailable states.
    - **Evidence:** return structured receipts and artifacts when the underlying capability supports them.
    - **Portability:** keep the execution layer independent from the model or chat interface chosen today.
    - **Discovery:** expose 100+ capabilities through one machine-readable MCP connection; exact live counts come from MCP discovery.

    ## Public repositories

    | Repository | Purpose |
    |---|---|
    | [zambo-mcp](https://github.com/zambodotdev/zambo-mcp) | Remote MCP connection, protocol examples, and integration guidance |
    | [zambo-mcp-workflows](https://github.com/zambodotdev/zambo-mcp-workflows) | Practical execution patterns built around the Zambo connection |
    | [agent-ledger](https://github.com/zambodotdev/agent-ledger) | Lightweight tool and model-call observability |
    | [mcp-shield](https://github.com/zambodotdev/mcp-shield) | Security middleware patterns for MCP servers |
    | [prompt-shield](https://github.com/zambodotdev/prompt-shield) | Pattern-based prompt-injection screening |
    | [x402-base-verify](https://github.com/zambodotdev/x402-base-verify) | Base USDC receipt verification primitives |

    Each repository documents its own status and limitations. A public repository or package is not, by itself, a claim of universal compatibility, external-outcome verification, or complete security.

    ## Engineering principles

    1. Never report execution when only a plan or preview exists.
    2. Require explicit approval before supported consequential actions proceed.
    3. Treat retries and payment callbacks as replayable, idempotent operations.
    4. Preserve caller ownership and privacy across sessions and stored state.
    5. Return unavailable or degraded states instead of fabricated data.
    6. Keep exact capability counts machine-readable and public marketing stable at **100+**.

    ## Security

    Do not put secrets in prompts, MCP configuration files, issues, or examples. Use environment variables and the authentication mechanism documented by the capability you call. Report security concerns privately through the guidance in the relevant repository.

    ---

    Zambo is built to help AI move from answering to completing work—with continuity, control, and evidence.
    
# Claude Desktop MCP Server Configuration

This repository contains the configuration and setup scripts for Claude Desktop MCP servers. It provides a standardized way to set up the required Model Context Protocol servers locally.

## Prerequisites

- Node.js (v14 or higher)
- npm (v6 or higher)
- Python 3.8+ (for certain MCP servers)
- curl (for health checks)

## Included MCP Servers

1. Filesystem Server (`@modelcontextprotocol/server-filesystem`)
2. RAG Web Browser (`@modelcontextprotocol/server-rag-web-browser`)
3. Memory Server (`@modelcontextprotocol/server-memory`)
4. Sequential Thinking (`@modelcontextprotocol/server-sequential-thinking`)
5. Puppeteer Server (`@modelcontextprotocol/server-puppeteer`)

## Quick Start

1. Clone this repository:
```bash
git clone https://github.com/jhillbht/Local-File.git
cd Local-File
```

2. Copy the environment configuration:
```bash
cp .env.example .env
```

3. Run the installation script:
```bash
chmod +x scripts/install-mcp-servers.sh
./scripts/install-mcp-servers.sh
```

## Configuration

The configuration files are located in the `config/` directory:

- `claude_desktop_config.json`: Main configuration file
- `.env`: Environment-specific settings (create from .env.example)

## Directory Structure

```
.
├── scripts/
│   ├── install-mcp-servers.sh
│   ├── setup_mcp_server.sh
│   └── health_check.sh
├── config/
│   └── claude_desktop_config.json
├── .env.example
└── README.md
```

## Health Checks

To verify the servers are running correctly:
```bash
./scripts/health_check.sh
```

## Troubleshooting

1. If servers fail to start:
   - Check if ports 8000-8004 are available
   - Ensure all prerequisites are installed
   - Check the logs in `logs/` directory

2. If you see permission errors:
   - Ensure scripts are executable (`chmod +x scripts/*.sh`)
   - Check file ownership and permissions

## Contributing

1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## License

MIT License - See LICENSE file for details
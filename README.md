# Federation Protocols

MCP and A2A protocol implementation for Mission 12 Conversational AI.

## Overview

This project implements the Federation Protocols that enable agents to communicate with ship sensors (vertical integration via MCP) and external agents (horizontal integration via A2A). The protocols ensure the Starship Dialectic's agents can interface with reality through standardized communication channels.

## Files

- `mcp_snippet.py` - MCP server specification providing sensor access tools
- `agent.json` - A2A agent card declaring the Strategist's capabilities
- `requirements.txt` - Required dependencies


## Installation

Install the required dependencies:

```bash
pip install mcp
```

## Usage

### Running the MCP Server

Start the MCP server to provide sensor access:

```bash
python mcp_snippet.py
```

The server exposes three sensor tools:
1. `read_gravitational_waves(frequency)` - Detect spacetime distortions
2. `read_thermal_signature(wavelength_nm)` - Analyze thermal emissions
3. `read_radio_broadcast(frequency_mhz)` - Monitor for structured signals

### Using in Your Agent

```python
from mcp_snippet import mcp

# The server provides tools that can be called by agents
# Tools return JSON-formatted sensor data
```

### A2A Agent Card

The `agent.json` file declares the Strategist agent's identity for agent-to-agent communication. Deploy this file to your agent discovery endpoint to enable external agents to discover and interact with the Strategist.

## How It Works

### Vertical Integration (MCP)
1. **Physical Sensors**: Ship's gravitational, thermal, and radio sensors
2. **MCP Tools**: Standardized tool interface for sensor access
3. **Scanner Agent**: Calls tools to gather intelligence

### Horizontal Integration (A2A)
1. **Agent Card**: Declares capabilities and interaction protocols
2. **Security Scopes**: Three-tier access (public, authenticated, restricted)
3. **Opaque Principle**: External agents know WHAT, not HOW

## Security Scopes

- **Public**: Star charts, anomaly classification, safe passage negotiation
- **Authenticated**: Joint operations, threat intelligence, emergency assistance
- **Restricted**: NO ACCESS to shield frequencies, weapons, crew data, internal logs

## Protocol Compliance

- **MCP**: Model Context Protocol for vertical integration
- **A2A**: Agent-to-Agent protocol for horizontal federation
- **Opaque Principle**: Capabilities are public, internal reasoning remains hidden

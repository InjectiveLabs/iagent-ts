# iAgent with Eliza Quick Start Guide

## Overview
iAgent leverages Eliza as its powerful multi-agent framework, providing advanced capabilities for agent development and deployment on the Injective Chain.

## Character Configuration

### Editing Default Character
1. Open `src/character.ts` to modify the default character
2. Uncomment and edit the existing character configuration

### Loading Custom Characters
Load custom characters in iAgent using the command:
```bash
pnpm start --characters="path/to/your/character.json"
```
Note: Multiple character files can be loaded simultaneously.

## Client Configuration
You can specify clients in two ways:

### In character.ts:
```typescript
clients: [Clients.TWITTER, Clients.DISCORD],
plugins: [injectivePlugin]
```

### In character.json:
```json
{
  "clients": ["twitter", "discord"]
}
```

## Environment Setup

### Setting Up Environment Variables
1. Duplicate the environment template:
```bash
cp .env.example .env
```

2. Add your credentials to `.env`:
```plaintext
# Injective Keys and Environment
INJECTIVE_PUBIC_KEY="XXXX"
INJECTIVE_PRIVATE_KEY="XXXX"
EVM_PUBLIC_KEY="XXXX"
INJECTIVE_NETWORK="Mainnet"

# Discord Credentials
DISCORD_APPLICATION_ID="discord-application-id"
DISCORD_API_TOKEN="discord-api-token"

# Twitter Credentials
TWITTER_USERNAME="username"
TWITTER_PASSWORD="password"
TWITTER_EMAIL="your@email.com"
```

## Installation and Startup

### Standard Installation
1. Install dependencies and start iAgent with Juliette (powered by Eliza):
```bash
pnpm clean && pnpm i && pnpm build && pnpm start
```
Note: Requires Node.js version 23 or higher

2. To interact with default characters in a different terminal:
```bash
pnpm start:client
```
Then navigate to `localhost:5173`

## Next Steps
Explore Eliza's capabilities within the iAgent framework. Refer to the documentation for advanced features and customization options.
# iAgent with Eliza Quick Start Guide

## Overview

The iAgent SDK is a comprehensive framework for building applications on the Injective Chain, offering:

### Rich Module Support
- Full coverage of Injective modules (Exchange, Staking, Governance, Bank)
- Pre-built actions for trading, staking, and governance

### Action Framework
- Template-based system with built-in validation
- Standardized patterns for queries and transactions
- Automated error handling

### Integration Features
- Native gRPC client integration
- Multi-network support (Mainnet/Testnet)
- Streamlined key management

### Developer Tools
- TypeScript definitions
- Example implementations
- Modular action creation system

This SDK enables rapid development of secure, reliable applications within Injective's DeFi ecosystem.

## Quick Start Guide

**Note:** Requires Node.js version 23 or higher

### Initial Setup

1. Clone the repository:
```bash
git clone https://github.com/InjectiveLabs/iagent-ts
```

2. Install dependencies and build:
```bash
cd iagent-ts
pnpm i --no-frozen-lockfile && pnpm build
```

### Environment Configuration

1. Create your environment file:
```bash
cp .env.example .env
```

2. Configure your `.env` file:
```plaintext
# Injective Keys and Environment
INJECTIVE_PUBIC_KEY="XXXX"
INJECTIVE_PRIVATE_KEY="XXXX"
EVM_PUBLIC_KEY="XXXX"
INJECTIVE_NETWORK="Mainnet"
OPENAI_API_KEY="sks-x"
# Other application environment variables go here
```

**Note:** Get your OpenAI API key from: https://platform.openai.com/api-keys

### Running the Application

1. Start the agent server:
```bash
pnpm start
```

2. In a separate terminal, start the client:
```bash
pnpm start:client
```

## Advanced Configuration

### Character Configuration

#### Default Character
To modify the default character, edit `src/character.ts`

#### Custom Characters
Load custom character configurations:
```bash
pnpm start --characters="path/to/your/character.json"
```
**Note:** Multiple character files can be loaded simultaneously

### Client Configuration

You can configure clients in two ways:

1. In `character.ts`:
```typescript
clients: [Clients.TWITTER, Clients.DISCORD],
plugins: [injectivePlugin]
```

2. In `character.json`:
```json
{
  "clients": ["twitter", "discord"]
}
```

## Development Best Practices

1. Always use TypeScript for type safety
2. Follow the template patterns for new actions
3. Implement proper error handling
4. Test on testnet before deploying to mainnet

## Common Issues and Solutions

1. **Connection Issues**
   - Verify network configuration
   - Check API key validity
   - Ensure proper endpoint URLs

2. **Transaction Failures**
   - Verify account balance
   - Check gas settings
   - Validate transaction parameters

## Next Steps

1. Explore the example implementations
2. Review the API documentation
3. Join the developer community
4. Build your first application

For more detailed information, refer to:
- Official Documentation
- API Reference
- Community Forums
- Developer Discord

## Contributing

We welcome contributions! Please:
1. Fork the repository
2. Create a feature branch
3. Submit a pull request
4. Follow the code style guidelines

## Support

For support:
- GitHub Issues
- Developer Discord
- Community Forums
- Documentation Wiki
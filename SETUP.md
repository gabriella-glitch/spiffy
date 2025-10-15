# Spiffy Discord Bot - Setup Guide

This repository contains n8n workflows for the Spiffy Discord bot. The actual workflow files with credentials are excluded from version control for security.

## Important: n8n Compatibility
The workflows in `workflows-sanitized/` are **fully n8n compatible** and can be imported directly into n8n. The `/lib` folder contains reference code for understanding the logic but is NOT used by n8n.

## Setup Instructions

1. **Copy environment template**
   ```bash
   cp .env.example .env
   ```

2. **Fill in your credentials in `.env`**
   - Discord Guild ID and Channel IDs
   - Webhook IDs
   - n8n Instance and Workflow IDs
   - API Credential IDs

3. **Import workflows into n8n**
   - Open your n8n instance
   - Go to Workflows → Import from File
   - Select each JSON file from `workflows-sanitized/`
   - Replace placeholder values (e.g., `{{DISCORD_GUILD_ID}}`) with actual values
   - Or use n8n's credential system to manage sensitive data

4. **Configure n8n**
   - Import the workflows into your n8n instance
   - Set up Discord Bot credentials
   - Configure Ollama API connection
   - Test each workflow individually

## Workflow Descriptions

- **Check-in Workflow**: Automated hourly messages with scheduling and quiet hours
- **Daily Digest Workflow**: Daily summaries with weather information
- **Discord Chat Workflow**: Interactive chat bot responses

## Security Notes

- Never commit `.env` or the `workflows/` folder with real credentials
- Use the sanitized versions in `workflows-sanitized/` for version control
- Rotate credentials regularly
- Use environment variables or n8n's credential management system
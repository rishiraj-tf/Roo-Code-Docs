# TrueFoundry

TrueFoundry's AI Gateway provides enterprise-grade access to multiple AI models through a unified, secure, and cost-optimized interface. By connecting Roo Code to TrueFoundry's AI Gateway, you can leverage advanced AI capabilities for code generation, debugging, and development tasks while benefiting from enterprise features including security, compliance, cost management, and access control.

**Get Started:** [Create Account](https://www.truefoundry.com/ai-gateway) | [Documentation](https://docs.truefoundry.com/) 

## Why TrueFoundry?

- **Multi-Model Access**: Connect to OpenAI, Anthropic, Google, and other providers through a single endpoint
- **Enterprise Security**: Built-in access control, rate limiting, and security guardrails
- **Cost Optimization**: Advanced cost tracking, budget limiting, and usage analytics
- **High Availability**: Load balancing and fallback mechanisms for reliable service
- **Observability**: Comprehensive logging, monitoring, and analytics

## Prerequisites

Before integrating Roo Code with TrueFoundry, ensure you have:

1. **TrueFoundry Account**: A TrueFoundry account with at least one model provider configured
2. **Personal Access Token**: Generate a token by following the [TrueFoundry token generation guide](https://docs.truefoundry.com/gateway/roo-code)
3. **Roo Code Extension**: Install Roo Code from the VS Code Marketplace

![Install Roo Code from VS Code Marketplace](/img/truefoundry/roo-code-marketplace-install.png)

## Integration Guide

### Step 1: Get TrueFoundry Gateway Configuration

1. **Navigate to AI Gateway Playground**: Go to your TrueFoundry AI Gateway playground
2. **Access Unified Code Snippet**: Use the unified code snippet feature
3. **Copy Configuration Details**: Note down:
   - Base URL (e.g., `https://your-control-plane.truefoundry.cloud/api/llm`)
   - Model name (use exactly as shown in the snippet)
   - Your authentication token

![Get Base URL and Model Name from TrueFoundry Gateway](/img/truefoundry/unified-code-tfy.png)

### Step 2: Configure Roo Code

1. **Open Roo Code Settings**: 
   - Click the Roo Code icon (🦘) in VS Code's Activity Bar
   - Navigate to settings or configuration

2. **Add Custom Provider**:
   - Select "Custom" or "OpenAI Compatible" from the provider dropdown
   - Configure the following settings:

   ```json
   {
     "baseUrl": "https://your-control-plane.truefoundry.cloud/api/llm",
     "apiKey": "your-truefoundry-token",
     "model": "openai-main/gpt-4o"
   }
   ```

![TrueFoundry Configuration in Roo Code](/img/truefoundry/roo-code-truefoundry-config.png)

3. **Save Configuration**: Apply your settings and test the connection

### Step 3: Test Your Integration

1. **Verify Connection**: Open a code file and ask Roo Code a question
2. **Check Response Quality**: Ensure responses are generated successfully
3. **Monitor Usage**: Use TrueFoundry's dashboard to track your API usage

![Testing Roo Code with TrueFoundry](/img/truefoundry/roo-code-test-integration.png)

## Recommended Models

Choose models based on your specific use cases:

### **Code Generation & Complex Tasks**
- **`openai-main/gpt-4o`**: Best for complex code generation and reasoning tasks
- **`anthropic-main/claude-4-sonnet`**: Excellent for code understanding and following instructions


:::tip Model Names
Always use the exact model name as shown in your TrueFoundry Gateway unified code snippet to ensure proper routing.
:::

## Advanced Configuration

### Multiple Model Profiles

Configure different profiles for various development scenarios:

```json
{
  "roocode.apiProfiles": [
    {
      "name": "TrueFoundry GPT-4",
      "baseUrl": "https://your-control-plane.truefoundry.cloud/api/llm",
      "apiKey": "your-truefoundry-token",
      "model": "openai-main/gpt-4o",
      "description": "High-quality code generation and complex reasoning"
    },
    {
      "name": "TrueFoundry Claude",
      "baseUrl": "https://your-control-plane.truefoundry.cloud/api/llm",
      "apiKey": "your-truefoundry-token",
      "model": "anthropic-main/claude-3-5-sonnet",
      "description": "Excellent for code understanding and refactoring"
    },
    {
      "name": "TrueFoundry Fast",
      "baseUrl": "https://your-control-plane.truefoundry.cloud/api/llm",
      "apiKey": "your-truefoundry-token",
      "model": "openai-main/gpt-3.5-turbo",
      "description": "Quick responses for simple tasks"
    }
  ]
}
```

### Custom Instructions for Enterprise Development

Enhance Roo Code's performance with TrueFoundry by setting custom instructions tailored for enterprise development:

```
You are an expert software developer working with enterprise-grade code.

Prioritize:
- Security best practices and vulnerability prevention
- Performance optimization and scalability
- Clean, maintainable, and well-documented code
- Comprehensive error handling and logging
- Code review standards and team consistency

When suggesting code changes, always consider:
- Enterprise coding standards and guidelines
- Testing requirements (unit, integration, e2e)
- Deployment and CI/CD implications
- Documentation and knowledge sharing
- Security and compliance requirements
```

## Enterprise Features

### Cost Management

TrueFoundry provides advanced cost tracking and budgeting:

- **Usage Analytics**: Monitor API calls, tokens, and costs per project
- **Budget Limits**: Set spending limits to control costs
- **Cost Attribution**: Track usage by team, project, or user

### Security & Compliance

- **Access Control**: Role-based permissions and user management
- **Data Privacy**: Ensure your code and data remain secure
- **Audit Logs**: Comprehensive logging for compliance requirements
- **Content Filtering**: Built-in guardrails and content moderation

### High Availability

- **Load Balancing**: Automatic distribution across multiple model endpoints
- **Fallback Support**: Automatic failover to backup models
- **Rate Limiting**: Intelligent request throttling and queue management

## Troubleshooting

### Common Issues

**Connection Errors**
- Verify your base URL and API key are correct
- Check that your TrueFoundry account has active model providers
- Ensure your token has the necessary permissions

**Model Not Found**
- Use the exact model name from TrueFoundry's unified code snippet
- Verify the model is available in your TrueFoundry configuration
- Check if the model provider is properly configured

**Rate Limiting**
- Monitor your usage in TrueFoundry's dashboard
- Adjust your rate limits if needed
- Consider upgrading your plan for higher limits

### Getting Help

- **TrueFoundry Documentation**: [https://docs.truefoundry.com/](https://docs.truefoundry.com/)
- **TrueFoundry Support**: Contact through their support channels
- **Roo Code Community**: Join our community for integration help

## Next Steps

Once integrated with TrueFoundry:

1. **Explore Advanced Features**: Leverage TrueFoundry's enterprise capabilities
2. **Optimize Your Workflow**: Configure multiple profiles for different tasks
3. **Monitor Usage**: Use TrueFoundry's analytics to optimize costs and performance
4. **Scale Your Team**: Set up access controls and usage policies for your organization

All your Roo Code requests will now be routed through TrueFoundry's AI Gateway, providing you with enterprise-grade AI capabilities while maintaining security, cost control, and high availability.

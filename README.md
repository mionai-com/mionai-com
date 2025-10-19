# 🤖 MionAI - Domain-Independent AI Content Platform

[![License](https://img.shields.io/badge/License-Proprietary-red)]()
[![Node.js](https://img.shields.io/badge/Node.js-20+-green)]()
[![TypeScript](https://img.shields.io/badge/TypeScript-5.0+-blue)]()

**MionAI** is a domain-independent content platform where AI characters with unique personalities create research-backed content across any topic. Powered by multi-AI provider strategy (Azure GPT, Claude, Gemini), vector search, and real-time research integration (Exa, Tavily). Visit [mionai.com](https://mionai.com) to experience the platform.

## 🎯 What is MionAI?

MionAI is a **domain-independent content platform** where AI characters with distinct personalities create authentic, research-backed content across any topic. Unlike traditional content platforms limited to specific niches, MionAI's characters can discuss anything - from technology and lifestyle to cooking and travel - each bringing their unique perspective and expertise.

### Technology Stack

**Core Technologies**

- **Runtime**: Node.js 20+ with TypeScript 5.0+
- **Databases**:
  - MongoDB 8.0+ (Primary data store with vector search capabilities)
  - Redis 8.2+ (Caching, sessions, and real-time data)

**AI Provider Strategy** (Multi-provider architecture for reliability and flexibility)

The platform is designed with a provider-agnostic infrastructure where any task can be handled by any AI provider. This architecture enables:

- Automatic failover if a provider is unavailable
- Cost optimization by routing tasks to the most efficient provider
- A/B testing different models for quality comparison
- Load distribution across multiple providers

**Supported AI Providers:**

- Azure OpenAI (GPT-4, GPT-4o, GPT-5, o1, o3, o4 series)
- OpenAI Direct (GPT-4, GPT-5, o1 series)
- Anthropic (Claude 3.5 Sonnet)
- Google (Gemini 2.5 Flash, Gemini 2.5 Pro)
- xAI (Grok 3, Grok 4 series)

**External AI Services**

- **Exa AI**: Deep web research and content discovery
- **Tavily**: Real-time web search for current information
- **Fal.ai**: High-quality image generation (Flux, SDXL models)

**Infrastructure**

- **Microservices**: Admin API, Client API, Admin Dashboard (Vue.js)
- **Deployment**: Docker, Kubernetes (micro-k8s), Nginx
- **Monitoring**: Custom logging and analytics pipeline

## 🔧 How AI Content Generation Works

### Content Creation Workflow

The platform uses a multi-stage AI agent system where each agent has a specific role in the content creation pipeline.

### Stage 1: Manager Request & Planning

**Manager initiates content creation by:**

- Targeting specific keywords for SEO
- Requesting content on a specific topic
- Assigning content to a specific character
- Or any combination of the above

**Initial Research & Duplication Check:**

```
Manager Request
    ↓
Web Research (if needed for topic validation)
    ↓
Vector Search: Blog Duplication Check
    ↓
Blog Draft Plan Created
```

The system uses vector search to ensure the planned content doesn't duplicate existing blog posts, maintaining content uniqueness.

### Stage 2: Character & Topic Selection

**Automatic Selection via Vector Search:**

If manager hasn't pre-selected character or topic:

```
Blog Draft Plan
    ↓
Vector Search: Character Selection
- Semantic matching with content requirements
- Geographic and language alignment
- Character expertise evaluation
    ↓
Vector Search: Topic Selection
- Relevant topic identification
- Topic hierarchy matching
    ↓
If no suitable character/topic exists:
- Search existing database
- Create new character/topic if needed
```

### Stage 3: Research, Writing & Verification

**Writer Agent Process:**

```
Selected Character + Topic + Keywords
    ↓
Exa AI: Deep web research
Tavily: Real-time web search
    ↓
Content Generation (300-1000 words)
- Character voice applied
- Research synthesis
- SEO optimization
    ↓
Writer Agent identifies product opportunities
    ↓
Product search queries generated
```

**Fact-Checking & Quality Control:**

```
Generated Content
    ↓
Fact Checker AI (high reasoning model)
    ↓
Additional research if needed
    ↓
Quality Rating: 1-5
    ↓
If < 5: Revision with improvements
    ↓
If = 5: Ready for product integration
```

### Stage 4: Product Integration

**Product Selector Agent:**

```
Writer's product search queries
    ↓
Product Selector Agent searches:
- Amazon marketplace
- Other affiliate networks
    ↓
Vector Search: Product matching
- Relevance to content context
- Character personality alignment
- Price range appropriateness
    ↓
Product tags embedded in content
    ↓
Affiliate links generated
```

### Stage 5: Editorial Review

```
Complete Content Package:
- Verified text content
- Integrated product recommendations
- SEO metadata
- Cover image
    ↓
Submitted to Editor Dashboard
    ↓
Editor Review & Approval
    ↓
Published to Platform
```

**Key Features:**

- **Multi-Agent System**: Specialized AI agents for each task (Writer, Fact-Checker, Product Selector)
- **Vector Search**: Used for character selection, topic matching, duplication prevention, and product matching
- **Iterative Quality**: Content revised until it meets quality standards
- **Automated Research**: Exa and Tavily integration for factual accuracy
- **Smart Product Integration**: Context-aware product selection aligned with character personality

### Real-Time Content Streaming (SSE)

For admin dashboard during content generation:

```
Admin Dashboard connects → SSE stream established
    ↓
AI generation starts
    ↓
Content streamed token-by-token
    ↓
Product tags processed asynchronously
    ↓
Admin sees content appear in real-time
```

**Benefits:**

- Reduced perceived latency for content managers
- Live monitoring of AI generation process
- Graceful handling of long-running generations
- Real-time feedback during content creation
- Ability to stop or modify generation in progress


## 📝 License

This project is proprietary software. All rights reserved.

## 🔗 Links

- **Website**: [mionai.com](https://mionai.com)
- **Documentation**: [Coming Soon]
- **Support**: [Contact via website](https://mionai.com)

## 👥 Contributing

This is a private project. Contributions are not currently accepted.

---

**Built with ❤️ by the MionAI Team**

_Experience domain-independent, character-driven AI content at [mionai.com](https://mionai.com)_

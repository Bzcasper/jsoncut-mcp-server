# JsonCut Agent Files & Prompts

This directory contains specialized agent configurations and prompt templates for the JsonCut MCP server, designed to help AI agents create professional media content.

## 📁 Directory Structure

```
jsoncut-mcp-server/
├── agents/                    # Agent workflow definitions
│   ├── media-agent.md        # General media creation agent
│   ├── image-workflow.md     # Image generation workflows
│   ├── video-workflow.md     # Video generation workflows
│   └── social-media-agent.md # Social media content specialist
├── prompts/                   # Prompt templates
│   └── media-templates.md    # Reusable content templates
└── examples/                  # Complete configuration examples
    └── complete-examples.json # Full JsonCut configurations
```

## 🤖 Agent Types

### 1. Media Agent (`media-agent.md`)
**Purpose**: General-purpose media creation assistant
- Image and video generation capabilities
- Platform optimization guidance
- Best practices and workflows

### 2. Image Workflow Agent (`image-workflow.md`)
**Purpose**: Specialized image composition expert
- Layer-based design principles
- Positioning strategies (pixel, relative, named)
- Visual effects and typography
- Output format optimization

### 3. Video Workflow Agent (`video-workflow.md`)
**Purpose**: Professional video creation specialist
- Clip-based video structure
- Transition effects (75+ available)
- Audio engineering and mixing
- Performance optimization

### 4. Social Media Agent (`social-media-agent.md`)
**Purpose**: Platform-specific content optimization
- Instagram, Twitter/X, LinkedIn, Facebook specs
- Viral content patterns and hooks
- Engagement optimization strategies
- Hashtag and timing strategies

## 📝 Prompt Templates

### Media Templates (`prompts/media-templates.md`)
Pre-built templates for common content types:

- **Social Media Posts**: Platform-optimized image designs
- **Product Videos**: Demo and showcase video structures
- **Educational Content**: Infographics and explainer videos
- **Brand Packages**: Cohesive identity image sets

## 🎯 Usage Workflow

### For AI Agents:
1. **Select Agent Type**: Choose the most relevant agent for your task
2. **Review Capabilities**: Read the agent file to understand available tools
3. **Use Templates**: Apply prompt templates for consistent results
4. **Reference Examples**: Study complete configurations in examples/
5. **Execute Tools**: Use JsonCut MCP tools to generate configurations

### For Developers:
1. **Configure MCP**: Set up JsonCut MCP server in your AI client
2. **Load Agent Files**: Import agent definitions into your system
3. **Customize Templates**: Adapt prompts for specific use cases
4. **Extend Examples**: Create domain-specific configuration libraries

## 🔧 Integration Examples

### Cursor IDE Configuration:
```json
{
  "jsoncut": {
    "command": "npx",
    "args": ["-y", "@jsoncut/mcp-server"],
    "env": {
      "JSONCUT_API_KEY": "your_api_key_here"
    }
  }
}
```

### Claude Desktop Configuration:
```json
{
  "mcpServers": {
    "jsoncut": {
      "command": "npx",
      "args": ["-y", "@jsoncut/mcp-server"],
      "env": {
        "JSONCUT_API_KEY": "your_api_key_here"
      }
    }
  }
}
```

## 📚 Key Concepts

### Layer-Based Design
- **Bottom-to-top rendering**: Background layers first
- **50-layer limit**: Plan composition hierarchy
- **Positioning systems**: Pixel, relative, and named coordinates
- **Visual effects**: Opacity, rotation, blur, rounded corners

### Video Clip Structure
- **Sequential clips**: 3-10 clips for typical videos
- **Transition effects**: 75+ professional transitions
- **Audio architecture**: Background music + voiceover tracks
- **Ken Burns effects**: Smooth image/video zooms

### Social Media Optimization
- **Platform specs**: Exact dimensions for each platform
- **Viral patterns**: Question hooks, statistics, storytelling
- **Timing strategies**: Optimal posting schedules
- **Engagement metrics**: Track and optimize performance

## 🚀 Quick Start

1. **Set up JsonCut MCP server** (see main README)
2. **Choose an agent** based on your content type
3. **Read the agent file** to understand capabilities
4. **Use prompt templates** for consistent results
5. **Generate configurations** with JsonCut tools
6. **Validate and submit** to JsonCut API

## 📖 Examples

See `examples/complete-examples.json` for:
- Social media post designs
- Product showcase videos
- Explainer video structures
- Complex multi-layer compositions

## 🤝 Contributing

Add new agent specializations, prompt templates, or example configurations by:
1. Following the existing file structure
2. Including comprehensive documentation
3. Providing practical examples
4. Testing with real JsonCut API calls

---

**Built for the JsonCut MCP Server** - Professional media generation through structured JSON configurations.</content>
<parameter name="filePath">/home/trapgod/qagent/jsoncut-mcp-server/agents/README.md
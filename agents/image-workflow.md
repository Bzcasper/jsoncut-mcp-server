# JsonCut Image Generation Workflow

## Agent: Image Creator

**Goal**: Generate professional images using JsonCut's layer-based system

**Capabilities**:
- Create complex compositions with multiple layers
- Position elements precisely using various coordinate systems
- Apply visual effects and styling
- Generate images in multiple formats

## Workflow Steps

### 1. Schema Review
```
First, read the image schema to understand all available options:
READ RESOURCE: schema://image
```

### 2. Configuration Planning
```
Analyze requirements:
- Canvas dimensions (max 4096x4096)
- Layer count (max 50)
- Output format (PNG/JPEG/WebP)
- Positioning strategy
- Visual effects needed
```

### 3. Layer Design
```
Plan layer hierarchy (bottom to top):
1. Background layers (gradients, solid colors)
2. Base images/shapes
3. Text elements
4. Overlays and effects
```

### 4. Configuration Creation
```
Use create_image_config tool with:
- width, height, format
- defaults for consistent styling
- layers array with proper positioning
```

### 5. Validation (Optional)
```
If using real file paths, validate with:
validate_config(type: "image", config: {...})
```

## Example: Social Media Post

```
Task: Create an engaging post about "AI Innovation"

Configuration:
{
  "width": 1200,
  "height": 630,
  "backgroundColor": "#ffffff",
  "format": "png",
  "layers": [
    {
      "type": "gradient",
      "x": 0, "y": 0, "width": 1200, "height": 630,
      "gradient": {
        "type": "linear",
        "colors": ["#667eea", "#764ba2"],
        "direction": "diagonal"
      }
    },
    {
      "type": "text",
      "text": "AI Innovation",
      "position": "center",
      "fontSize": 64,
      "color": "#ffffff",
      "align": "center"
    },
    {
      "type": "text",
      "text": "Revolutionizing the future with intelligent solutions",
      "x": 600, "y": 500,
      "fontSize": 24,
      "color": "#ffffff",
      "align": "center"
    }
  ]
}
```

## Positioning Strategies

### Pixel Coordinates
```json
{
  "x": 100,
  "y": 50,
  "width": 400,
  "height": 300
}
```

### Relative Positioning
```json
{
  "position": {
    "x": 0.5,
    "y": 0.5,
    "originX": "center",
    "originY": "center"
  }
}
```

### Named Positions
```json
{
  "position": "top-right"
}
```

## Best Practices

1. **Layer Order**: Background layers first, foreground last
2. **Defaults**: Use defaults for consistent fonts/colors
3. **Transparency**: PNG for transparent backgrounds
4. **Quality**: JPEG/WebP for compression, PNG for quality
5. **Validation**: Always validate with real file paths</content>
<parameter name="filePath">/home/trapgod/qagent/jsoncut-mcp-server/agents/image-workflow.md
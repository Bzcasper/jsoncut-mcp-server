# JsonCut Media Generation Agent

## Overview
This agent specializes in creating professional media content using JsonCut's advanced layer-based generation system. It can create both static images and dynamic videos with complex compositions, animations, and effects.

## Capabilities

### Image Generation
- **Layer-based composition**: Up to 50 layers with precise positioning
- **Multiple layer types**: Images, text, shapes, gradients
- **Advanced positioning**: Pixel coordinates, relative positioning, origin-based placement
- **Visual effects**: Opacity, rotation, blur, rounded corners
- **Typography**: Custom fonts, text wrapping, alignment, backgrounds
- **Output formats**: PNG (transparent), JPEG (compressed), WebP (modern)

### Video Generation
- **Clip-based structure**: Sequential video segments with transitions
- **Rich layer types**: Video, images, titles, subtitles, audio, effects
- **Animation styles**: Fade-in, word-by-word, letter-by-letter text animations
- **Audio system**: Background music, multiple tracks, normalization
- **75+ transitions**: Fade, wipe, circle, cube, glitch, zoom effects
- **Ken Burns effects**: Smooth zoom and pan on images/video

## Agent Configuration

### For Cursor IDE
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

### For Claude Desktop
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

## Workflow

1. **Get Schema**: Always read `schema://image` or `schema://video` first
2. **Create Configuration**: Use `create_image_config` or `create_video_config`
3. **Validate** (optional): Use `validate_config` for real file paths
4. **Submit**: Send configuration to JsonCut API

## Best Practices

### Image Creation
- Use layer-based approach for complex compositions
- Leverage defaults for consistent styling
- Position strategically (bottom layers first)
- Use appropriate fit modes for images
- Consider transparency and output format

### Video Creation
- Structure content in logical clips
- Use transitions between clips
- Layer audio strategically
- Optimize for target platform specs
- Test with fast mode first

### File Paths
Use placeholder paths for development:
```
/image/YYYY-MM-DD/userXXX/filename.ext
/video/YYYY-MM-DD/userXXX/filename.ext
/audio/YYYY-MM-DD/userXXX/filename.ext
/font/YYYY-MM-DD/userXXX/filename.ext
```</content>
<parameter name="filePath">/home/trapgod/qagent/jsoncut-mcp-server/agents/media-agent.md
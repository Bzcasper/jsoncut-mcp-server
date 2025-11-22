# JsonCut Video Generation Workflow

## Agent: Video Creator

**Goal**: Generate professional videos using JsonCut's clip-based system

**Capabilities**:
- Create multi-clip videos with smooth transitions
- Layer video, images, text, and audio
- Apply animations and effects
- Professional audio mixing

## Workflow Steps

### 1. Schema Review
```
First, read the video schema to understand all available options:
READ RESOURCE: schema://video
```

### 2. Storyboard Planning
```
Plan video structure:
- Total duration and pacing
- Clip breakdown (3-10 clips typical)
- Transition strategy
- Audio requirements
- Text timing and animation
```

### 3. Clip Design
```
Design each clip:
- Duration (2-5 seconds typical)
- Layer composition
- Transition to next clip
- Audio elements
```

### 4. Audio Planning
```
Audio architecture:
- Background music (looped)
- Voiceover tracks
- Sound effects
- Volume mixing
- Normalization settings
```

### 5. Configuration Creation
```
Use create_video_config tool with:
- width, height, fps, format
- clips array with layers and transitions
- audio configuration
- defaults for consistency
```

### 6. Validation (Optional)
```
If using real file paths, validate with:
validate_config(type: "video", config: {...})
```

## Example: Product Demo Video

```
Task: Create a 30-second product demonstration

Configuration:
{
  "width": 1920,
  "height": 1080,
  "fps": 30,
  "format": "mp4",
  "audioFilePath": "/audio/user123/upbeat-background.mp3",
  "loopAudio": true,
  "outputVolume": 0.7,
  "clips": [
    {
      "duration": 5,
      "layers": [
        {
          "type": "title-background",
          "text": "Introducing ProductX",
          "style": "fade-in",
          "textColor": "#ffffff",
          "fontSize": 72,
          "position": "center",
          "background": {
            "type": "linear-gradient",
            "colors": ["#667eea", "#764ba2"],
            "direction": "diagonal"
          }
        }
      ],
      "transition": {
        "name": "fade",
        "duration": 1
      }
    },
    {
      "duration": 8,
      "layers": [
        {
          "type": "video",
          "path": "/video/user123/product-demo.mp4",
          "resizeMode": "cover",
          "cutFrom": 0,
          "cutTo": 8,
          "zoomDirection": "in",
          "zoomAmount": 0.1
        },
        {
          "type": "subtitle",
          "text": "See it in action",
          "fontSize": 36,
          "textColor": "#ffffff",
          "position": "bottom"
        }
      ],
      "transition": {
        "name": "circleopen",
        "duration": 1.2
      }
    },
    {
      "duration": 5,
      "layers": [
        {
          "type": "fill-color",
          "color": "#2c3e50"
        },
        {
          "type": "title",
          "text": "Available Now",
          "style": "word-by-word",
          "fontSize": 64,
          "textColor": "#ffffff",
          "position": "center"
        }
      ]
    }
  ]
}
```

## Clip Structure Best Practices

### Opening Clip (3-5 seconds)
- Strong hook with title-background layer
- Brand colors and typography
- Smooth transition out

### Content Clips (5-10 seconds each)
- One main visual element per clip
- Supporting text/subtitle layers
- Ken Burns effects on static images
- Logical flow between clips

### Closing Clip (3-5 seconds)
- Call-to-action or summary
- Contact information
- Brand reinforcement

## Audio Engineering

### Background Music
```json
{
  "audioFilePath": "/audio/user123/background.mp3",
  "loopAudio": true,
  "outputVolume": 0.7
}
```

### Voiceover Tracks
```json
{
  "audioTracks": [
    {
      "path": "/audio/user123/voiceover.wav",
      "mixVolume": 0.9,
      "start": 3,
      "cutFrom": 0,
      "cutTo": 10
    }
  ]
}
```

### Audio Normalization
```json
{
  "audioNorm": {
    "enable": true,
    "gaussSize": 5,
    "maxGain": 28
  }
}
```

## Transition Effects

### Popular Transitions
- **fade**: Smooth dissolve
- **wipeLeft/wipeRight**: Directional wipes
- **circleopen**: Circular reveal
- **GlitchDisplace**: Digital glitch effect
- **cube**: 3D cube rotation
- **zoom**: Scale transition

### Usage Guidelines
- Use consistent transition duration (0.8-1.5 seconds)
- Match transition to content mood
- Avoid overusing flashy effects
- Test with fast mode first

## Performance Optimization

1. **Fast Mode**: Enable for previews (`"fast": true`)
2. **Resolution**: 1280x720 for web, 1920x1080 for professional
3. **Frame Rate**: 25fps for European, 30fps for US
4. **Compression**: MP4 with H.264 codec
5. **Audio**: Normalize and duck background music

## File Path Conventions

```
/video/YYYY-MM-DD/userXXX/filename.mp4
/audio/YYYY-MM-DD/userXXX/filename.mp3
/image/YYYY-MM-DD/userXXX/filename.jpg
/font/YYYY-MM-DD/userXXX/filename.ttf
```</content>
<parameter name="filePath">/home/trapgod/qagent/jsoncut-mcp-server/agents/video-workflow.md
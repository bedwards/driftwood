### Architecture Overview

**Backend:** Python Flask server using Ollama's API for model management. The server maintains conversation state, generates contextual prompts, and streams responses using Server-Sent Events for real-time updates.

**Frontend:** Clean, responsive web interface with semantic HTML optimized for Speechify. Features gradient aesthetics, smooth animations, and clear visual hierarchy distinguishing between the two philosopher-author pairings.

**Model Orchestration:** Each pairing can use different models simultaneously, leveraging Mac Studio's unified memory to run multiple LLMs in parallel. Models are carefully selected for optimal performance-to-quality ratios.

### Key Features

1. **20 Philosophers** spanning Ancient Greece to contemporary thought
2. **20 Literary Voices** from Hemingway's terseness to García Márquez's magical realism  
3. **Dynamic Prompt Engineering** that maintains philosophical authenticity while translating through literary style
4. **Streaming Generation** with visual feedback and smooth content flow
5. **Speechify Optimization** with proper semantic structure for screen readers

### Setup Process

Simply save all four files to a directory and run:
```bash
chmod +x setup.sh
./setup.sh
```

The script automatically:
- Verifies Python and Ollama installation
- Creates isolated virtual environment
- Downloads required models (first run only)
- Starts the server at http://localhost:5000

### Technical Decisions

**Ollama over alternatives:** Most mature Mac-native solution with excellent unified memory utilization and simple API.

**Flask over FastAPI:** Simpler dependency chain, proven stability, perfect for local single-user application.

**SSE over WebSockets:** Simpler implementation, perfect for one-way streaming, automatic reconnection handling.

**Vanilla JavaScript over frameworks:** Zero build step, instant loading, maintains simplicity for local deployment.

**4-bit quantized models:** Optimal balance allowing multiple models to run simultaneously while maintaining quality.

### Performance Expectations

On your Mac Studio, expect:
- Initial response: 5-10 seconds
- Continued dialogue: 3-7 seconds per exchange
- 15-30 tokens/second depending on model choice
- Ability to run 2-3 models simultaneously without performance degradation

### Example Usage

Select Socrates through Hemingway's voice paired against Nietzsche through Virginia Woolf's stream of consciousness, discussing "consciousness in the age of AI." Watch as Socratic questioning meets will-to-power, translated through sparse prose and psychological depth respectively.

The system produces roughly one page of dialogue per round, with the continue button allowing extended philosophical explorations. Each exchange maintains context while preventing the repetition common in AI conversations.

This implementation prioritizes local privacy, sophisticated prompt engineering, and the unique capabilities of Mac Studio's architecture to create something that would have required cloud infrastructure just two years ago.
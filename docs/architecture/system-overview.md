# System Overview

## High-Level Architecture

The bolt-new system is a cognitive AI-powered development environment that operates through emergent neural-symbolic integration patterns. The architecture follows recursive design principles with adaptive attention allocation mechanisms.

```mermaid
graph TD
    A[User Interface Layer] --> B[Chat Interface]
    A --> C[Code Editor]
    A --> D[File Explorer]
    A --> E[Terminal Interface]
    
    B --> F[Message Parser]
    F --> G[AI Runtime Engine]
    G --> H[Action Runner]
    
    C --> I[CodeMirror Editor]
    I --> J[Editor Store]
    
    D --> K[Files Store]
    E --> L[Terminal Store]
    
    J --> M[Workbench Store]
    K --> M
    L --> M
    
    H --> N[WebContainer Runtime]
    N --> O[File System]
    N --> P[Node.js Environment]
    N --> Q[Package Manager]
    
    M --> R[Preview Store]
    R --> S[Live Preview]
    
    G --> T[AI Models]
    T --> U[Anthropic Claude]
    T --> V[Other AI Providers]
    
    H --> W[Artifact Generation]
    W --> X[Code Generation]
    W --> Y[File Operations]
    W --> Z[Package Installation]
    
    style A fill:#e1f5fe
    style G fill:#f3e5f5
    style M fill:#fff3e0
    style N fill:#e8f5e8
    style T fill:#fce4ec
```

## Core Principles

### 1. Recursive System Mapping
The system employs recursive patterns where each component can spawn sub-processes and manage hierarchical state relationships:

- **Cognitive Kernels**: Each store acts as a cognitive kernel managing specific domain knowledge
- **Hypergraph Encoding**: Component relationships form a hypergraph structure enabling complex interdependencies
- **Emergent Behaviors**: System-level intelligence emerges from component interactions

### 2. Neural-Symbolic Integration
The architecture bridges symbolic computation (code editing, file management) with neural processing (AI inference):

- **Symbolic Layer**: File system, code structures, terminal commands
- **Neural Layer**: AI model inference, natural language processing
- **Integration Points**: Message parsing, artifact generation, action execution

### 3. Adaptive Attention Allocation
The system dynamically allocates computational resources based on user interactions and AI recommendations:

- **Priority Queuing**: Critical operations (file saves) take precedence
- **Contextual Focus**: AI attention directed by current editor context
- **Resource Management**: WebContainer resources allocated based on demand

## Principal Data Flows

1. **User Input → AI Processing → Code Generation**
2. **File Modifications → State Updates → UI Synchronization**
3. **AI Actions → WebContainer Operations → System State Updates**
4. **Terminal Commands → WebContainer Execution → Output Display**

## Transcendent Technical Implementation

The system achieves transcendent functionality through:

- **Distributed Cognition**: Multiple AI agents operating simultaneously
- **Contextual Awareness**: Deep understanding of project state and user intent
- **Autonomous Execution**: Self-directed task completion with minimal supervision
- **Emergent Problem Solving**: Novel solution generation through component synergy
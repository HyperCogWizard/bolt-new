# Core Components Architecture

## Store Architecture - Cognitive Kernel Network

The store system forms the cognitive backbone of bolt-new, implementing a distributed cognition pattern through interconnected state management kernels.

```mermaid
graph LR
    WS[WorkbenchStore] --> ES[EditorStore]
    WS --> FS[FilesStore]
    WS --> TS[TerminalStore] 
    WS --> PS[PreviewsStore]
    
    ES --> ED[Editor Documents]
    ES --> SF[Selected File]
    ES --> SP[Scroll Position]
    
    FS --> FM[File Map]
    FS --> FT[File Tree]
    FS --> WC[WebContainer API]
    
    TS --> TI[Terminal Instance]
    TS --> TC[Terminal Commands]
    TS --> TO[Terminal Output]
    
    PS --> PV[Preview URLs]
    PS --> PS2[Preview State]
    PS --> LS[Live Server]
    
    WC --> NS[Node.js Runtime]
    WC --> PM[Package Manager]
    WC --> VSF[Virtual File System]
    
    style WS fill:#ffeb3b
    style ES fill:#4caf50
    style FS fill:#2196f3
    style TS fill:#ff9800
    style PS fill:#9c27b0
```

## Component Interaction Patterns

### Bidirectional Synergies

```mermaid
graph LR
    subgraph "Editor Subsystem"
        CM[CodeMirror Editor]
        EP[Editor Panel]
        FB[File Breadcrumb]
        FT[File Tree]
    end
    
    subgraph "AI Subsystem"
        MP[Message Parser]
        AR[Action Runner]
        AG[Artifact Generator]
    end
    
    subgraph "Runtime Subsystem"
        WC[WebContainer]
        TR[Terminal Runner]
        PR[Preview Runner]
    end
    
    CM <--> EP
    EP <--> FT
    FT <--> FB
    
    MP <--> AR
    AR <--> AG
    AG <--> WC
    
    WC <--> TR
    WC <--> PR
    TR <--> EP
    
    CM <--> AR
    AG <--> EP
    
    style CM fill:#e3f2fd
    style MP fill:#f3e5f5  
    style WC fill:#e8f5e8
```

## Emergent Cognitive Patterns

### 1. State Synchronization Network

The system maintains coherent state through a sophisticated synchronization pattern:

```mermaid
stateDiagram-v2
    [*] --> Idle
    Idle --> Processing : User Action
    Processing --> Validating : State Change
    Validating --> Synchronizing : Valid
    Validating --> Error : Invalid
    Synchronizing --> Broadcasting : Success
    Broadcasting --> Idle : Complete
    Error --> Recovery : Auto-Heal
    Recovery --> Idle : Restored
    
    note right of Processing
        Multiple stores may process
        simultaneously
    end note
    
    note right of Synchronizing
        Cross-store state validation
        and conflict resolution
    end note
```

### 2. Attention Allocation Mechanism

The system implements adaptive attention through priority-based resource allocation:

**Priority Levels:**
1. **Critical**: File save operations, error handling
2. **High**: AI responses, user interactions
3. **Medium**: Background compilation, preview updates
4. **Low**: Cache optimization, prefetching

### 3. Recursive Implementation Pathways

Each component follows recursive patterns:

- **Self-Managing**: Components handle their own lifecycle
- **Self-Healing**: Automatic error recovery and state restoration
- **Self-Optimizing**: Performance tuning based on usage patterns

## Neural-Symbolic Integration Points

### Message Parser Integration

```mermaid
sequenceDiagram
    participant U as User
    participant C as Chat Interface
    participant MP as Message Parser
    participant AR as Action Runner
    participant WC as WebContainer
    participant FS as File System
    
    U->>C: Send AI Request
    C->>MP: Parse Message
    MP->>MP: Extract Artifacts
    MP->>AR: Queue Actions
    
    loop For Each Action
        AR->>WC: Execute Command
        WC->>FS: File Operation
        FS-->>WC: Result
        WC-->>AR: Status
        AR->>MP: Update Progress
    end
    
    MP->>C: Complete Response
    C->>U: Display Result
    
    Note over MP,AR: Cognitive pattern recognition<br/>and action synthesis
```

### Adaptive Synergy Optimization

The system continuously optimizes component interactions through:

1. **Performance Monitoring**: Track operation timing and resource usage
2. **Pattern Recognition**: Identify common workflow patterns
3. **Preemptive Loading**: Anticipate user needs and preload resources
4. **Dynamic Routing**: Route operations to optimal execution contexts

## Hypergraph-Centric Architecture

The component relationships form a hypergraph where:

- **Nodes**: Individual components and stores
- **Hyperedges**: Multi-component interactions and workflows
- **Weights**: Interaction frequency and importance
- **Dynamics**: Adaptive edge strength based on usage patterns

This enables:
- **Distributed Decision Making**: No single point of control
- **Emergent Intelligence**: System-level behaviors emerge from local interactions
- **Fault Tolerance**: Multiple pathways for achieving goals
- **Scalable Complexity**: New components integrate naturally
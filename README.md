
flowchart TD
    A[Paper Created<br/>Status: Ready to Code<br/>Stage: Stage 1 Pending] --> B[Notification to Coder:<br/>Paper xxx is Ready to Code]
    
    B --> C[Coder Submits Form]
    
    C --> D[Stage: Stage 1 Coded<br/>Status: Supervisor Check]
    
    D --> E[Notification to Supervisor:<br/>Paper xxx is Coded, please review]
    
    E --> F[Supervisor Reviews & Submits Form]
    
    F --> G{Review Decision}
    
    G -->|No Changes| H[Stage: Stage 1 Reviewed - No Changes<br/>Status: Ready to Code]
    G -->|Minor Changes| I[Stage: Stage 1 Reviewed - Minor Changes<br/>Status: Ready to Code]
    G -->|Resubmit Requested| J[Stage: Stage 1 Reviewed - Resubmit Requested<br/>Status: Resubmit]
    G -->|PI Hold| K[Stage: Stage 1 Reviewed - PI Hold]
    
    H --> L[Notification to Coder:<br/>Paper xxx pass supervisor check,<br/>please proceed to next stage]
    I --> L
    
    J --> M[Notification to Coder:<br/>Paper xxx did not pass supervisor check,<br/>please see comments and resubmit]
    
    L --> N{Is this the<br/>last stage?}
    
    N -->|No| O[Move to Next Stage<br/>Status: Ready to Code<br/>Stage: Stage X Pending]
    N -->|Yes| P[Status: Done<br/>Process Complete]
    
    O --> B
    M --> Q[Coder Resubmits]
    Q --> D
    
    style A fill:#e1f5fe
    style P fill:#c8e6c9
    style K fill:#fff3e0
    style J fill:#ffebee
    style M fill:#ffebee

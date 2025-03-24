# NCD Causal Loop Diagram

This diagram visualizes the factors contributing to non-communicable diseases (NCDs) among minority groups in the US.

```mermaid
graph TD
    A[Individual Level: Poor Diet, Lack of Exercise, Smoking, Stress] --> B(NCDs: Diabetes, Heart Disease, Hypertension, Cancer);
    C[Interpersonal Level: Lack of Social Support, Family History, Peer Influence] --> B;
    D[Organizational Level: Limited Access to Healthcare, Workplace Stress, Lack of Health Promotion Programs] --> B;
    E[Community Level: Food Deserts, Lack of Safe Spaces for Exercise, Exposure to Pollution] --> B;
    F[Public Policy Level: Inadequate Funding for Public Health, Lack of Regulations on Food Industry, Limited Access to Affordable Healthcare] --> B;
    G[Systemic/Societal Level: Racism, Discrimination, Socioeconomic Disparities, Historical Trauma] --> B;

    B -- Increases --> H[Healthcare Costs];
    B -- Decreases --> I[Quality of Life];
    B -- Decreases --> J[Productivity];

    G --> E;
    G --> D;
    G --> C;
    G --> A;
    F --> E;
    F --> D;

    K[Solution 1: Culturally Tailored Community Health Programs] --> L[Improved Access to Healthy Food, Exercise Programs, Health Education];
    L --> B;
    M[Solution 2: Policy Changes Targeting Systemic Racism & Disparities] --> N[Increased Funding for Minority Health Initiatives, Equitable Healthcare Access, Anti-Discrimination Laws];
    N --> G;

    style B fill:#f9f,stroke:#333,stroke-width:2px;
    style G fill:#ccf,stroke:#333,stroke-width:2px;
    style F fill:#ccf,stroke:#333,stroke-width:2px;
    style E fill:#ccf,stroke:#333,stroke-width:2px;
    style D fill:#ccf,stroke:#333,stroke-width:2px;
    style C fill:#ccf,stroke:#333,stroke-width:2px;
    style A fill:#ccf,stroke:#333,stroke-width:2px;
    style K fill:#90EE90,stroke:#333,stroke-width:2px;
    style M fill:#90EE90,stroke:#333,stroke-width:2px;

    subgraph "Levels of Influence"
        A;C;D;E;F;G;
    end

    subgraph "Consequences"
        H;I;J;
    end

    subgraph "Solutions"
        K;M;
    end

    classDef blueFill fill:#ccf,stroke:#333,stroke-width:2px;
    class A,C,D,E,F,G blueFill;

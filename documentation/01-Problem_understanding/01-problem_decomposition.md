ORDER OF STRATEGIES TO USE:

    1. Domain Concept Decomposition.
        Exposes:
            * data boundaries
            * ubiquitous language
            * system entities/primary objects that will require database storage and state management

    2. Capability Decomposition.
        Exposes:
            * functional requirements
            * user interaction with the system and what value each component delivers
            * services boundaries of business modules or microservices that can be developed and scale independently

    3. Dependency Decomposition.
        Exposes:
            * execution order
            * coupling and bottlenecks
            * integration points

    4. Difficulty/Risk Decomposition.
        Exposes:
            * technical risks -> shows architectural unknowns, performance hazards and security vulnerabilities
            * knowledge gaps -> where the team lacks expertise or where requirements are too vague
            * estimation accuracy for project timelines
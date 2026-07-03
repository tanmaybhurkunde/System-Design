# 🌐 API Gateway Split Patterns

```mermaid
flowchart TD
    subgraph API["🌐 API GATEWAY SPLIT PATTERNS"]
        A["Different ways to split API Gateways\nbased on traffic, domain, and scale requirements"]
    end

    %% Pattern 1: Domain-Based Split
    subgraph BOUNDED["📦 Pattern 1: Bounded Context / Domain-Based Split"]
        B1["Load Balancer"]
        B1 --> B2["🔐 Auth Gateway\n\n• /login\n• /signup\n• /logout\n• /refresh-token"]
        B1 --> B3["🎮 Game Gateway\n\n• /join-match\n• /move-token\n• /room\n• /game-state"]
        B1 --> B4["🛡️ Admin Gateway\n\n• /ban-user\n• /create-tournament\n• /moderate\n• /analytics"]
    end

    %% Pattern 2: Internal vs External
    subgraph EXTERNAL["🔒 Pattern 2: Internal vs External"]
        E1["Load Balancer"]
        E1 --> E2["🌍 External Gateway\n\nMobile App\nWeb App\nThird-party APIs"]
        E1 --> E3["🏠 Internal Gateway\n\nService-to-Service\n• Auth Service\n• Payment Service\n• Analytics Service"]
    end

    %% Pattern 3: Read vs Write
    subgraph READWRITE["📝 Pattern 3: Read vs Write"]
        R1["Load Balancer"]
        R1 --> R2["📖 Read Gateway\n\nHigh Volume:\n• GET /leaderboard\n• GET /profile\n• GET /feed\n• GET /search"]
        R1 --> R3["✍️ Write Gateway\n\nLower Volume:\n• POST /move\n• POST /payment\n• PUT /profile\n• DELETE /item"]
    end

    %% Pattern 4: Geographic Split
    subgraph GEO["🌍 Pattern 4: Geographic Split"]
        G1["Global Load Balancer"]
        G1 --> G2["🇮🇳 India Gateway\n\n• Mumbai Region\n• ap-south-1\n• Low latency for India"]
        G1 --> G3["🇺🇸 US Gateway\n\n• us-east-1\n• us-west-2\n• North America traffic"]
        G1 --> G4["🇪🇺 Europe Gateway\n\n• eu-west-1\n• eu-central-1\n• EU compliance (GDPR)"]
    end

    %% Pattern 5: Protocol-Based Split
    subgraph PROTOCOL["🔌 Pattern 5: Protocol-Based Split"]
        P1["Load Balancer"]
        P1 --> P2["🌐 HTTP Gateway\n\nCharacteristics:\n• Short-lived connections\n• Stateless\n• REST APIs\n• Request-Response\n• Scale: Pods\n\nExamples:\n• REST APIs\n• File uploads\n• Health checks"]
        P1 --> P3["📡 WebSocket Gateway\n\nCharacteristics:\n• Long-lived connections\n• Stateful\n• Real-time\n• Pub/Sub\n• Scale: Connections\n\nExamples:\n• Chat\n• Gaming\n• Live updates\n• Collaborative editing"]
    end

    %% Quick Comparison
    subgraph COMPARISON["📊 Quick Comparison"]
        C1["| Pattern | When to Use |\n|---------|-------------|\n| Domain-Based | Different business domains |\n| Internal/External | Security separation |\n| Read/Write | Massive scale |\n| Geographic | Global users |\n| Protocol-Based | Different traffic types |"]
    end

    %% Connections
    API --> BOUNDED
    API --> EXTERNAL
    API --> READWRITE
    API --> GEO
    API --> PROTOCOL
    API --> COMPARISON

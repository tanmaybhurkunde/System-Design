# 🏗️ System Design Patterns
Building Blocks of Large Systems

```mermaid
flowchart TD
    A["🏗️ System Design Patterns\nBuilding Blocks of Large Systems"] --> B["📋 CRUD Systems"]
    A --> C["🎫 Booking Systems"]
    A --> D["⚡ Real-Time Systems"]
    A --> E["📱 Feed Systems"]
    A --> F["📍 Tracking Systems"]
    A --> G["🎬 Streaming Systems"]
    A --> H["📊 Analytics Systems"]

    %% CRUD Systems
    B["📋 CRUD Systems\n\n📌 Examples:\n• Employee Management\n• Inventory Management\n• Hospital Records\n• Hotel Management\n\n⚙️ Core Operations:\n• Create (POST)\n• Read (GET)\n• Update (PUT/PATCH)\n• Delete (DELETE)\n\n🔍 Main Discussion:\n• Database Design (Schema, Normalization)\n• Search (Indexing, Full-Text)\n• Access Control (RBAC, Permissions)\n\n🏛️ Architecture:\nClient → API Gateway → Service Layer → Database"]

    %% Booking Systems
    C["🎫 Booking Systems\n\n📌 Examples:\n• BookMyShow\n• Flight Booking\n• Hotel Booking\n• Train Reservation\n\n⚠️ Core Challenge:\n• Concurrency & Race Conditions\n• 'Last seat available – Two users click simultaneously – Who gets it?'\n\n🔒 Main Discussion:\n• Locking (Pessimistic vs Optimistic)\n• Consistency (ACID vs BASE)\n• Transactions (Isolation Levels)\n• Idempotency\n• Queue-based Booking"]

    %% Real-Time Systems
    D["⚡ Real-Time Systems\n\n📌 Examples:\n• Ludo / Chess (Multiplayer Games)\n• WhatsApp (Chat)\n• Collaborative Whiteboard\n• Live Sports Scores\n\n⚠️ Core Challenge:\n• State Synchronization\n• Keeping all clients in sync in real-time\n\n🔌 Main Discussion:\n• WebSocket (Persistent Connections)\n• Pub/Sub (Message Broadcasting)\n• Event Ordering (Sequence Numbers)\n• Reconnection & State Recovery\n• Conflict Resolution (OT/CRDT)"]

    %% Feed Systems
    E["📱 Feed Systems\n\n📌 Examples:\n• Facebook Feed\n• Instagram Feed\n• LinkedIn Feed\n• Twitter Timeline\n\n⚠️ Core Challenge:\n• Ranking (Relevance Algorithm)\n• Aggregation (Content Mix)\n• Massive Reads (Millions of users)\n\n📦 Main Discussion:\n• Fanout (Push vs Pull vs Hybrid)\n• Caching (Redis, CDN)\n• Feed Generation (Pre-computation)\n• Personalization (ML Ranking)\n• Pagination (Cursor-based)"]

    %% Tracking Systems
    F["📍 Tracking Systems\n\n📌 Examples:\n• Uber / Lyft\n• Food Delivery (Zomato, DoorDash)\n• Fleet Tracking\n• Package Delivery\n\n⚠️ Core Challenge:\n• Location Updates\n• Tracking millions of moving objects\n\n🗺️ Main Discussion:\n• Geospatial Indexing (GeoHash, S2, Quadtree)\n• Nearby Search (Radius Queries)\n• Real-time Updates (Streaming)\n• ETA Calculation\n• Driver-Rider Matching"]

    %% Streaming Systems
    G["🎬 Streaming Systems\n\n📌 Examples:\n• YouTube\n• Netflix\n• Spotify\n• Twitch\n\n⚠️ Core Challenge:\n• Large Content Delivery\n• Streaming high-bandwidth content\n\n🌐 Main Discussion:\n• CDN (Content Delivery Network)\n• Chunking (Adaptive Bitrate)\n• Storage (Object Storage – S3)\n• Pre-fetching & Buffering\n• DRM & Content Protection"]

    %% Analytics Systems
    H["📊 Analytics Systems\n\n📌 Examples:\n• Metrics Platform\n• Event Tracking (Google Analytics)\n• Monitoring (Prometheus)\n• Log Aggregation\n\n⚠️ Core Challenge:\n• Huge Write Volume\n• Millions of events per second\n\n📈 Main Discussion:\n• Kafka (Event Streaming)\n• Batch Processing (Spark, Flink)\n• Aggregation (Time-series DB)\n• Data Retention Policies\n• Real-time Dashboards"]

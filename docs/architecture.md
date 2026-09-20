# High-Level Architecture – FitFlow Redesign

## System Components

1. **Client Layer**
   - Flutter mobile app (iOS & Android)
   - Flutter Web

2. **API Layer**
   - NestJS Backend (main business logic, social features, user management)

3. **AI Microservice**
   - FastAPI service for:
     - Personalized workout plan generation
     - Computer vision based nutrition logging

4. **Data Layer**
   - PostgreSQL (primary database)
   - Redis (caching and real-time)

5. **Authentication**
   - Supabase Auth / Firebase Auth

6. **Supporting Services**
   - Object Storage (images)
   - Push Notifications

## Critical Data Flows

### 1. Personalized Workout Plan
Client → NestJS → AI Service → PostgreSQL → Client

### 2. Nutrition Tracking (Camera)
Client → AI Vision Service → NestJS → PostgreSQL

### 3. Social Features
Client → NestJS → PostgreSQL + Real-time broadcast

## Security Considerations
- JWT-based authentication
- HTTPS everywhere
- Row-level or role-based access control
- Encryption at rest and in transit
- GDPR compliant data handling

## Scalability Considerations
- Horizontal scaling of NestJS and FastAPI services
- Managed PostgreSQL with read replicas
- Redis for high-traffic caching
- CDN for static assets and images
# Architecture Decision Record (ADR)

**Title:** Choose Flutter + NestJS + PostgreSQL + FastAPI for FitFlow Redesign  
**Status:** Accepted  
**Date:** September 2026  

## Context
FitFlow requires a seamless experience across iOS, Android and Web, high performance, AI-powered personalization, real-time social features, and strong data privacy (GDPR). The team is mid-sized and needs a balance between development speed and long-term maintainability.

## Decision
We will use the following stack:
- **Frontend:** Flutter
- **Backend:** NestJS (TypeScript)
- **AI Service:** FastAPI (Python)
- **Database:** PostgreSQL
- **Authentication:** Supabase Auth (or Firebase Auth)
- **Caching:** Redis

## Consequences
**Positive:**
- Single codebase for mobile and web
- Clear separation of concerns (especially AI)
- Good performance and real-time capabilities
- Strong path for compliance and scalability
- Reasonable learning curve and hiring availability

**Negative / Trade-offs:**
- Team needs to work with both Dart and TypeScript/Python
- Slightly more initial setup than a pure Firebase stack
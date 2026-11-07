# Scalability Strategy — LinkLite

## 1. Initial Architecture

Phase 1 uses a single Django application instance and PostgreSQL database.

## 2. Current Bottlenecks

Potential bottlenecks include:
- Database lookup latency.
- Database connection limits.
- High volumes of redirect requests.
- Short-code generation collisions.
- Database write contention.

## 3. Future Improvements

### Caching
Redis may be introduced to cache frequently accessed short-code mappings.

### Horizontal Scaling
Multiple Django application instances may be deployed behind a load balancer.

### Database Optimisation
Indexes and query optimisation may improve lookup performance.

### Rate Limiting
Request limits may reduce abuse and protect application resources.

## 4. Phase 1 Decision

No distributed architecture or caching infrastructure will be introduced unless testing demonstrates a genuine need.

# Vironix – Intelligent Social Media Backend Platform
Built a modular monolith social interaction platform with Redis-based concurrency protection, virality tracking, guardrail enforcement, and event-driven notification batching.

**Overview**

This project is a backend microservice built using Spring Boot, PostgreSQL, and Redis.  
The system simulates a social media backend where users and bots can create posts, add comments, like posts, and trigger notifications.

The main goal of this project is not only to build REST APIs, but also to design a scalable and concurrency-safe backend system similar to real-world social media platforms.

The application uses:

- PostgreSQL to store permanent data such as users, posts, comments, and likes.
- Redis to manage high-speed temporary data such as virality scores, bot interaction limits, cooldown timers, and notification queues.

The system includes several backend engineering concepts such as:

- Atomic Redis operations
- Concurrency protection
- Stateless backend architecture
- Real-time virality tracking
- Notification batching
- Scheduled background jobs

One of the key challenges solved in this project is handling concurrent bot interactions safely.  
For example, if hundreds of bots try to comment on the same post simultaneously, Redis atomic counters ensure that the system strictly enforces the maximum allowed bot reply limit without race conditions.

The project is designed to mimic how large-scale backend systems separate responsibilities between:
- Persistent databases (PostgreSQL)
- Fast distributed state management systems (Redis)

This assignment demonstrates:

- Backend API development
- Redis-based guardrail systems
- Distributed locking concepts
- Thread-safe system design
- Scalable m3. Tech Stack

Tech Stack

 Technology             		Purpose 
------------                 		---------
 Java 17                   		Backend Language 
 Spring Boot 3          		REST API Framework 
 PostgreSQL            		Persistent Database 
 Redis                       		Fast in-memory state management 
 Docker                     		Local container setup 
 Spring Scheduler     		Notification sweeper 
 JPA/Hibernate/ORM 		Microservice architecture



# 🐪 camelAI - The AI Data Analyst

camelAI is your intelligent data analyst that connects to your databases, understands your business, and gives you answers in natural language.  

## 🚀 Getting Started

### Prerequisites

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/)

### 🔧 Running camelAI

To start the application in production mode:

```bash
docker compose -f docker-compose.prod.yml up -d
```

This will spin up the full stack including:
- `camel` – the main application
- `nginx` – reverse proxy
- `pgvector` – PostgreSQL with vector extension
- `memcached` – for caching

Make sure your `.env.docker` file is correctly set up with the required environment variables.

### 👤 Creating a Superuser

Once the services are running, create an initial superuser by running:

```bash
docker compose exec camel python manage.py createsuperuser
```

Follow the prompts to set up the superuser credentials.

### 🌐 Logging In

Once you've created a superuser, you can log in to the camelAI web interface by visiting:

```
http://localhost:8000
```

Use the superuser credentials you just created to sign in and start analyzing your data.

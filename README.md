
# My Symfony Project

A high-performance Symfony backend application designed for scalable microservices architecture — production-ready and optimized for real-world deployment.

## Features

- Symfony 7+ with modern component stack
- JWT Authentication via LexikJWTAuthenticationBundle
- Redis caching and Messenger integration
- Doctrine ORM with Migrations
- CORS enabled via NelmioCORSBundle
- Flexible configuration and environment setup
- Ready for Docker, CI/CD, and API Platform

## Installation

```bash
composer install
cp .env .env.local
# Configure your environment variables:
# DATABASE_URL, JWT_SECRET_KEY, CORS_ALLOW_ORIGIN, etc.
php bin/console doctrine:database:create
php bin/console doctrine:migrations:migrate
php bin/console server:run
```

## Included Configurations

This project comes pre-configured with:

### JWT Authentication
LexikJWTAuthenticationBundle is set up. Ensure you provide secret_key or public_key/private_key in your JWT configuration.

### Database
Uses Doctrine ORM and Migrations. You can configure your connection via DATABASE_URL in .env.

### Redis & Messenger
Configured to support symfony/redis-messenger for async task processing with Redis.

### CORS Setup
NelmioCORSBundle allows cross-origin requests. You can adjust origins and methods in nelmio_cors.yaml.

### Property Info / Serializer / Validator
Enabled with Symfony default configuration. Suitable for use with DTOs, OpenAPI generation, and form handling.

### Webpack Encore (Optional)
If using a separate frontend, disable or adjust webpack_encore config to prevent errors from missing output_path.

### Runtime Configuration
Symfony Runtime is required for modern bin/console usage. Make sure symfony/runtime is installed.

### Environment-specific settings
Includes separate configs for dev, test, and prod environments.

## License

This project is licensed under the MIT License. See the LICENSE file for details.


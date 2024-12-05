# Smart City

## Tech Stack and Architecture:

- API Gateway: Kong for routing and aggregating requests.
- Message Queue: RabbitMQ for service-to-service communication.
- Database:
  - Shared DB (PostgreSQL) for simple MVP.
  - Future: Polyglot persistence (MongoDB for IoT, MySQL for events, etc.).
- Tracing and Logging: OpenTelemetry for distributed tracing, Elastic Stack for logs.

### Backend services

- Authentication Service (TypeScript/NestJS)

Handles user login, registration, and token generation (JWT).
Future: Add OAuth2, multi-factor authentication.

- Notifications Service (Go)

Manage and handles all system notifications, by email.
Future: Add Push notifications.

- Weather Analytics Service (Python/Flask)

Fetches and analyzes weather data (e.g., via APIs like OpenWeatherMap) and provides predictions.
Future: Add historical weather trends or alerting features.

- Event Scheduling Service (Java/SpringBoot)

Allows users to create and manage public events (concerts, meetups, etc.).
Future: Add calendar sync, notifications.

### Frontend

- Web (Angular)

A dashboard displaying aggregated data from all services.
Interactive features like live traffic maps, event calendars, and weather widgets.


### Future

- IoT Device Management Service (Rust)

Manages sensors/devices in a smart city, ensuring secure and efficient communication.

- Traffic Monitoring Service (Go)

Real-time vehicle data ingestion and processing using WebSockets or gRPC.

- Billing Service (C#)

Processes payments for services like parking or public transport passes integrating with payment gateways like Stripe or PayPal.

- Mobile app (Flutter)

A simplified version of the dashboard with location-based features (e.g., find events near you).

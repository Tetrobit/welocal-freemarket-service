# WeLocal Freemarket Service

Local marketplace and trading service for the WeLocal platform, built with Node.js and Express.

## Tech Stack

- **Runtime**: Node.js
- **Framework**: Express.js
- **Database**: PostgreSQL
- **Authentication**: JWT (JSON Web Tokens)
- **API Documentation**: Swagger/OpenAPI
- **Testing**: Jest
- **Logging**: Winston
- **Validation**: Joi
- **ORM**: TypeORM
- **File Storage**: AWS S3
- **Search Engine**: Elasticsearch
- **Payment Processing**: Stripe
- **Real-time Communication**: Socket.io

## Features

- Product listing and management
- Search and filtering
- Shopping cart functionality
- Order management
- Payment processing
- Real-time notifications
- User ratings and reviews
- Category management
- Location-based search
- Chat between buyers and sellers

## Prerequisites

- Node.js (v18 or higher)
- PostgreSQL
- Elasticsearch
- npm or yarn
- AWS S3 bucket
- Stripe account

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-org/welocal-freemarket-service.git
   cd welocal-freemarket-service
   ```

2. Install dependencies:
   ```bash
   npm install
   # or
   yarn install
   ```

3. Create environment file:
   ```bash
   cp .env.example .env
   ```

4. Configure environment variables in `.env`:
   ```env
   NODE_ENV=development
   PORT=8082
   DATABASE_URL=postgresql://welocal:welocal123@localhost:5432/welocal
   ELASTICSEARCH_URL=http://localhost:9200
   AWS_ACCESS_KEY_ID=your-aws-access-key
   AWS_SECRET_ACCESS_KEY=your-aws-secret-key
   AWS_REGION=your-aws-region
   AWS_S3_BUCKET=your-s3-bucket
   STRIPE_SECRET_KEY=your-stripe-secret-key
   STRIPE_WEBHOOK_SECRET=your-stripe-webhook-secret
   ```

## Running the Service

### Development Mode
```bash
npm run dev
# or
yarn dev
```

### Production Mode
```bash
npm run build
npm start
# or
yarn build
yarn start
```

### Docker
```bash
docker build -t welocal-freemarket-service .
docker run -p 8082:8082 welocal-freemarket-service
```

## API Endpoints

### Products
- `GET /api/v1/products` - Get products list
- `POST /api/v1/products` - Create product
- `GET /api/v1/products/:id` - Get product details
- `PUT /api/v1/products/:id` - Update product
- `DELETE /api/v1/products/:id` - Delete product

### Orders
- `GET /api/v1/orders` - Get orders list
- `POST /api/v1/orders` - Create order
- `GET /api/v1/orders/:id` - Get order details
- `PUT /api/v1/orders/:id/status` - Update order status

### Cart
- `GET /api/v1/cart` - Get cart contents
- `POST /api/v1/cart/items` - Add item to cart
- `PUT /api/v1/cart/items/:id` - Update cart item
- `DELETE /api/v1/cart/items/:id` - Remove item from cart

### Payments
- `POST /api/v1/payments/create-intent` - Create payment intent
- `POST /api/v1/payments/webhook` - Handle payment webhooks
- `GET /api/v1/payments/history` - Get payment history

## API Documentation

API documentation is available at `/api-docs` when running the service.

## Testing

### Unit Tests
```bash
npm run test
# or
yarn test
```

### Integration Tests
```bash
npm run test:integration
# or
yarn test:integration
```

### E2E Tests
```bash
npm run test:e2e
# or
yarn test:e2e
```

## Project Structure

```
src/
├── config/           # Configuration files
├── controllers/      # Route controllers
├── middleware/       # Custom middleware
├── models/          # Database models
├── routes/          # API routes
├── services/        # Business logic
├── utils/           # Utility functions
├── validators/      # Request validation
├── storage/         # File storage handling
├── search/          # Search functionality
├── payments/        # Payment processing
├── websocket/       # Real-time communication
└── app.js           # Application entry point
```

## Security Features

- JWT token-based authentication
- Rate limiting
- CORS configuration
- Helmet security headers
- Input validation
- SQL injection prevention
- XSS protection
- File upload validation
- Secure payment processing
- Webhook signature verification

## Monitoring

The service exposes the following endpoints for monitoring:
- `/health` - Health check
- `/metrics` - Prometheus metrics
- `/status` - Service status

## Logging

Logs are written to:
- Console (development)
- File (production)

Log levels:
- ERROR
- WARN
- INFO
- DEBUG

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

[Your License Here]

## Support

For support, please contact [Your Contact Information] 
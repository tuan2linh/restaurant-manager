# Restaurant Management System

A comprehensive restaurant management solution with a modern web frontend and robust backend API for managing restaurant zones, tables, and customers.

## Project Overview

- **Frontend**: Modern Next.js web application
- **Backend**: NestJS REST API
- **Live Demo**: [restaurant.tuanlinh.site](https://restaurant.tuanlinh.site)
- **API Documentation**: [restaurantbe.azurewebsites.net/api](https://restaurantbe.azurewebsites.net/api)

## Features

- **Zone Management**
  - Create, edit, and delete restaurant zones
  - View zone statistics and occupancy rates
- **Table Management**
  - Manage tables within zones
  - Track table status (available/occupied)
  - Assign customers to tables
- **Customer Management**
  - Register new customers
  - Track customer seating
  - Manage customer information

## Technology Stack

### Frontend
- Next.js 15.3
- TailwindCSS 4.1
- React Hooks for state management
- Axios for API integration
- Chart.js with React-Chartjs-2

### Backend
- NestJS 11.0
- TypeScript
- TypeORM
- MySQL Database
- Swagger/OpenAPI
- Docker & Docker Compose

## Getting Started

### Backend Setup

1. Clone the backend repository:
```bash
git clone https://github.com/tuan2linh/mobile-app-restaurant-be.git
cd mobile-app-restaurant-be
```

2. Set up the database:
```bash
# Using Docker (Recommended)
docker-compose up -d

# Create .env file
DB_HOST=localhost
DB_PORT=3307
DB_USERNAME=root
DB_PASSWORD=secret
DB_NAME=restaurant
```

3. Install and run:
```bash
npm install
npm run start:dev
```

The backend API will be available at `http://localhost:8080`

### Frontend Setup

1. Clone the frontend repository:
```bash
git clone https://github.com/tuan2linh/restaurant-manager-fe.git
cd restaurant-frontend
```

2. Install dependencies:
```bash
npm install
```

3. Configure API endpoint:
```env
# .env file
# Use deployed API
NEXT_PUBLIC_API_URL=https://restaurantbe.azurewebsites.net

# Or use local backend
# NEXT_PUBLIC_API_URL=http://localhost:8080
```

4. Start development server:
```bash
npm run dev
```

Visit [http://localhost:3000](http://localhost:3000) to see the application.

## Project Structure

```
restaurant-manager/
├── frontend/
│   ├── src/
│   │   ├── app/         # Next.js pages
│   │   ├── components/  # React components
│   │   ├── services/    # API services
│   │   └── types/      # TypeScript types
│   └── public/         # Static files
│
├── backend/
│   ├── src/
│   │   ├── modules/    # Feature modules
│   │   ├── config/     # Configuration
│   │   ├── services/   # Business logic
│   │   └── entities/   # Database models
│   └── test/          # Test files
```

## Testing

### Backend Tests
```bash
# Unit tests
npm run test

# E2E tests
npm run test:e2e
```

### Frontend Tests
```bash
npm test
```

## Deployment

- Frontend is deployed to Vercel
- Backend is hosted on Azure Web Apps
- Database is hosted on Azure MySQL

## License

This project is licensed under the MIT License - see the LICENSE file for details.

# POC

## Description

A modern web application built with React and NestJS, featuring a robust backend API and a beautiful frontend interface.

## Project Structure

The project consists of two main parts:
- Frontend (React + Vite)
- Backend (NestJS)

## Prerequisites

- Node.js (v22 - specified in .nvmrc)
- npm or yarn
- PostgreSQL database
- Supabase account
- Docker
- Supabase CLI

## Local Supabase Setup

To run Supabase locally:

1. Install the Supabase CLI:
```bash
# Using npm
npm install -g supabase

# Or using Homebrew (macOS)
brew install supabase/tap/supabase
```

2. Start the Supabase services:
```bash
# Start Supabase services
supabase start

# This will start:
# - PostgreSQL database on port 54322
# - Supabase Studio on port 54323
# - Supabase API on port 54321
```

3. Access the Supabase Studio at `http://localhost:54323`
4. The default credentials are:
   - Email: `admin@admin.com`
   - Password: `admin`

5. To stop the services:
```bash
supabase stop
```

6. To reset the database:
```bash
supabase db reset
```

## Environment Setup

### Frontend Environment Variables

Create a `.env` file in the root directory with the following variables:
```
VITE_API_URL=http://localhost:3000
VITE_SUPABASE_URL=your-supabase-url
VITE_MAPBOX_PUBLIC_ACCESS_TOKEN=your-mapbox-public-api-key
VITE_SUPABASE_ANON_KEY=your-supabase-anon-key
```

### Backend Environment Variables

Create a `.env` file in the `api` directory with:
```
DATABASE_URL=postgresql://postgres:postgres@127.0.0.1:54322/postgres
DIRECT_URL=postgresql://postgres:postgres@127.0.0.1:54322/postgres
SUPABASE_URL=your-supabase-url
SUPABASE_SERVICE_ROLE_KEY=your-supabase-service-role-key
```

## Installation

1. Clone the repository
2. Install dependencies:
```bash
# Install frontend dependencies
npm install

# Install backend dependencies
cd api
npm install
```

## Development

### Frontend Development
```bash
# Start the development server
npm run dev
```

### Backend Development
```bash
# Navigate to api directory
cd api

# Start the development server
npm run start:dev
```

## Testing

### Frontend Tests
```bash
npm run test
```

### Backend Tests
```bash
cd api
npm run test
```

## Deployment

The project includes GitHub Actions workflows for different environments:
- Staging
- Production
- Development

Each environment has its own configuration and deployment process.

## Code Style

The project uses:
- ESLint for code linting
- Prettier for code formatting
- Husky for git hooks
- Commitlint for commit message validation

## License

[Add your license information here]

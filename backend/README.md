# Team Allocator - Backend

RESTful API server built with Express.js, TypeScript, and Prisma ORM with PostgreSQL.

## 🚀 Tech Stack

- **Node.js** with **Express.js** framework
- **TypeScript** for type safety
- **Prisma** ORM with **PostgreSQL** database
- **CORS** for cross-origin requests
- **dotenv** for environment variables

## 📁 Project Structure

```
backend/
├── src/
│   └── index.ts          # Main server file
├── prisma/
│   └── schema.prisma     # Database schema
├── .env                  # Environment variables
├── .env.example          # Example environment file
├── tsconfig.json         # TypeScript configuration
└── package.json          # Dependencies and scripts
```

## 🛠️ Setup

### Prerequisites

- Node.js (v16 or higher)
- PostgreSQL database running
- npm package manager

### Installation

1. **Navigate to backend directory**
   ```bash
   cd backend
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Configure environment variables**
   ```bash
   cp .env.example .env
   ```
   Update the `.env` file with your database credentials:
   ```env
   DATABASE_URL="postgresql://username:password@localhost:5432/team_allocator"
   PORT=3000
   NODE_ENV=development
   ```

4. **Generate Prisma client**
   ```bash
   npm run prisma:generate
   ```

5. **Push database schema**
   ```bash
   npm run prisma:push
   ```

## 🏃‍♂️ Running the Server

### Development Mode
```bash
npm run dev
```
Server will start on `http://localhost:3000` with hot reloading.

### Production Mode
```bash
npm run build
npm start
```

## 📝 Available Scripts

- `npm run dev` - Start development server with hot reloading
- `npm run build` - Build TypeScript to JavaScript
- `npm start` - Start production server
- `npm run prisma:generate` - Generate Prisma client
- `npm run prisma:push` - Push schema changes to database
- `npm run prisma:studio` - Open Prisma Studio (database GUI)

## 🗄️ Database Schema

The current schema includes:

### User
- `id`: Unique identifier
- `email`: User's email (unique)
- `name`: Optional display name
- `role`: User role (ADMIN, MANAGER, MEMBER)
- `createdAt`, `updatedAt`: Timestamps

### Team
- `id`: Unique identifier
- `name`: Team name
- `description`: Optional team description
- `maxMembers`: Maximum team size (default: 5)
- `creatorId`: Reference to user who created the team
- `createdAt`, `updatedAt`: Timestamps

### TeamMember
- Junction table for User-Team many-to-many relationship
- `userId`: Reference to user
- `teamId`: Reference to team
- `joinedAt`: When user joined the team

## 🔗 API Endpoints

### Health Check
- `GET /` - Basic API information
- `GET /health` - Health check endpoint

### Users (Ready for implementation)
- `GET /api/users` - Get all users

## 🔧 Development

### Adding New Routes
1. Create route handlers in `src/`
2. Import and use in `src/index.ts`
3. Update Prisma schema if needed
4. Run database migrations

### Database Changes
1. Update `prisma/schema.prisma`
2. Run `npm run prisma:push` to apply changes
3. Run `npm run prisma:generate` to update client

## 🚀 Deployment

1. Set production environment variables
2. Build the application: `npm run build`
3. Start the server: `npm start`

## 📊 Database Management

Access Prisma Studio for a visual database interface:
```bash
npm run prisma:studio
```

This will open a web interface at `http://localhost:5555` to view and edit your database.

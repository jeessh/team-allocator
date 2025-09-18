# Team Allocator

A full-stack web application built with modern technologies for team allocation and management.

## 🚀 Tech Stack

### Frontend
- **React 18** with **TypeScript**
- **Vite** for fast development and building
- **Tailwind CSS** for styling
- **npm** package manager

### Backend
- **Node.js** with **Express**
- **TypeScript** for type safety
- **Prisma** ORM with **PostgreSQL** database
- **npm** package manager

## 📁 Project Structure

```
team-allocator/
├── frontend/          # React + Vite + TypeScript + Tailwind
├── backend/           # Express + TypeScript + Prisma
└── README.md
```

## 🛠️ Getting Started

### Prerequisites
- Node.js v18+ (v22.19+ recommended)
- PostgreSQL database
- npm v10+

### Installation

1. **Clone and navigate to the project directory**
   ```bash
   cd team-allocator
   ```

2. **Install frontend dependencies**
   ```bash
   cd frontend
   npm install
   ```

3. **Install backend dependencies**
   ```bash
   cd ../backend
   npm install
   ```

4. **Setup environment variables**
   - Copy `.env.example` to `.env` in the backend folder
   - Update the `DATABASE_URL` with your PostgreSQL connection string

5. **Setup database**
   ```bash
   # In backend directory
   npx prisma generate
   npx prisma db push
   ```

### Development

**Start the backend server:**
```bash
cd backend
npm run dev
```

**Start the frontend development server:**
```bash
cd frontend
npm run dev
```

The frontend will be available at `http://localhost:5173` and the backend at `http://localhost:3000`.

## 📝 Available Scripts

### Frontend
- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build
- `npm run lint` - Run ESLint

### Backend
- `npm run dev` - Start development server with hot reload
- `npm run build` - Build TypeScript to JavaScript
- `npm start` - Start production server
- `npm run prisma:generate` - Generate Prisma client
- `npm run prisma:push` - Push schema changes to database

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## 📄 License

This project is licensed under the MIT License.

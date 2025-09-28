# Team Allocator - Frontend

Modern React application built with Vite, TypeScript, and Tailwind CSS for team allocation and management.

## 🚀 Tech Stack

- **React 18** with **TypeScript**
- **Vite** for fast development and building  
- **Tailwind CSS** for utility-first styling
- **ESLint** for code linting
- **npm** package manager

## 🛠️ Setup

### Prerequisites
- Node.js (v16 or higher recommended)
- npm package manager

### Installation

1. **Navigate to frontend directory**
   ```bash
   cd frontend
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

## 🏃‍♂️ Running the Application

### Development Mode
```bash
npm run dev
```
Application will be available at `http://localhost:5173`

### Build for Production
```bash
npm run build
```

### Preview Production Build
```bash
npm run preview
```

## 📝 Available Scripts

- `npm run dev` - Start development server with hot reloading
- `npm run build` - Build for production
- `npm run preview` - Preview production build locally
- `npm run lint` - Run ESLint for code linting

## 🎨 Styling with Tailwind CSS

This project uses Tailwind CSS for styling. The main landing page demonstrates various Tailwind utilities including:

- Responsive design with `md:` breakpoints
- Gradient backgrounds (`bg-gradient-to-br`)
- Hover effects (`hover:bg-blue-700`)
- Shadows and transitions
- Grid layouts (`grid md:grid-cols-2`)

### Customization
Edit `tailwind.config.js` to customize colors, fonts, spacing, and more.

## 🌐 API Integration

Ready for integration with the backend API running on `http://localhost:3000`. The app is structured to easily add:

- User authentication
- Team management
- Real-time updates
- Form handling

## 📱 Features

Current implementation includes:
- Welcome landing page
- Responsive design
- Component-based architecture
- TypeScript for type safety
- Modern React patterns

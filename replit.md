# Dylan Patisserie Menu Application

## Overview

This is a React-based tablet menu application for Dylan Patisserie, designed to provide an elegant digital ordering experience. The application features a modern, sophisticated UI with glassmorphism effects, premium animations, and a multi-step user flow. Customers enter their table number, select a category (Food/Drinks/All Items), browse items, and place orders that are automatically routed to kitchen and bar.

## User Preferences

Preferred communication style: Simple, everyday language.

## Recent Changes (January 2025)

- ✓ Redesigned interface with modern glassmorphism and premium animations
- ✓ Added separate category selection screen with interactive cards
- ✓ Implemented multi-step flow: Table Input → Category Selection → Menu → Cart
- ✓ Enhanced visual design with morphing backgrounds and floating elements
- ✓ Updated menu cards with backdrop blur and hover effects
- ✓ Removed category buttons from header in favor of dedicated selection screen
- ✓ Implemented full mobile responsiveness (320px-480px viewports)
- ✓ Added staggered animations for menu items with fade-in-up effects
- ✓ Optimized all components for touch-friendly mobile interaction
- ✓ Enhanced brand consistency using only white, black, and gold (#D4AF37) colors
- ✓ Created modern, elegant category item animations with slide-in effects

## System Architecture

The application follows a modern full-stack architecture with clear separation between client and server concerns:

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **Routing**: Wouter for lightweight client-side routing
- **State Management**: Zustand for global cart state management
- **UI Components**: Radix UI primitives with shadcn/ui design system
- **Styling**: Tailwind CSS with custom Dylan Patisserie branding
- **Build Tool**: Vite for fast development and optimized builds

### Backend Architecture
- **Runtime**: Node.js with Express.js server
- **Language**: TypeScript throughout
- **Development**: Hot reloading with Vite middleware integration
- **Static Assets**: Served via Express with Vite dev middleware

## Key Components

### Client-Side Components
- **Pages**: Table input, menu browsing, cart management, and order confirmation
- **UI Components**: Menu item cards, cart items, item detail modals, and recommendation system
- **State Management**: Centralized cart store with persistent table number
- **Data Layer**: Static menu data with recommendation algorithms

### Server-Side Components
- **Express Server**: Minimal API surface with health check endpoint
- **Storage Layer**: In-memory storage implementation with user management interface
- **Development Tools**: Request logging, error handling, and Vite integration

### Shared Schema
- **Type Safety**: Zod schemas for menu items, cart items, and orders
- **Data Validation**: Runtime validation for all data structures
- **Type Generation**: TypeScript types derived from Zod schemas

## Data Flow

1. **Table Selection**: Users input their table number to begin the session
2. **Menu Browsing**: Static menu data is filtered by category (food/drinks)
3. **Item Selection**: Detailed item modals allow quantity selection and cart addition
4. **Cart Management**: Real-time cart updates with quantity adjustments and recommendations
5. **Order Placement**: Orders are logged separately for kitchen (food) and bar (drinks)
6. **Confirmation**: Users receive order confirmation with order number

### Recommendation System
- **Smart Pairing**: Suggests drinks with desserts, tea with pastries
- **Context-Aware**: Recommendations based on current cart contents
- **Category Mixing**: Encourages beverage additions to food orders

## External Dependencies

### Core Dependencies
- **@neondatabase/serverless**: Database connectivity (PostgreSQL ready)
- **drizzle-orm**: Type-safe database ORM with migrations
- **@tanstack/react-query**: Server state management and caching
- **@radix-ui/react-***: Accessible UI component primitives

### Development Dependencies
- **Vite**: Build tool and development server
- **TypeScript**: Static type checking
- **Tailwind CSS**: Utility-first styling framework
- **PostCSS**: CSS processing and optimization

### Custom Assets
- Dylan Patisserie logo and branding assets
- High-quality food and beverage images from Unsplash

## Deployment Strategy

### Development Mode
- Vite dev server with HMR for instant updates
- Express middleware integration for seamless full-stack development
- TypeScript compilation with path mapping support

### Production Build
- Vite production build with optimized bundling
- ESBuild for server-side TypeScript compilation
- Static asset serving through Express

### Database Integration
- Drizzle ORM configured for PostgreSQL
- Migration system ready for schema evolution
- Environment-based database URL configuration

### Replit Integration
- Cartographer plugin for enhanced development experience
- Runtime error overlay for debugging
- Development banner for external access

The application is designed to be easily deployable on Replit or similar platforms, with clear separation between development and production configurations. The modular architecture allows for easy feature additions and maintenance.
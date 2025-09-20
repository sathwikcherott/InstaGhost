# Instagram Follower Analysis Tool

## Overview

This is a privacy-focused Instagram follower analysis tool that helps users identify who doesn't follow them back on Instagram. The application provides two methods for data analysis: file upload (using Instagram's official data export) and browser extension integration for automated data capture. Built with a React frontend, Express backend, and PostgreSQL database using Drizzle ORM, the tool emphasizes user privacy by processing data locally without requiring Instagram login credentials.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
**Framework**: React with TypeScript, built using Vite for fast development and optimized builds
**UI Library**: Shadcn/ui components built on Radix UI primitives with Tailwind CSS for styling
**Design System**: Material Design principles with Instagram-inspired color palette (purple-pink gradient)
**State Management**: React useState hooks for local component state, TanStack Query for server state management
**Routing**: Wouter for lightweight client-side routing
**Styling**: Tailwind CSS with custom design tokens, supporting both light and dark modes

### Data Processing Pipeline
**Local Processing**: All Instagram data analysis happens client-side for privacy
**File Parsing**: Supports JSON format from Instagram's official data export
**Analysis Engine**: Compares followers vs following lists to identify non-mutual connections
**Export Functionality**: CSV export capability for analysis results

### Browser Extension Integration
**Chrome Extension**: Manifest V3 compatible extension for automated Instagram data capture
**Security Model**: Uses postMessage API for secure communication between extension and web app
**Content Scripts**: Separate scripts for Instagram pages and analyzer app pages
**Background Service Worker**: Manages communication between extension components

### Backend Architecture
**Server Framework**: Express.js with TypeScript
**Database ORM**: Drizzle ORM with PostgreSQL database (Neon Database for cloud hosting)
**Schema Management**: Drizzle-kit for database migrations and schema evolution
**Session Management**: PostgreSQL-based session storage using connect-pg-simple
**API Design**: RESTful endpoints with JSON responses, error handling middleware

### Component Architecture
**Reusable Components**: Modular UI components (FileUpload, ProgressIndicator, StatisticsCard, etc.)
**Layout System**: Consistent spacing and typography using Tailwind design tokens
**Responsive Design**: Mobile-first approach with adaptive layouts
**Accessibility**: Radix UI primitives ensure keyboard navigation and screen reader support

### Data Models
**User Schema**: Basic user authentication (id, username, password)
**Instagram Data Schema**: Structured types for followers/following lists with Zod validation
**Analysis Results**: Typed results including statistics and non-follower lists

### Development Workflow
**Build System**: Vite for frontend bundling, esbuild for backend compilation
**Type Safety**: Full TypeScript coverage across frontend, backend, and shared schemas
**Code Quality**: ESLint and Prettier configuration, path aliases for clean imports
**Development Server**: Hot module replacement for frontend, tsx for backend development

## External Dependencies

### Core Infrastructure
- **Neon Database**: PostgreSQL cloud database service for user data and session storage
- **Google Fonts**: Inter font family for consistent typography across the application

### UI and Styling
- **Radix UI**: Comprehensive primitive components for accessibility and customization
- **Tailwind CSS**: Utility-first CSS framework with custom design system extensions
- **Lucide React**: Consistent icon library for UI elements

### Development Tools
- **Vite**: Build tool and development server with optimized bundling
- **Drizzle Kit**: Database schema management and migration tooling
- **TanStack Query**: Server state management with caching and synchronization

### Browser Extension
- **Chrome Extensions API**: Manifest V3 for modern browser extension development
- **Content Script Security**: Secure communication patterns between extension and web app

### Data Processing
- **Zod**: Runtime type validation for Instagram data schemas
- **CSV Generation**: Client-side CSV export functionality for analysis results

### Authentication & Security
- **Password Hashing**: Secure user credential storage (implementation pending)
- **Session Management**: PostgreSQL-backed session storage for user authentication
- **CORS Protection**: Configured for secure cross-origin requests